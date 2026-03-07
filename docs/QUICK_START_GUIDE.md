# Quick Start Guide - Week 1

**Welcome!** This guide will help you start immediately. Don't feel overwhelmed by the full 60-day plan - focus on just this week.

---

## 🎯 Week 1 Mission

Build **2 simple projects** to learn:
1. Spring Boot backend (Task Manager API)
2. Node.js backend + React frontend (Blog App)

**Time**: 4-5 hours/day for 7 days

---

## 📋 Day-by-Day Breakdown

### **Day 1: Setup Everything** (3 hours)

**Morning (1.5 hours)**: Install tools
```bash
# Check Java version
java -version  # Should be 21+

# Check Node.js
node -v  # Should be 20+

# Install Docker Desktop
# Download from: https://www.docker.com/products/docker-desktop

# Check installations
docker --version
git --version
```

**Afternoon (1.5 hours)**: Create GitHub account and first repo
```bash
# Configure Git
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Create SSH key for GitHub
ssh-keygen -t ed25519 -C "your.email@example.com"
# Copy key: cat ~/.ssh/id_ed25519.pub
# Add to GitHub: Settings → SSH Keys

# Create your first repo on GitHub: "learning-journey"
git clone git@github.com:yourusername/learning-journey.git
cd learning-journey
echo "# My 60-Day Learning Journey" > README.md
git add .
git commit -m "Initial commit: Starting my journey"
git push
```

**Evening**: Watch quick tutorials
- Spring Boot basics (30 min)
- Node.js basics (30 min)

---

### **Day 2-3: Build Task Manager API** (6 hours total)

**Day 2 Morning**: Set up Spring Boot project

```bash
# Go to https://start.spring.io/
# Configure:
# - Project: Maven
# - Language: Java
# - Spring Boot: 3.2.x
# - Java: 21
# - Dependencies: Spring Web, Spring Data JPA, PostgreSQL Driver, Lombok

# Download and extract
# Open in IntelliJ IDEA
```

**Day 2 Afternoon**: Create your first entity

```java
// src/main/java/com/example/taskmanager/model/Task.java
@Entity
@Table(name = "tasks")
@Data
@NoArgsConstructor
@AllArgsConstructor
@Builder
public class Task {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @Column(nullable = false)
    private String title;

    private String description;

    @Enumerated(EnumType.STRING)
    private TaskStatus status = TaskStatus.TODO;

    @CreationTimestamp
    private LocalDateTime createdAt;

    public enum TaskStatus {
        TODO, IN_PROGRESS, DONE
    }
}
```

**Day 3**: Complete the API

```java
// Repository
@Repository
public interface TaskRepository extends JpaRepository<Task, Long> {
}

// Service
@Service
@RequiredArgsConstructor
public class TaskService {
    private final TaskRepository taskRepository;

    public List<Task> getAllTasks() {
        return taskRepository.findAll();
    }

    public Task createTask(Task task) {
        return taskRepository.save(task);
    }

    public Task getTask(Long id) {
        return taskRepository.findById(id)
            .orElseThrow(() -> new ResponseStatusException(HttpStatus.NOT_FOUND));
    }

    public Task updateTask(Long id, Task taskDetails) {
        Task task = getTask(id);
        task.setTitle(taskDetails.getTitle());
        task.setDescription(taskDetails.getDescription());
        task.setStatus(taskDetails.getStatus());
        return taskRepository.save(task);
    }

    public void deleteTask(Long id) {
        taskRepository.deleteById(id);
    }
}

// Controller
@RestController
@RequestMapping("/api/tasks")
@RequiredArgsConstructor
public class TaskController {
    private final TaskService taskService;

    @GetMapping
    public List<Task> getAllTasks() {
        return taskService.getAllTasks();
    }

    @PostMapping
    public Task createTask(@RequestBody Task task) {
        return taskService.createTask(task);
    }

    @GetMapping("/{id}")
    public Task getTask(@PathVariable Long id) {
        return taskService.getTask(id);
    }

    @PutMapping("/{id}")
    public Task updateTask(@PathVariable Long id, @RequestBody Task task) {
        return taskService.updateTask(id, task);
    }

    @DeleteMapping("/{id}")
    public ResponseEntity<?> deleteTask(@PathVariable Long id) {
        taskService.deleteTask(id);
        return ResponseEntity.ok().build();
    }
}
```

**Configure PostgreSQL**:
```yaml
# application.yml
spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/taskdb
    username: postgres
    password: postgres
  jpa:
    hibernate:
      ddl-auto: create-drop
    show-sql: true
```

**Run PostgreSQL with Docker**:
```bash
docker run --name postgres-task \
  -e POSTGRES_PASSWORD=postgres \
  -e POSTGRES_DB=taskdb \
  -p 5432:5432 \
  -d postgres:15
```

**Test your API**:
```bash
# Start Spring Boot
mvn spring-boot:run

# Test with curl
curl -X POST http://localhost:8080/api/tasks \
  -H "Content-Type: application/json" \
  -d '{"title": "Learn Spring Boot", "description": "Build a REST API"}'

curl http://localhost:8080/api/tasks
```

**Commit your work**:
```bash
git add .
git commit -m "feat: Add Task Manager API with CRUD operations"
git push
```

✅ **Checkpoint**: You should have a working Spring Boot API!

---

### **Day 4-5: Build Blog API (Node.js)** (6 hours total)

**Day 4**: Set up Node.js project with authentication

```bash
mkdir blog-api
cd blog-api
npm init -y
npm install express mongoose bcrypt jsonwebtoken dotenv
npm install -D nodemon

# Update package.json scripts
"scripts": {
  "start": "node server.js",
  "dev": "nodemon server.js"
}
```

Create project structure:
```
blog-api/
├── models/
│   ├── User.js
│   └── Post.js
├── routes/
│   ├── auth.js
│   └── posts.js
├── middleware/
│   └── auth.js
├── server.js
└── .env
```

**Key files**:

```javascript
// models/User.js
const mongoose = require('mongoose');

const userSchema = new mongoose.Schema({
  email: { type: String, required: true, unique: true },
  password: { type: String, required: true },
  name: { type: String, required: true }
}, { timestamps: true });

module.exports = mongoose.model('User', userSchema);

// models/Post.js
const postSchema = new mongoose.Schema({
  title: { type: String, required: true },
  content: { type: String, required: true },
  author: { type: mongoose.Schema.Types.ObjectId, ref: 'User', required: true }
}, { timestamps: true });

module.exports = mongoose.model('Post', postSchema);

// middleware/auth.js
const jwt = require('jsonwebtoken');

module.exports = (req, res, next) => {
  try {
    const token = req.header('Authorization').replace('Bearer ', '');
    const decoded = jwt.verify(token, process.env.JWT_SECRET);
    req.userId = decoded.userId;
    next();
  } catch (error) {
    res.status(401).json({ error: 'Please authenticate' });
  }
};

// server.js
const express = require('express');
const mongoose = require('mongoose');
require('dotenv').config();

const app = express();
app.use(express.json());

mongoose.connect(process.env.MONGODB_URI);

app.use('/api/auth', require('./routes/auth'));
app.use('/api/posts', require('./routes/posts'));

app.listen(3000, () => console.log('Server running on port 3000'));
```

**Run MongoDB**:
```bash
docker run --name mongodb-blog \
  -p 27017:27017 \
  -d mongo:7
```

**.env file**:
```
MONGODB_URI=mongodb://localhost:27017/blogdb
JWT_SECRET=your-secret-key-here
```

**Day 5**: Implement auth and posts routes (see full plan for complete code)

✅ **Checkpoint**: Working Node.js API with JWT auth

---

### **Day 6-7: Build React Frontend** (6 hours total)

```bash
npx create-react-app blog-frontend
cd blog-frontend
npm install axios react-router-dom
npm start
```

**Day 6**: Authentication UI
- Login page
- Register page
- Token storage

**Day 7**: Blog UI
- Post list
- Create post form
- Edit/Delete functionality

✅ **Checkpoint**: Full-stack blog application working!

---

## 🎯 Week 1 Success Criteria

By Sunday evening, you should have:

- [ ] ✅ Task Manager API (Spring Boot) - working and on GitHub
- [ ] ✅ Blog API (Node.js) - working and on GitHub
- [ ] ✅ Blog Frontend (React) - can login and create posts
- [ ] ✅ Both projects running locally
- [ ] ✅ All code committed to GitHub with good commit messages
- [ ] ✅ Basic understanding of REST APIs, JWT, and React

**Total GitHub commits**: Aim for 20+

---

## 💡 Quick Tips for Week 1

### When You Get Stuck
1. **Google the exact error message** - 90% of errors are solved this way
2. **Check Stack Overflow** - someone had your problem before
3. **Use ChatGPT/Claude** - paste error and ask for help
4. **Read documentation** - Spring Boot and Express docs are excellent

### Time Management
- **Morning (2 hours)**: Focused coding
- **Evening (2-3 hours)**: Continue + learning
- **Don't code for 5 hours straight** - take 10min breaks every hour

### Commit Messages
Good:
```
feat: Add user authentication with JWT
fix: Resolve CORS issue in API
docs: Update README with setup instructions
```

Bad:
```
updated files
fixes
code
```

### Don't Get Stuck On
- Perfect code - done is better than perfect
- Understanding everything - learn by doing
- Styling - focus on functionality first

---

## 📚 Resources for Week 1

### Documentation
- Spring Boot: https://spring.io/guides/gs/rest-service/
- Express: https://expressjs.com/en/starter/installing.html
- React: https://react.dev/learn

### Video Tutorials (If Stuck)
- Spring Boot REST API: Search "Spring Boot REST API tutorial" on YouTube
- Node.js Auth: Search "Node.js JWT authentication" on YouTube
- React basics: Search "React hooks tutorial" on YouTube

### Communities (For Questions)
- r/learnjava
- r/node
- r/reactjs
- Stack Overflow

---

## ✅ End of Week 1 Checklist

Before moving to Week 2:

- [ ] Task Manager API works via Postman
- [ ] Blog API authentication working (can register/login)
- [ ] React app communicates with backend
- [ ] All code on GitHub with READMEs
- [ ] PostgreSQL and MongoDB running in Docker
- [ ] Can explain what you built to someone

**If all checked**: Congrats! You're ready for Week 2 🚀

**If some unchecked**: That's okay! Take an extra day or two to solidify Week 1. The foundation is critical.

---

## 🎊 Celebrate Your Progress!

Week 1 is the hardest because everything is new. If you made it this far:

1. **Tweet about it**: "Just completed Week 1 of my 60-day learning journey! Built my first Spring Boot API and Node.js app. #100DaysOfCode"

2. **Update LinkedIn**: Add the projects to your profile

3. **Tell someone**: Share what you learned with a friend

**You've got this!** See you in Week 2 where we add Docker, testing, and CI/CD.

---

## 📞 Need Help?

If you're truly stuck:
1. Read the error message carefully
2. Google: "spring boot [your error]" or "react [your error]"
3. Ask ChatGPT/Claude: "I'm getting this error: [paste error]. Here's my code: [paste code]"
4. Check the full learning plan for more detailed examples

**Remember**: Every expert was once a beginner. Struggling is part of learning!

---

**Next**: After completing Week 1, open `BACKEND_FULLSTACK_LEARNING_PLAN.md` and start Week 2!
