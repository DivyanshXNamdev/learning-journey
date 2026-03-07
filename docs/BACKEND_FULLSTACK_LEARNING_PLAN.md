# Backend/Full Stack Engineer - 2 Month Learning Plan
## March 6 - May 6, 2026

> **Goal**: Master in-demand backend/full-stack skills and build portfolio projects to land engineering roles in 2026

---

## 📊 Plan Overview

**Duration**: 8 weeks (60 days)
**Time Commitment**: 4-5 hours/day (120-150 total hours)
**Projects**: 3 production-ready portfolio projects
**Primary Focus**: Backend with Full Stack capabilities

### Core Technologies You'll Master
- **Backend**: Java Spring Boot, Node.js/Express, Go (basics)
- **Frontend**: React/Next.js (essential full-stack skills)
- **Databases**: PostgreSQL, MongoDB, Redis
- **Infrastructure**: Docker, Kubernetes, AWS
- **Messaging**: Kafka, WebSockets
- **DevOps**: CI/CD, monitoring, testing
- **AI Integration**: OpenAI API, RAG patterns

---

## 🎯 Three Flagship Projects

1. **Cloud-Native Microservices E-Commerce** (Weeks 3-4)
2. **Real-Time Event-Driven Analytics Dashboard** (Weeks 5-6)
3. **AI-Powered Full Stack SaaS Application** (Weeks 7-8)

---

# WEEK 1: Foundations & Environment Setup

## Session 1.1: Development Environment (Day 1)
**Duration**: 3 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Set up professional development environment
- Understand modern development workflows
- Master version control and collaboration tools

### Tasks
- [ ] Install Java 21+ (or 25 if available)
- [ ] Install Node.js 20+ LTS
- [ ] Install Docker Desktop
- [ ] Install VS Code + IntelliJ IDEA Community
- [ ] Configure Git and create GitHub account
- [ ] Set up GitHub SSH keys
- [ ] Install Postman/Insomnia for API testing
- [ ] Install PostgreSQL locally

### Hands-on Exercise
Create a GitHub repository with:
- README.md with your learning goals
- .gitignore configured for Java and Node.js
- First commit with proper commit message format

### Resources
- Git workflow: https://www.atlassian.com/git/tutorials
- GitHub SSH setup: https://docs.github.com/en/authentication

---

## Session 1.2: Spring Boot Fundamentals (Days 2-3)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Understand Spring Boot architecture
- Build RESTful APIs
- Implement dependency injection
- Work with Spring Data JPA

### Tasks
- [ ] Learn Spring Boot project structure
- [ ] Study @RestController, @Service, @Repository layers
- [ ] Understand application.properties/yml configuration
- [ ] Learn Spring Boot auto-configuration
- [ ] Study JPA entity relationships (@OneToMany, @ManyToMany)

### Hands-on Exercise
**Build**: Simple Task Manager API
- CRUD endpoints for tasks
- PostgreSQL database
- Proper layered architecture (Controller → Service → Repository)
- Exception handling with @ControllerAdvice
- Input validation with Bean Validation

**API Endpoints**:
```
POST   /api/tasks          - Create task
GET    /api/tasks          - List all tasks
GET    /api/tasks/{id}     - Get task by ID
PUT    /api/tasks/{id}     - Update task
DELETE /api/tasks/{id}     - Delete task
```

### Validation Checkpoint
- [ ] All CRUD operations work via Postman
- [ ] Data persists in PostgreSQL
- [ ] Proper error responses (404, 400, 500)
- [ ] Code pushed to GitHub with clear commits

### Resources
- Spring Boot Guides: https://spring.io/guides
- Baeldung Spring Boot: https://www.baeldung.com/spring-boot

---

## Session 1.3: Node.js & Express Basics (Days 4-5)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Understand Node.js event loop and async patterns
- Build REST APIs with Express
- Work with MongoDB
- Implement middleware patterns

### Tasks
- [ ] Learn Node.js fundamentals (callbacks, promises, async/await)
- [ ] Study Express routing and middleware
- [ ] Learn MongoDB with Mongoose ODM
- [ ] Understand environment variables with dotenv
- [ ] Study JWT authentication basics

### Hands-on Exercise
**Build**: Blog API with Authentication
- User registration and login (JWT)
- Blog post CRUD (authenticated users only)
- MongoDB for data storage
- Middleware for authentication
- Password hashing with bcrypt

**API Endpoints**:
```
POST   /api/auth/register  - Register user
POST   /api/auth/login     - Login (returns JWT)
GET    /api/posts          - List posts (public)
POST   /api/posts          - Create post (authenticated)
PUT    /api/posts/:id      - Update post (authenticated, author only)
DELETE /api/posts/:id      - Delete post (authenticated, author only)
```

### Validation Checkpoint
- [ ] JWT authentication working
- [ ] Protected routes require valid token
- [ ] Passwords are hashed
- [ ] MongoDB relationships working (User → Posts)
- [ ] Code on GitHub with documentation

### Resources
- Node.js docs: https://nodejs.org/docs
- Express guide: https://expressjs.com/en/guide
- MongoDB University (free): https://university.mongodb.com/

---

## Session 1.4: React Fundamentals (Days 6-7)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Understand React components and hooks
- Master state management
- Work with React Router
- Call APIs from React

### Tasks
- [ ] Learn functional components and JSX
- [ ] Study useState, useEffect, useContext hooks
- [ ] Understand component lifecycle
- [ ] Learn React Router v6
- [ ] Study API calls with fetch/axios
- [ ] Learn form handling in React

### Hands-on Exercise
**Build**: Frontend for Blog API (Session 1.3)
- Login/Register forms
- Blog post list view
- Create/Edit post forms (authenticated)
- Protected routes (React Router)
- JWT token storage (localStorage)
- Loading states and error handling

### Validation Checkpoint
- [ ] Login/Register working with backend API
- [ ] Token stored and sent with authenticated requests
- [ ] CRUD operations functional from UI
- [ ] Proper error messages displayed
- [ ] Responsive design (basic CSS/Tailwind)

### Resources
- React docs: https://react.dev
- React Router: https://reactrouter.com/

---

## 🎓 WEEK 1 CHECKPOINT

### Completed Skills
- [ ] Spring Boot REST APIs
- [ ] Node.js/Express with MongoDB
- [ ] React frontend basics
- [ ] JWT authentication
- [ ] Git workflow

### Portfolio Status
- [ ] 2 projects on GitHub (Task Manager + Blog App)
- [ ] Both projects documented with README
- [ ] Basic full-stack application complete

### Self-Assessment Questions
1. Can you explain the layered architecture in Spring Boot?
2. What's the difference between authentication and authorization?
3. How does React's virtual DOM work?
4. Can you explain the Node.js event loop?

**If you can't answer these confidently, review Week 1 materials before proceeding.**

---

# WEEK 2: Databases, Docker & DevOps Fundamentals

## Session 2.1: Database Deep Dive (Days 8-9)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Master SQL and NoSQL patterns
- Understand database indexing and optimization
- Learn Redis for caching
- Study database transactions and ACID

### Tasks
- [ ] Learn PostgreSQL advanced features (indexes, views, triggers)
- [ ] Study query optimization and EXPLAIN plans
- [ ] Learn MongoDB aggregation pipeline
- [ ] Understand Redis data structures (strings, hashes, lists, sets)
- [ ] Study caching strategies (cache-aside, write-through)
- [ ] Learn database connection pooling

### Hands-on Exercise
**Enhance Task Manager API** (from Session 1.2):
- Add database indexes for frequently queried fields
- Implement Redis caching for GET requests
- Add cache invalidation on updates
- Implement pagination for task lists
- Add filtering and sorting capabilities
- Monitor query performance with EXPLAIN

**New Features**:
```
GET /api/tasks?page=1&size=10&sort=createdAt&filter=status:ACTIVE
```

### Validation Checkpoint
- [ ] Redis cache working (verify cache hits in logs)
- [ ] Pagination working correctly
- [ ] Query performance improved (measure before/after)
- [ ] Database indexes created
- [ ] Cache invalidation working on updates

### Resources
- PostgreSQL Tutorial: https://www.postgresqltutorial.com/
- Redis University: https://university.redis.com/

---

## Session 2.2: Docker Fundamentals (Days 10-11)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Understand containerization concepts
- Build Docker images
- Work with Docker Compose
- Manage multi-container applications

### Tasks
- [ ] Learn Docker concepts (images, containers, volumes, networks)
- [ ] Study Dockerfile best practices
- [ ] Learn multi-stage builds
- [ ] Study Docker Compose for local development
- [ ] Understand container networking
- [ ] Learn volume management for data persistence

### Hands-on Exercise
**Dockerize Both Applications**:

1. **Task Manager API** (Spring Boot + PostgreSQL + Redis)
    - Create Dockerfile with multi-stage build
    - Create docker-compose.yml
    - Configure PostgreSQL and Redis services
    - Set up health checks

2. **Blog App** (Node.js + MongoDB + React)
    - Dockerize backend
    - Dockerize frontend with Nginx
    - Create docker-compose.yml
    - Configure MongoDB service

### Validation Checkpoint
- [ ] Both apps start with `docker-compose up`
- [ ] No manual setup required (databases auto-initialized)
- [ ] Environment variables configured properly
- [ ] Services can communicate (backend ↔ database)
- [ ] Data persists after container restart (volumes working)

### Docker Compose Structure
```yaml
# Example for Task Manager
services:
  api:
    build: .
    ports: ["8080:8080"]
    depends_on: [db, redis]
  db:
    image: postgres:15
    volumes: [postgres-data:/var/lib/postgresql/data]
  redis:
    image: redis:7-alpine
```

### Resources
- Docker tutorial: https://docs.docker.com/get-started/
- Docker best practices: https://docs.docker.com/develop/dev-best-practices/

---

## Session 2.3: Testing Fundamentals (Days 12-13)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Write unit tests
- Implement integration tests
- Understand test-driven development (TDD)
- Learn mocking and test containers

### Tasks
- [ ] Learn JUnit 5 for Java testing
- [ ] Study Mockito for mocking dependencies
- [ ] Learn Jest for JavaScript/Node.js testing
- [ ] Study React Testing Library
- [ ] Understand test coverage metrics
- [ ] Learn Testcontainers for integration tests

### Hands-on Exercise
**Add comprehensive tests to both projects**:

**Task Manager API Tests**:
- Unit tests for service layer (mock repository)
- Integration tests for controllers (MockMvc)
- Integration tests with real database (Testcontainers)
- Achieve >80% code coverage

**Blog API Tests**:
- Unit tests with Jest
- Integration tests with supertest
- React component tests with Testing Library
- Mock API calls in frontend tests

### Test Examples
```java
// Spring Boot Integration Test
@SpringBootTest
@Testcontainers
class TaskControllerIT {
    @Container
    static PostgreSQLContainer<?> postgres = new PostgreSQLContainer<>("postgres:15");

    @Test
    void shouldCreateTask() {
        // Test implementation
    }
}
```

```javascript
// Node.js Integration Test
describe('POST /api/posts', () => {
  it('should create post with valid token', async () => {
    const response = await request(app)
      .post('/api/posts')
      .set('Authorization', `Bearer ${validToken}`)
      .send({ title: 'Test', content: 'Content' });
    expect(response.status).toBe(201);
  });
});
```

### Validation Checkpoint
- [ ] All tests pass locally
- [ ] Code coverage >80% for backend
- [ ] Integration tests use Testcontainers
- [ ] Frontend components have tests
- [ ] Tests run in CI (GitHub Actions - next session)

### Resources
- JUnit 5 docs: https://junit.org/junit5/docs/current/user-guide/
- Jest docs: https://jestjs.io/docs/getting-started
- Testcontainers: https://testcontainers.com/

---

## Session 2.4: CI/CD Pipeline (Day 14)
**Duration**: 4 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Understand CI/CD concepts
- Build GitHub Actions workflows
- Automate testing and deployment
- Implement code quality checks

### Tasks
- [ ] Learn GitHub Actions syntax
- [ ] Study workflow triggers (push, PR, schedule)
- [ ] Understand jobs and steps
- [ ] Learn secrets management
- [ ] Study artifact publishing

### Hands-on Exercise
**Create GitHub Actions workflows for both projects**:

1. **CI Pipeline** (runs on every push/PR):
    - Checkout code
    - Set up Java/Node.js
    - Run tests
    - Generate coverage report
    - Upload coverage to Codecov
    - Build Docker image

2. **CD Pipeline** (runs on main branch):
    - Run CI steps
    - Build and push Docker image to Docker Hub
    - (Deployment to cloud - Week 4)

### Workflow Example
```yaml
# .github/workflows/ci.yml
name: CI Pipeline
on: [push, pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-java@v4
        with:
          java-version: '21'
      - name: Run tests
        run: mvn test
      - name: Upload coverage
        uses: codecov/codecov-action@v3
```

### Validation Checkpoint
- [ ] CI pipeline runs on every commit
- [ ] Tests run automatically
- [ ] Coverage reports generated
- [ ] Build fails if tests fail
- [ ] Status badges added to README

### Resources
- GitHub Actions docs: https://docs.github.com/en/actions

---

## 🎓 WEEK 2 CHECKPOINT

### Completed Skills
- [ ] Database optimization and caching
- [ ] Docker containerization
- [ ] Comprehensive testing strategies
- [ ] CI/CD with GitHub Actions

### Portfolio Status
- [ ] Both projects fully containerized
- [ ] Test coverage >80%
- [ ] CI/CD pipelines active
- [ ] Professional README with badges

### Weekly Review
**Answer these questions**:
1. Why is Redis faster than PostgreSQL for caching?
2. What's the difference between Docker images and containers?
3. Why are integration tests important alongside unit tests?
4. What triggers a CI pipeline in your projects?

---

# WEEK 3-4: PROJECT 1 - Cloud-Native Microservices E-Commerce

## Overview
**Goal**: Build a production-ready microservices application demonstrating distributed systems expertise

**Architecture**:
- 4 microservices (User, Product, Order, Notification)
- API Gateway (Spring Cloud Gateway)
- Service Discovery (Eureka)
- Inter-service communication (REST + Kafka)
- Distributed caching (Redis)
- Centralized logging
- Monitoring and tracing

---

## Session 3.1: Microservices Architecture Design (Day 15)
**Duration**: 4 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Understand microservices patterns
- Learn service decomposition
- Design inter-service communication
- Plan data management strategies

### Tasks
- [ ] Study microservices architecture principles
- [ ] Learn Spring Cloud ecosystem (Gateway, Eureka, Config)
- [ ] Understand API Gateway patterns
- [ ] Study service discovery mechanisms
- [ ] Learn distributed tracing concepts
- [ ] Design database-per-service pattern

### Architecture Planning
**Design your system**:
1. Create architecture diagram (use draw.io or Excalidraw)
2. Define service boundaries
3. Plan API contracts between services
4. Design database schemas for each service
5. Plan Kafka topics for events

**Services**:
- **User Service**: Authentication, user management (PostgreSQL)
- **Product Service**: Product catalog, inventory (PostgreSQL)
- **Order Service**: Order processing, cart (PostgreSQL)
- **Notification Service**: Email/SMS notifications (MongoDB for logs)
- **API Gateway**: Request routing, authentication
- **Service Registry**: Eureka for service discovery

**Event Topics**:
- `user.registered` - User registration events
- `order.created` - New order events
- `order.completed` - Order completion events
- `inventory.updated` - Stock updates

### Validation Checkpoint
- [ ] Architecture diagram complete
- [ ] Service boundaries clearly defined
- [ ] API contracts documented (OpenAPI/Swagger)
- [ ] Database schemas designed
- [ ] Kafka event schemas defined

---

## Session 3.2: Service Registry & API Gateway (Days 16-17)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Implement Eureka service registry
- Build API Gateway with Spring Cloud Gateway
- Configure service routing
- Implement gateway filters

### Tasks
- [ ] Set up Eureka Server
- [ ] Configure Spring Cloud Gateway
- [ ] Implement service registration
- [ ] Set up routing rules
- [ ] Add authentication filter in gateway
- [ ] Implement rate limiting

### Hands-on Exercise
**Build Core Infrastructure**:

1. **Eureka Server**:
```java
@SpringBootApplication
@EnableEurekaServer
public class ServiceRegistryApplication {
    public static void main(String[] args) {
        SpringApplication.run(ServiceRegistryApplication.class, args);
    }
}
```

2. **API Gateway**:
```yaml
# application.yml
spring:
  cloud:
    gateway:
      routes:
        - id: user-service
          uri: lb://USER-SERVICE
          predicates:
            - Path=/api/users/**
        - id: product-service
          uri: lb://PRODUCT-SERVICE
          predicates:
            - Path=/api/products/**
```

3. **Docker Compose** for infrastructure:
```yaml
services:
  eureka-server:
    build: ./eureka-server
    ports: ["8761:8761"]

  api-gateway:
    build: ./api-gateway
    ports: ["8080:8080"]
    depends_on: [eureka-server]

  postgres:
    image: postgres:15

  kafka:
    image: confluentinc/cp-kafka:7.5.0

  redis:
    image: redis:7-alpine
```

### Validation Checkpoint
- [ ] Eureka UI accessible at http://localhost:8761
- [ ] Gateway routes requests correctly
- [ ] Services register with Eureka
- [ ] Gateway can discover services dynamically
- [ ] Rate limiting working (test with multiple requests)

---

## Session 3.3: User Service (Days 18-19)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Implement OAuth2/JWT authentication
- Build user management service
- Integrate with service registry
- Implement Spring Security

### Tasks
- [ ] Set up User Service Spring Boot project
- [ ] Configure Eureka client
- [ ] Implement User entity and repository
- [ ] Build authentication endpoints
- [ ] Implement JWT token generation
- [ ] Add role-based authorization
- [ ] Publish `user.registered` event to Kafka

### API Endpoints
```
POST /api/users/register        - Register new user
POST /api/users/login           - Login (returns JWT)
GET  /api/users/me              - Get current user
PUT  /api/users/me              - Update current user
GET  /api/users/{id}            - Get user by ID (admin only)
```

### Implementation Example
```java
@Service
public class AuthService {
    @Autowired
    private UserRepository userRepository;

    @Autowired
    private KafkaTemplate<String, UserEvent> kafkaTemplate;

    public AuthResponse register(RegisterRequest request) {
        User user = User.builder()
            .email(request.getEmail())
            .password(passwordEncoder.encode(request.getPassword()))
            .role(Role.USER)
            .build();

        userRepository.save(user);

        // Publish event
        kafkaTemplate.send("user.registered", new UserRegisteredEvent(user.getId()));

        return generateAuthResponse(user);
    }
}
```

### Validation Checkpoint
- [ ] Registration working
- [ ] Login returns valid JWT
- [ ] JWT contains user ID and roles
- [ ] Protected endpoints require valid token
- [ ] Kafka event published on registration
- [ ] Service registers with Eureka

---

## Session 3.4: Product Service (Days 20-21)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Build CRUD service with caching
- Implement Redis caching strategy
- Add search and filtering
- Publish inventory events

### Tasks
- [ ] Set up Product Service
- [ ] Implement Product entity with inventory
- [ ] Add Redis caching with @Cacheable
- [ ] Implement search with specifications
- [ ] Add pagination and sorting
- [ ] Publish `inventory.updated` events

### API Endpoints
```
GET    /api/products              - List products (with search, pagination)
GET    /api/products/{id}         - Get product details
POST   /api/products              - Create product (admin only)
PUT    /api/products/{id}         - Update product (admin only)
DELETE /api/products/{id}         - Delete product (admin only)
PATCH  /api/products/{id}/inventory - Update inventory
```

### Caching Implementation
```java
@Service
public class ProductService {
    @Cacheable(value = "products", key = "#id")
    public Product getProduct(Long id) {
        return productRepository.findById(id)
            .orElseThrow(() -> new ProductNotFoundException(id));
    }

    @CacheEvict(value = "products", key = "#id")
    public void updateInventory(Long id, int quantity) {
        Product product = getProduct(id);
        product.setInventory(quantity);
        productRepository.save(product);

        kafkaTemplate.send("inventory.updated",
            new InventoryUpdatedEvent(id, quantity));
    }
}
```

### Validation Checkpoint
- [ ] CRUD operations working
- [ ] Redis cache working (verify with cache hits)
- [ ] Search and filtering functional
- [ ] Pagination working correctly
- [ ] Inventory events published to Kafka
- [ ] Cache invalidated on updates

---

## Session 3.5: Order Service (Days 22-23)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Implement complex business logic
- Handle distributed transactions
- Consume and publish Kafka events
- Implement saga pattern (simplified)

### Tasks
- [ ] Set up Order Service
- [ ] Implement Order and OrderItem entities
- [ ] Build order creation logic
- [ ] Consume `inventory.updated` events
- [ ] Publish `order.created` and `order.completed` events
- [ ] Implement order status tracking
- [ ] Add validation (check inventory before order)

### API Endpoints
```
POST   /api/orders                - Create order
GET    /api/orders                - List user's orders
GET    /api/orders/{id}           - Get order details
PUT    /api/orders/{id}/cancel    - Cancel order
```

### Order Creation Flow
```java
@Service
public class OrderService {
    @Transactional
    public Order createOrder(CreateOrderRequest request) {
        // 1. Validate inventory (call Product Service)
        validateInventory(request.getItems());

        // 2. Create order
        Order order = Order.builder()
            .userId(getCurrentUserId())
            .status(OrderStatus.PENDING)
            .items(request.getItems())
            .totalAmount(calculateTotal(request.getItems()))
            .build();

        orderRepository.save(order);

        // 3. Publish event
        kafkaTemplate.send("order.created", new OrderCreatedEvent(order));

        return order;
    }

    @KafkaListener(topics = "inventory.updated")
    public void handleInventoryUpdate(InventoryUpdatedEvent event) {
        // Update order status if inventory available
    }
}
```

### Validation Checkpoint
- [ ] Order creation working
- [ ] Inventory validated before order
- [ ] Orders linked to correct user
- [ ] Order events published to Kafka
- [ ] Order status updates based on inventory events
- [ ] Total amount calculated correctly

---

## Session 3.6: Notification Service (Days 24-25)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Build event-driven service
- Consume multiple Kafka topics
- Implement notification logic
- Use MongoDB for event logs

### Tasks
- [ ] Set up Notification Service (Node.js or Spring Boot)
- [ ] Configure Kafka consumers for multiple topics
- [ ] Implement email notification (use mock/SendGrid)
- [ ] Store notification logs in MongoDB
- [ ] Add retry logic for failed notifications
- [ ] Implement notification templates

### Event Handlers
```java
@Service
public class NotificationService {
    @KafkaListener(topics = "user.registered")
    public void handleUserRegistered(UserRegisteredEvent event) {
        sendEmail(event.getEmail(), "welcome-template", event);
        saveNotificationLog(event);
    }

    @KafkaListener(topics = "order.created")
    public void handleOrderCreated(OrderCreatedEvent event) {
        sendEmail(event.getUserEmail(), "order-confirmation", event);
        saveNotificationLog(event);
    }

    @KafkaListener(topics = "order.completed")
    public void handleOrderCompleted(OrderCompletedEvent event) {
        sendEmail(event.getUserEmail(), "order-completed", event);
        saveNotificationLog(event);
    }
}
```

### Validation Checkpoint
- [ ] Consumes all event topics
- [ ] Notifications triggered on events
- [ ] Logs stored in MongoDB
- [ ] Retry logic works for failures
- [ ] Email templates rendering correctly

---

## Session 3.7: Distributed Tracing & Monitoring (Day 26)
**Duration**: 4 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Implement distributed tracing
- Set up centralized logging
- Add monitoring and metrics
- Use Zipkin/Jaeger

### Tasks
- [ ] Add Sleuth for distributed tracing
- [ ] Set up Zipkin for trace visualization
- [ ] Configure centralized logging (ELK stack or Loki)
- [ ] Add Micrometer for metrics
- [ ] Set up Prometheus and Grafana
- [ ] Create custom dashboards

### Implementation
```yaml
# docker-compose.monitoring.yml
services:
  zipkin:
    image: openzipkin/zipkin
    ports: ["9411:9411"]

  prometheus:
    image: prom/prometheus
    volumes:
      - ./prometheus.yml:/etc/prometheus/prometheus.yml
    ports: ["9090:9090"]

  grafana:
    image: grafana/grafana
    ports: ["3000:3000"]
```

```java
// Add to each service
@Bean
public RestTemplate restTemplate(RestTemplateBuilder builder) {
    return builder.build();
}
```

### Validation Checkpoint
- [ ] Trace IDs propagate across services
- [ ] Zipkin shows complete request traces
- [ ] Metrics exported to Prometheus
- [ ] Grafana dashboards showing service metrics
- [ ] Can trace a request from gateway through all services

---

## Session 3.8: Testing & Documentation (Day 27)
**Duration**: 4 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Write integration tests for microservices
- Test inter-service communication
- Document APIs with OpenAPI
- Create architecture documentation

### Tasks
- [ ] Add integration tests for each service
- [ ] Test Kafka event publishing/consuming
- [ ] Add contract tests (Spring Cloud Contract)
- [ ] Generate OpenAPI documentation
- [ ] Write comprehensive README
- [ ] Create architecture diagrams
- [ ] Document deployment process

### Testing Example
```java
@SpringBootTest
@Testcontainers
class OrderServiceIntegrationTest {
    @Container
    static PostgreSQLContainer<?> postgres = new PostgreSQLContainer<>("postgres:15");

    @Container
    static KafkaContainer kafka = new KafkaContainer(
        DockerImageName.parse("confluentinc/cp-kafka:7.5.0")
    );

    @Test
    void shouldPublishOrderCreatedEvent() {
        // Test implementation
    }
}
```

### Validation Checkpoint
- [ ] All services have >70% test coverage
- [ ] Integration tests pass
- [ ] OpenAPI docs accessible at /swagger-ui
- [ ] README includes architecture diagram
- [ ] Deployment instructions documented
- [ ] Postman collection created

---

## Session 3.9: Deployment to Cloud (Day 28)
**Duration**: 4 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Deploy to AWS/Azure
- Use managed services (RDS, ElastiCache, MSK)
- Implement infrastructure as code
- Set up production monitoring

### Tasks
- [ ] Choose cloud provider (AWS recommended)
- [ ] Set up Kubernetes cluster (EKS/AKS) or use ECS
- [ ] Create Kubernetes manifests for each service
- [ ] Set up managed PostgreSQL (RDS)
- [ ] Set up managed Redis (ElastiCache)
- [ ] Set up managed Kafka (MSK/Confluent Cloud)
- [ ] Configure load balancer
- [ ] Set up SSL certificates
- [ ] Configure auto-scaling

### Kubernetes Deployment Example
```yaml
# user-service-deployment.yml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: user-service
spec:
  replicas: 2
  selector:
    matchLabels:
      app: user-service
  template:
    metadata:
      labels:
        app: user-service
    spec:
      containers:
      - name: user-service
        image: your-dockerhub/user-service:latest
        ports:
        - containerPort: 8081
        env:
        - name: SPRING_DATASOURCE_URL
          value: jdbc:postgresql://your-rds-endpoint:5432/userdb
---
apiVersion: v1
kind: Service
metadata:
  name: user-service
spec:
  selector:
    app: user-service
  ports:
  - port: 8081
    targetPort: 8081
```

### Validation Checkpoint
- [ ] All services deployed to cloud
- [ ] Services accessible via public URL
- [ ] Auto-scaling configured
- [ ] Monitoring active (CloudWatch/Azure Monitor)
- [ ] Logs centralized
- [ ] SSL configured

---

## 🎓 PROJECT 1 CHECKPOINT (End of Week 4)

### Completed Features
- [ ] 4 microservices running
- [ ] API Gateway routing requests
- [ ] Service discovery with Eureka
- [ ] Event-driven communication with Kafka
- [ ] Redis caching implemented
- [ ] Distributed tracing with Zipkin
- [ ] Deployed to cloud platform

### Portfolio Impact
**This project demonstrates**:
✅ Microservices architecture
✅ Spring Boot expertise
✅ Kafka event streaming
✅ Docker & Kubernetes
✅ Cloud deployment
✅ Distributed systems knowledge
✅ Production-ready practices

### Documentation Checklist
- [ ] README with architecture diagram
- [ ] API documentation (Swagger)
- [ ] Deployment guide
- [ ] Local development setup guide
- [ ] Architecture decision records (ADRs)
- [ ] Performance benchmarks

### Demo Video Script
Record a 5-minute demo showing:
1. System architecture overview
2. User registration flow (trace through all services)
3. Order creation (show Kafka events)
4. Zipkin trace visualization
5. Monitoring dashboards
6. Cloud deployment

---

# WEEK 5-6: PROJECT 2 - Real-Time Event-Driven Analytics Dashboard

## Overview
**Goal**: Build a real-time analytics system with WebSockets, demonstrating event processing and streaming capabilities

**Tech Stack**:
- Backend: Node.js/Express + Go (for high-performance streaming)
- Frontend: React + WebSockets + Chart.js/Recharts
- Database: PostgreSQL + TimescaleDB (time-series data)
- Message Queue: Kafka
- Caching: Redis
- Real-time: Socket.io / Server-Sent Events

**Use Case**: Real-time e-commerce analytics dashboard
- Live sales tracking
- Customer activity monitoring
- Inventory alerts
- Revenue analytics

---

## Session 5.1: Go Basics & Data Ingestion Service (Days 29-30)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Learn Go fundamentals
- Build high-performance API
- Work with Kafka in Go
- Implement concurrent processing

### Tasks
- [ ] Learn Go syntax and basics (goroutines, channels)
- [ ] Study Go HTTP servers
- [ ] Learn Kafka producer in Go (sarama library)
- [ ] Understand Go error handling
- [ ] Study Go project structure

### Hands-on Exercise
**Build Data Ingestion Service in Go**:

Purpose: Accept high-volume events and stream to Kafka

```go
// main.go
package main

import (
    "encoding/json"
    "log"
    "net/http"

    "github.com/Shopify/sarama"
)

type Event struct {
    Type      string                 `json:"type"`
    Timestamp int64                  `json:"timestamp"`
    Data      map[string]interface{} `json:"data"`
}

var kafkaProducer sarama.AsyncProducer

func eventHandler(w http.ResponseWriter, r *http.Request) {
    var event Event
    if err := json.NewDecoder(r.Body).Decode(&event); err != nil {
        http.Error(w, err.Error(), http.StatusBadRequest)
        return
    }

    // Send to Kafka asynchronously
    kafkaProducer.Input() <- &sarama.ProducerMessage{
        Topic: "analytics.events",
        Value: sarama.StringEncoder(toJSON(event)),
    }

    w.WriteHeader(http.StatusAccepted)
}

func main() {
    // Initialize Kafka producer
    config := sarama.NewConfig()
    var err error
    kafkaProducer, err = sarama.NewAsyncProducer([]string{"localhost:9092"}, config)
    if err != nil {
        log.Fatal(err)
    }
    defer kafkaProducer.Close()

    http.HandleFunc("/events", eventHandler)
    log.Println("Server starting on :8080")
    log.Fatal(http.ListenAndServe(":8080", nil))
}
```

### Event Types
```json
{
  "type": "page_view",
  "timestamp": 1678901234000,
  "data": {
    "user_id": "user123",
    "page": "/products/123"
  }
}

{
  "type": "purchase",
  "timestamp": 1678901234000,
  "data": {
    "user_id": "user123",
    "product_id": "prod456",
    "amount": 99.99
  }
}

{
  "type": "inventory_change",
  "timestamp": 1678901234000,
  "data": {
    "product_id": "prod456",
    "quantity": 50
  }
}
```

### Validation Checkpoint
- [ ] Go service accepts HTTP POST requests
- [ ] Events published to Kafka
- [ ] Handles concurrent requests efficiently
- [ ] Error handling works correctly
- [ ] Dockerized with multi-stage build

### Resources
- Go by Example: https://gobyexample.com/
- Go Kafka library: https://github.com/IBM/sarama

---

## Session 5.2: Event Processing Service (Days 31-32)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Implement Kafka Streams processing
- Build aggregations and windowing
- Work with TimescaleDB
- Implement stream processing patterns

### Tasks
- [ ] Learn Kafka Streams/KSQL or Node.js stream processing
- [ ] Set up TimescaleDB for time-series data
- [ ] Implement event aggregations
- [ ] Build time-window calculations
- [ ] Store aggregated metrics in TimescaleDB

### Hands-on Exercise
**Build Event Processing Service (Node.js)**:

Process events from Kafka and aggregate metrics

```javascript
// processor.js
const { Kafka } = require('kafkajs');
const { Pool } = require('pg');

const kafka = new Kafka({ brokers: ['localhost:9092'] });
const consumer = kafka.consumer({ groupId: 'analytics-processor' });

const db = new Pool({
  connectionString: process.env.DATABASE_URL
});

// In-memory aggregations (flushed every minute)
const metrics = {
  pageViews: new Map(),
  revenue: new Map(),
  purchases: 0
};

async function processEvent(event) {
  const { type, timestamp, data } = JSON.parse(event.value);

  switch(type) {
    case 'page_view':
      const count = metrics.pageViews.get(data.page) || 0;
      metrics.pageViews.set(data.page, count + 1);
      break;

    case 'purchase':
      metrics.purchases += 1;
      const revenue = metrics.revenue.get('total') || 0;
      metrics.revenue.set('total', revenue + data.amount);
      break;

    case 'inventory_change':
      await checkInventoryAlert(data);
      break;
  }
}

async function flushMetrics() {
  const timestamp = new Date();

  // Save page views
  for (const [page, count] of metrics.pageViews) {
    await db.query(
      'INSERT INTO page_views_metrics (timestamp, page, count) VALUES ($1, $2, $3)',
      [timestamp, page, count]
    );
  }

  // Save revenue
  await db.query(
    'INSERT INTO revenue_metrics (timestamp, amount) VALUES ($1, $2)',
    [timestamp, metrics.revenue.get('total') || 0]
  );

  // Reset metrics
  metrics.pageViews.clear();
  metrics.revenue.clear();
  metrics.purchases = 0;
}

async function run() {
  await consumer.connect();
  await consumer.subscribe({ topic: 'analytics.events' });

  // Flush metrics every minute
  setInterval(flushMetrics, 60000);

  await consumer.run({
    eachMessage: async ({ message }) => {
      await processEvent(message);
    }
  });
}

run();
```

### Database Schema (TimescaleDB)
```sql
CREATE EXTENSION IF NOT EXISTS timescaledb;

CREATE TABLE page_views_metrics (
  timestamp TIMESTAMPTZ NOT NULL,
  page VARCHAR(255) NOT NULL,
  count INTEGER NOT NULL
);

SELECT create_hypertable('page_views_metrics', 'timestamp');

CREATE TABLE revenue_metrics (
  timestamp TIMESTAMPTZ NOT NULL,
  amount DECIMAL(10, 2) NOT NULL
);

SELECT create_hypertable('revenue_metrics', 'timestamp');

-- Create continuous aggregates for real-time queries
CREATE MATERIALIZED VIEW hourly_revenue
WITH (timescaledb.continuous) AS
  SELECT
    time_bucket('1 hour', timestamp) AS hour,
    SUM(amount) as total_revenue
  FROM revenue_metrics
  GROUP BY hour;
```

### Validation Checkpoint
- [ ] Kafka consumer processing events
- [ ] Metrics aggregated correctly
- [ ] TimescaleDB storing time-series data
- [ ] Continuous aggregates working
- [ ] Can query metrics by time ranges

---

## Session 5.3: Real-Time WebSocket Service (Days 33-34)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Implement WebSocket server
- Build pub/sub with Redis
- Stream data to connected clients
- Handle connection management

### Tasks
- [ ] Set up Socket.io server
- [ ] Configure Redis pub/sub
- [ ] Implement room-based broadcasting
- [ ] Add authentication for WebSocket connections
- [ ] Implement reconnection handling

### Hands-on Exercise
**Build WebSocket Server**:

```javascript
// websocket-server.js
const express = require('express');
const { createServer } = require('http');
const { Server } = require('socket.io');
const { createClient } = require('redis');
const jwt = require('jsonwebtoken');

const app = express();
const httpServer = createServer(app);
const io = new Server(httpServer, {
  cors: { origin: '*' }
});

const redis = createClient();
const subscriber = redis.duplicate();

// Authentication middleware
io.use((socket, next) => {
  const token = socket.handshake.auth.token;
  try {
    const user = jwt.verify(token, process.env.JWT_SECRET);
    socket.userId = user.id;
    next();
  } catch (err) {
    next(new Error('Authentication failed'));
  }
});

io.on('connection', (socket) => {
  console.log(`User connected: ${socket.userId}`);

  // Subscribe to analytics updates
  socket.join('analytics');

  socket.on('disconnect', () => {
    console.log(`User disconnected: ${socket.userId}`);
  });
});

// Subscribe to Redis pub/sub for metrics updates
subscriber.subscribe('metrics.updates', (message) => {
  const data = JSON.parse(message);
  io.to('analytics').emit('metrics:update', data);
});

// REST endpoint to trigger metrics broadcast
app.post('/api/broadcast/metrics', async (req, res) => {
  const metrics = await fetchLatestMetrics();
  await redis.publish('metrics.updates', JSON.stringify(metrics));
  res.json({ status: 'broadcasted' });
});

httpServer.listen(3001, () => {
  console.log('WebSocket server running on port 3001');
});
```

### Validation Checkpoint
- [ ] WebSocket connections authenticated
- [ ] Real-time updates pushed to clients
- [ ] Redis pub/sub working
- [ ] Multiple clients receive updates
- [ ] Reconnection handling works

---

## Session 5.4: Analytics API Service (Day 35)
**Duration**: 4 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Build analytics query API
- Implement caching strategies
- Optimize time-series queries
- Add aggregation endpoints

### Tasks
- [ ] Create Express API for analytics
- [ ] Implement time-range queries
- [ ] Add Redis caching for expensive queries
- [ ] Build aggregation endpoints
- [ ] Add rate limiting

### API Endpoints
```javascript
// analytics-api.js
const express = require('express');
const router = express.Router();

// Get real-time metrics
router.get('/metrics/realtime', async (req, res) => {
  const metrics = await db.query(`
    SELECT * FROM revenue_metrics
    WHERE timestamp > NOW() - INTERVAL '5 minutes'
  `);
  res.json(metrics.rows);
});

// Get hourly revenue for date range
router.get('/metrics/revenue', async (req, res) => {
  const { start, end } = req.query;

  const cacheKey = `revenue:${start}:${end}`;
  const cached = await redis.get(cacheKey);

  if (cached) return res.json(JSON.parse(cached));

  const metrics = await db.query(`
    SELECT hour, total_revenue
    FROM hourly_revenue
    WHERE hour BETWEEN $1 AND $2
    ORDER BY hour
  `, [start, end]);

  await redis.setex(cacheKey, 300, JSON.stringify(metrics.rows));
  res.json(metrics.rows);
});

// Get top pages by views
router.get('/metrics/pages', async (req, res) => {
  const metrics = await db.query(`
    SELECT page, SUM(count) as total_views
    FROM page_views_metrics
    WHERE timestamp > NOW() - INTERVAL '1 hour'
    GROUP BY page
    ORDER BY total_views DESC
    LIMIT 10
  `);
  res.json(metrics.rows);
});

module.exports = router;
```

### Validation Checkpoint
- [ ] All endpoints return correct data
- [ ] Caching working (verify with Redis CLI)
- [ ] Time-range queries optimized
- [ ] Rate limiting preventing abuse

---

## Session 5.5: React Dashboard Frontend (Days 36-37)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Build real-time React dashboard
- Integrate WebSocket updates
- Create interactive charts
- Implement responsive design

### Tasks
- [ ] Set up React app with Vite
- [ ] Integrate Socket.io client
- [ ] Add Chart.js or Recharts
- [ ] Build dashboard components
- [ ] Implement real-time updates
- [ ] Add date range filters

### Dashboard Components

```jsx
// Dashboard.jsx
import { useEffect, useState } from 'react';
import { io } from 'socket.io-client';
import { Line, Bar } from 'react-chartjs-2';

function Dashboard() {
  const [metrics, setMetrics] = useState({
    revenue: [],
    pageViews: [],
    realtimeUsers: 0
  });

  const [socket, setSocket] = useState(null);

  useEffect(() => {
    // Connect to WebSocket
    const newSocket = io('http://localhost:3001', {
      auth: { token: localStorage.getItem('token') }
    });

    newSocket.on('metrics:update', (data) => {
      setMetrics(prev => ({
        ...prev,
        ...data,
        revenue: [...prev.revenue, data.latestRevenue]
      }));
    });

    setSocket(newSocket);

    return () => newSocket.close();
  }, []);

  // Fetch initial data
  useEffect(() => {
    fetch('/api/metrics/revenue?start=2026-03-01&end=2026-03-06')
      .then(res => res.json())
      .then(data => setMetrics(prev => ({ ...prev, revenue: data })));
  }, []);

  return (
    <div className="dashboard">
      <h1>Real-Time Analytics Dashboard</h1>

      <div className="metrics-cards">
        <MetricCard
          title="Real-time Users"
          value={metrics.realtimeUsers}
          live={true}
        />
        <MetricCard
          title="Today's Revenue"
          value={`$${calculateTodayRevenue(metrics.revenue)}`}
        />
      </div>

      <div className="charts">
        <div className="chart">
          <h2>Hourly Revenue</h2>
          <Line data={revenueChartData(metrics.revenue)} />
        </div>

        <div className="chart">
          <h2>Top Pages</h2>
          <Bar data={pageViewsChartData(metrics.pageViews)} />
        </div>
      </div>
    </div>
  );
}
```

### Features to Implement
- [ ] Real-time revenue counter
- [ ] Live activity feed
- [ ] Interactive charts with zoom
- [ ] Date range picker
- [ ] Export data to CSV
- [ ] Dark/light theme toggle

### Validation Checkpoint
- [ ] Dashboard loads with historical data
- [ ] Real-time updates working
- [ ] Charts render correctly
- [ ] Responsive on mobile
- [ ] No memory leaks (check with React DevTools)

---

## Session 5.6: Load Testing & Optimization (Day 38)
**Duration**: 4 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Perform load testing
- Identify bottlenecks
- Optimize performance
- Scale horizontally

### Tasks
- [ ] Set up K6 or Artillery for load testing
- [ ] Test ingestion service throughput
- [ ] Test WebSocket scalability
- [ ] Optimize database queries
- [ ] Implement connection pooling
- [ ] Add horizontal scaling

### Load Testing Script
```javascript
// k6-test.js
import http from 'k6/http';
import { check } from 'k6';

export let options = {
  stages: [
    { duration: '1m', target: 100 },  // Ramp up
    { duration: '3m', target: 100 },  // Steady state
    { duration: '1m', target: 0 },    // Ramp down
  ],
  thresholds: {
    http_req_duration: ['p(95)<500'], // 95% of requests < 500ms
  },
};

export default function () {
  const payload = JSON.stringify({
    type: 'page_view',
    timestamp: Date.now(),
    data: {
      user_id: `user${__VU}`,
      page: `/page${Math.floor(Math.random() * 100)}`
    }
  });

  const res = http.post('http://localhost:8080/events', payload, {
    headers: { 'Content-Type': 'application/json' },
  });

  check(res, {
    'status is 202': (r) => r.status === 202,
  });
}
```

### Performance Targets
- Ingestion: >10,000 events/second
- WebSocket: >1,000 concurrent connections
- API response: <200ms p95
- Dashboard updates: <100ms latency

### Validation Checkpoint
- [ ] Load tests passing
- [ ] Performance targets met
- [ ] System stable under load
- [ ] Identified and fixed bottlenecks
- [ ] Documented optimization results

---

## Session 5.7: Deployment & Monitoring (Day 39)
**Duration**: 4 hours
**Status**: ⬜ Not Started

### Tasks
- [ ] Deploy all services to cloud
- [ ] Set up Kubernetes with autoscaling
- [ ] Configure managed Kafka (MSK/Confluent)
- [ ] Set up managed TimescaleDB
- [ ] Configure WebSocket load balancing
- [ ] Add application monitoring (Datadog/New Relic)
- [ ] Set up alerts for anomalies

### Kubernetes Autoscaling
```yaml
apiVersion: autoscaling/v2
kind: HorizontalPodAutoscaler
metadata:
  name: ingestion-service-hpa
spec:
  scaleTargetRef:
    apiVersion: apps/v1
    kind: Deployment
    name: ingestion-service
  minReplicas: 2
  maxReplicas: 10
  metrics:
  - type: Resource
    resource:
      name: cpu
      target:
        type: Utilization
        averageUtilization: 70
```

### Validation Checkpoint
- [ ] All services deployed
- [ ] Auto-scaling working
- [ ] Monitoring dashboards active
- [ ] Alerts configured
- [ ] Public URL accessible

---

## 🎓 PROJECT 2 CHECKPOINT (End of Week 6)

### Completed Features
- [ ] High-performance Go ingestion service
- [ ] Kafka event streaming
- [ ] TimescaleDB time-series analytics
- [ ] Real-time WebSocket updates
- [ ] Interactive React dashboard
- [ ] Load tested and optimized
- [ ] Cloud deployment

### Portfolio Impact
**This project demonstrates**:
✅ Real-time systems
✅ Event-driven architecture
✅ Go and Node.js expertise
✅ Time-series data handling
✅ WebSocket communication
✅ High-performance optimization
✅ Frontend integration

### New Skills Acquired
- Go programming
- TimescaleDB
- WebSocket real-time communication
- Load testing and optimization
- Stream processing

---

# WEEK 7-8: PROJECT 3 - AI-Powered Full Stack SaaS Application

## Overview
**Goal**: Build an AI-integrated SaaS product demonstrating modern full-stack capabilities with AI features

**Project**: AI-Powered Document Analysis & Chat Platform
- Upload and analyze documents (PDFs, text)
- AI-powered search with semantic understanding
- Chat with your documents (RAG)
- Document summarization
- Multi-user collaboration

**Tech Stack**:
- Frontend: Next.js 14 (App Router) + Tailwind CSS + Shadcn UI
- Backend: Python FastAPI
- AI: OpenAI API (GPT-4) + Embeddings
- Vector DB: Pinecone or Weaviate
- Database: PostgreSQL + Supabase
- Auth: NextAuth.js
- Storage: AWS S3 / Cloudflare R2
- Deployment: Vercel (frontend) + Railway/Fly.io (backend)

---

## Session 7.1: Next.js & Modern Frontend Setup (Days 40-41)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Master Next.js 14 App Router
- Understand Server Components vs Client Components
- Learn server actions
- Implement modern UI with Shadcn

### Tasks
- [ ] Learn Next.js App Router fundamentals
- [ ] Study Server Components and Client Components
- [ ] Understand data fetching patterns
- [ ] Learn Server Actions for mutations
- [ ] Set up Tailwind CSS + Shadcn UI
- [ ] Implement dark mode

### Hands-on Exercise
**Set up Next.js project with authentication**:

```bash
npx create-next-app@latest ai-docs-app --typescript --tailwind --app
cd ai-docs-app
npx shadcn-ui@latest init
npx shadcn-ui@latest add button card input
npm install next-auth
```

```tsx
// app/page.tsx (Server Component)
import { getServerSession } from 'next-auth';
import { authOptions } from '@/lib/auth';
import { redirect } from 'next/navigation';

export default async function HomePage() {
  const session = await getServerSession(authOptions);

  if (!session) {
    redirect('/login');
  }

  // Fetch user's documents (server-side)
  const documents = await fetchUserDocuments(session.user.id);

  return (
    <div className="container mx-auto py-8">
      <h1 className="text-4xl font-bold mb-8">Your Documents</h1>
      <DocumentGrid documents={documents} />
    </div>
  );
}
```

```tsx
// components/DocumentGrid.tsx (Client Component)
'use client';

import { useState } from 'react';
import { Card } from '@/components/ui/card';
import { Button } from '@/components/ui/button';

export function DocumentGrid({ documents }) {
  const [selected, setSelected] = useState(null);

  return (
    <div className="grid grid-cols-3 gap-4">
      {documents.map(doc => (
        <Card key={doc.id} onClick={() => setSelected(doc)}>
          <h3>{doc.name}</h3>
          <p>{doc.summary}</p>
        </Card>
      ))}
    </div>
  );
}
```

### Authentication Setup
```typescript
// lib/auth.ts
import NextAuth from 'next-auth';
import GoogleProvider from 'next-auth/providers/google';
import { PrismaAdapter } from '@next-auth/prisma-adapter';
import { prisma } from './db';

export const authOptions = {
  adapter: PrismaAdapter(prisma),
  providers: [
    GoogleProvider({
      clientId: process.env.GOOGLE_CLIENT_ID!,
      clientSecret: process.env.GOOGLE_CLIENT_SECRET!,
    }),
  ],
  callbacks: {
    session: async ({ session, user }) => {
      session.user.id = user.id;
      return session;
    },
  },
};
```

### Validation Checkpoint
- [ ] Next.js app running
- [ ] Authentication working (Google OAuth)
- [ ] Shadcn UI components integrated
- [ ] Dark mode toggle working
- [ ] Server and Client Components used correctly

### Resources
- Next.js docs: https://nextjs.org/docs
- Shadcn UI: https://ui.shadcn.com/

---

## Session 7.2: Python FastAPI Backend (Days 42-43)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Build FastAPI application
- Implement async endpoints
- Work with Pydantic models
- Set up CORS and authentication
- Integrate with PostgreSQL

### Tasks
- [ ] Learn FastAPI basics
- [ ] Study async/await in Python
- [ ] Learn Pydantic for validation
- [ ] Set up SQLAlchemy with async support
- [ ] Implement JWT authentication
- [ ] Add file upload handling

### Hands-on Exercise
**Build FastAPI backend**:

```python
# main.py
from fastapi import FastAPI, UploadFile, Depends, HTTPException
from fastapi.middleware.cors import CORSMiddleware
from sqlalchemy.ext.asyncio import AsyncSession
from typing import List
import uvicorn

from .database import get_db
from .models import Document, User
from .schemas import DocumentCreate, DocumentResponse
from .auth import get_current_user

app = FastAPI(title="AI Document API")

# CORS middleware
app.add_middleware(
    CORSMiddleware,
    allow_origins=["http://localhost:3000"],
    allow_credentials=True,
    allow_methods=["*"],
    allow_headers=["*"],
)

@app.post("/api/documents/upload", response_model=DocumentResponse)
async def upload_document(
    file: UploadFile,
    db: AsyncSession = Depends(get_db),
    current_user: User = Depends(get_current_user)
):
    """Upload and process a document"""

    # Save file to S3
    file_url = await upload_to_s3(file)

    # Extract text from document
    text_content = await extract_text(file)

    # Create document record
    document = Document(
        user_id=current_user.id,
        name=file.filename,
        file_url=file_url,
        content=text_content,
        status="processing"
    )

    db.add(document)
    await db.commit()

    # Trigger background processing (embeddings)
    await queue_document_processing(document.id)

    return document

@app.get("/api/documents", response_model=List[DocumentResponse])
async def list_documents(
    db: AsyncSession = Depends(get_db),
    current_user: User = Depends(get_current_user)
):
    """List user's documents"""
    documents = await db.execute(
        select(Document).where(Document.user_id == current_user.id)
    )
    return documents.scalars().all()

@app.get("/api/documents/{document_id}", response_model=DocumentResponse)
async def get_document(
    document_id: int,
    db: AsyncSession = Depends(get_db),
    current_user: User = Depends(get_current_user)
):
    """Get document details"""
    document = await db.get(Document, document_id)

    if not document or document.user_id != current_user.id:
        raise HTTPException(status_code=404, detail="Document not found")

    return document

if __name__ == "__main__":
    uvicorn.run(app, host="0.0.0.0", port=8000)
```

```python
# schemas.py
from pydantic import BaseModel, EmailStr
from datetime import datetime
from typing import Optional

class DocumentCreate(BaseModel):
    name: str

class DocumentResponse(BaseModel):
    id: int
    name: str
    file_url: str
    status: str
    created_at: datetime
    summary: Optional[str] = None

    class Config:
        from_attributes = True

class UserCreate(BaseModel):
    email: EmailStr
    password: str
    full_name: str
```

### Validation Checkpoint
- [ ] FastAPI server running
- [ ] File upload endpoint working
- [ ] Authentication protecting endpoints
- [ ] CORS configured correctly
- [ ] PostgreSQL integration working
- [ ] API documented at /docs

---

## Session 7.3: AI Integration - Document Processing (Days 44-45)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Integrate OpenAI API
- Generate embeddings
- Work with vector databases
- Implement semantic search
- Build RAG pipeline

### Tasks
- [ ] Set up OpenAI Python client
- [ ] Learn embeddings generation
- [ ] Set up Pinecone/Weaviate vector DB
- [ ] Implement document chunking
- [ ] Build semantic search
- [ ] Create document summarization

### Hands-on Exercise
**Implement AI document processing**:

```python
# services/ai_service.py
from openai import AsyncOpenAI
import pinecone
from typing import List

client = AsyncOpenAI(api_key=os.getenv("OPENAI_API_KEY"))
pinecone.init(api_key=os.getenv("PINECONE_API_KEY"))
index = pinecone.Index("documents")

async def process_document(document_id: int, content: str):
    """Process document: chunk, embed, and store"""

    # 1. Chunk the document
    chunks = chunk_text(content, chunk_size=1000, overlap=200)

    # 2. Generate embeddings for each chunk
    embeddings = await generate_embeddings(chunks)

    # 3. Store in vector database
    vectors = [
        {
            "id": f"{document_id}_chunk_{i}",
            "values": embedding,
            "metadata": {
                "document_id": document_id,
                "chunk_index": i,
                "text": chunk
            }
        }
        for i, (chunk, embedding) in enumerate(zip(chunks, embeddings))
    ]

    index.upsert(vectors=vectors)

    # 4. Generate summary
    summary = await generate_summary(content)

    return summary

async def generate_embeddings(texts: List[str]) -> List[List[float]]:
    """Generate embeddings using OpenAI"""
    response = await client.embeddings.create(
        model="text-embedding-3-small",
        input=texts
    )
    return [item.embedding for item in response.data]

async def generate_summary(text: str) -> str:
    """Generate document summary using GPT-4"""
    response = await client.chat.completions.create(
        model="gpt-4-turbo-preview",
        messages=[
            {
                "role": "system",
                "content": "You are a helpful assistant that summarizes documents concisely."
            },
            {
                "role": "user",
                "content": f"Summarize this document in 2-3 sentences:\n\n{text[:4000]}"
            }
        ],
        max_tokens=200
    )
    return response.choices[0].message.content

def chunk_text(text: str, chunk_size: int, overlap: int) -> List[str]:
    """Split text into overlapping chunks"""
    chunks = []
    start = 0

    while start < len(text):
        end = start + chunk_size
        chunk = text[start:end]
        chunks.append(chunk)
        start = end - overlap

    return chunks

async def semantic_search(query: str, document_id: int = None, top_k: int = 5):
    """Search for relevant chunks using semantic similarity"""

    # Generate query embedding
    query_embedding = (await generate_embeddings([query]))[0]

    # Search vector database
    filter_dict = {"document_id": document_id} if document_id else None

    results = index.query(
        vector=query_embedding,
        top_k=top_k,
        include_metadata=True,
        filter=filter_dict
    )

    return [
        {
            "text": match.metadata["text"],
            "score": match.score,
            "document_id": match.metadata["document_id"]
        }
        for match in results.matches
    ]
```

### Background Processing
```python
# workers/document_worker.py
import asyncio
from celery import Celery

celery_app = Celery('tasks', broker='redis://localhost:6379/0')

@celery_app.task
def process_document_task(document_id: int):
    """Background task to process document"""
    asyncio.run(process_document_async(document_id))

async def process_document_async(document_id: int):
    async with get_db() as db:
        document = await db.get(Document, document_id)

        # Process document
        summary = await process_document(document_id, document.content)

        # Update document
        document.summary = summary
        document.status = "completed"
        await db.commit()
```

### Validation Checkpoint
- [ ] Document processing pipeline working
- [ ] Embeddings stored in vector database
- [ ] Semantic search returning relevant results
- [ ] Summarization working
- [ ] Background processing with Celery

---

## Session 7.4: AI Chat Interface (Days 46-47)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Learning Objectives
- Build RAG (Retrieval Augmented Generation)
- Implement streaming responses
- Create chat interface
- Handle conversation history

### Tasks
- [ ] Implement RAG pipeline
- [ ] Add streaming chat endpoint
- [ ] Build chat UI in Next.js
- [ ] Implement conversation history
- [ ] Add typing indicators

### RAG Implementation
```python
# services/chat_service.py
from openai import AsyncOpenAI
from typing import AsyncIterator

client = AsyncOpenAI()

async def chat_with_document(
    document_id: int,
    query: str,
    conversation_history: List[dict]
) -> AsyncIterator[str]:
    """RAG-based chat with document"""

    # 1. Retrieve relevant chunks
    relevant_chunks = await semantic_search(
        query=query,
        document_id=document_id,
        top_k=3
    )

    # 2. Build context from chunks
    context = "\n\n".join([chunk["text"] for chunk in relevant_chunks])

    # 3. Build prompt with context
    system_prompt = f"""You are a helpful assistant that answers questions about documents.
    Use the following context to answer the user's question. If the answer is not in the context, say so.

    Context:
    {context}
    """

    messages = [
        {"role": "system", "content": system_prompt},
        *conversation_history,
        {"role": "user", "content": query}
    ]

    # 4. Stream response from GPT-4
    stream = await client.chat.completions.create(
        model="gpt-4-turbo-preview",
        messages=messages,
        stream=True,
        temperature=0.7
    )

    async for chunk in stream:
        if chunk.choices[0].delta.content:
            yield chunk.choices[0].delta.content

# API endpoint
@app.post("/api/chat/{document_id}/stream")
async def chat_stream(
    document_id: int,
    request: ChatRequest,
    current_user: User = Depends(get_current_user)
):
    """Streaming chat endpoint"""

    async def generate():
        async for chunk in chat_with_document(
            document_id=document_id,
            query=request.message,
            conversation_history=request.history
        ):
            yield f"data: {json.dumps({'text': chunk})}\n\n"

    return StreamingResponse(generate(), media_type="text/event-stream")
```

### Chat UI Component
```tsx
// components/ChatInterface.tsx
'use client';

import { useState, useRef, useEffect } from 'react';
import { Button } from '@/components/ui/button';
import { Input } from '@/components/ui/input';

export function ChatInterface({ documentId }: { documentId: number }) {
  const [messages, setMessages] = useState<Message[]>([]);
  const [input, setInput] = useState('');
  const [isLoading, setIsLoading] = useState(false);
  const messagesEndRef = useRef<HTMLDivElement>(null);

  const sendMessage = async () => {
    if (!input.trim()) return;

    const userMessage = { role: 'user', content: input };
    setMessages(prev => [...prev, userMessage]);
    setInput('');
    setIsLoading(true);

    // Create assistant message
    const assistantMessage = { role: 'assistant', content: '' };
    setMessages(prev => [...prev, assistantMessage]);

    // Stream response
    const response = await fetch(`/api/chat/${documentId}/stream`, {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({
        message: input,
        history: messages
      })
    });

    const reader = response.body?.getReader();
    const decoder = new TextDecoder();

    while (true) {
      const { done, value } = await reader!.read();
      if (done) break;

      const chunk = decoder.decode(value);
      const lines = chunk.split('\n');

      for (const line of lines) {
        if (line.startsWith('data: ')) {
          const data = JSON.parse(line.slice(6));
          setMessages(prev => {
            const updated = [...prev];
            updated[updated.length - 1].content += data.text;
            return updated;
          });
        }
      }
    }

    setIsLoading(false);
  };

  // Auto-scroll to bottom
  useEffect(() => {
    messagesEndRef.current?.scrollIntoView({ behavior: 'smooth' });
  }, [messages]);

  return (
    <div className="flex flex-col h-full">
      <div className="flex-1 overflow-y-auto p-4 space-y-4">
        {messages.map((msg, i) => (
          <div
            key={i}
            className={`flex ${msg.role === 'user' ? 'justify-end' : 'justify-start'}`}
          >
            <div
              className={`max-w-[80%] rounded-lg p-3 ${
                msg.role === 'user'
                  ? 'bg-blue-500 text-white'
                  : 'bg-gray-200 dark:bg-gray-700'
              }`}
            >
              {msg.content}
            </div>
          </div>
        ))}
        {isLoading && (
          <div className="flex justify-start">
            <div className="bg-gray-200 dark:bg-gray-700 rounded-lg p-3">
              <div className="flex space-x-2">
                <div className="w-2 h-2 bg-gray-500 rounded-full animate-bounce" />
                <div className="w-2 h-2 bg-gray-500 rounded-full animate-bounce delay-100" />
                <div className="w-2 h-2 bg-gray-500 rounded-full animate-bounce delay-200" />
              </div>
            </div>
          </div>
        )}
        <div ref={messagesEndRef} />
      </div>

      <div className="border-t p-4">
        <div className="flex space-x-2">
          <Input
            value={input}
            onChange={(e) => setInput(e.target.value)}
            onKeyPress={(e) => e.key === 'Enter' && sendMessage()}
            placeholder="Ask a question about this document..."
            disabled={isLoading}
          />
          <Button onClick={sendMessage} disabled={isLoading}>
            Send
          </Button>
        </div>
      </div>
    </div>
  );
}
```

### Validation Checkpoint
- [ ] RAG pipeline working
- [ ] Streaming responses working
- [ ] Chat UI functional
- [ ] Conversation history maintained
- [ ] Citations showing relevant chunks

---

## Session 7.5: Additional AI Features (Day 48)
**Duration**: 4 hours
**Status**: ⬜ Not Started

### Tasks
- [ ] Add bulk document upload
- [ ] Implement document comparison
- [ ] Add export functionality (PDF summaries)
- [ ] Build admin dashboard
- [ ] Add usage analytics

### Quick Features
```python
# Additional endpoints
@app.post("/api/documents/compare")
async def compare_documents(doc_ids: List[int]):
    """Compare multiple documents"""
    # Implementation

@app.get("/api/documents/{doc_id}/export")
async def export_summary(doc_id: int):
    """Export document summary as PDF"""
    # Implementation

@app.get("/api/analytics")
async def get_analytics(current_user: User = Depends(get_current_user)):
    """Get usage analytics"""
    return {
        "total_documents": await count_documents(current_user.id),
        "total_chats": await count_chats(current_user.id),
        "tokens_used": await get_token_usage(current_user.id)
    }
```

---

## Session 7.6: Testing & Deployment (Days 49-50)
**Duration**: 6 hours
**Status**: ⬜ Not Started

### Tasks
- [ ] Add comprehensive tests (pytest for backend)
- [ ] Add E2E tests (Playwright for frontend)
- [ ] Deploy frontend to Vercel
- [ ] Deploy backend to Railway/Fly.io
- [ ] Set up production database (Supabase)
- [ ] Configure production OpenAI keys
- [ ] Set up monitoring (Sentry)

### Deployment Commands
```bash
# Deploy frontend
cd frontend
vercel --prod

# Deploy backend
cd backend
railway up

# Or with Docker
docker build -t ai-docs-api .
docker push your-registry/ai-docs-api
```

### Environment Variables
```bash
# Backend (.env)
DATABASE_URL=postgresql://...
OPENAI_API_KEY=sk-...
PINECONE_API_KEY=...
AWS_ACCESS_KEY_ID=...
AWS_SECRET_ACCESS_KEY=...
JWT_SECRET=...

# Frontend (.env.local)
NEXTAUTH_URL=https://your-domain.com
NEXTAUTH_SECRET=...
NEXT_PUBLIC_API_URL=https://api.your-domain.com
GOOGLE_CLIENT_ID=...
GOOGLE_CLIENT_SECRET=...
```

### Validation Checkpoint
- [ ] All tests passing
- [ ] Frontend deployed to Vercel
- [ ] Backend deployed and accessible
- [ ] Database migrations run
- [ ] SSL certificates active
- [ ] Monitoring configured

---

## 🎓 PROJECT 3 CHECKPOINT (End of Week 8)

### Completed Features
- [ ] Next.js 14 full-stack app
- [ ] Google OAuth authentication
- [ ] Document upload and processing
- [ ] AI-powered summarization
- [ ] Semantic search
- [ ] RAG-based chat interface
- [ ] Streaming responses
- [ ] Production deployment

### Portfolio Impact
**This project demonstrates**:
✅ Modern full-stack development (Next.js)
✅ AI/ML integration (OpenAI, embeddings, RAG)
✅ Python backend (FastAPI)
✅ Vector databases
✅ Real-time streaming
✅ Production SaaS architecture
✅ Modern UI/UX

### New Skills Acquired
- Next.js 14 App Router
- Python FastAPI
- OpenAI API integration
- Vector databases (Pinecone)
- RAG implementation
- Streaming responses
- Modern React patterns

---

# FINAL WEEK CHECKLIST (Days 51-60)

## Polish & Portfolio Presentation

### Days 51-52: Documentation Week
**Tasks**:
- [ ] Write comprehensive READMEs for all 3 projects
- [ ] Create architecture diagrams (use Excalidraw/draw.io)
- [ ] Document API endpoints with examples
- [ ] Write blog posts about each project
- [ ] Create project demos (GIFs/videos)

### Days 53-54: GitHub Portfolio Optimization
**Tasks**:
- [ ] Clean up commit history
- [ ] Add GitHub Actions badges
- [ ] Create GitHub profile README
- [ ] Pin best projects to profile
- [ ] Add project screenshots
- [ ] Write meaningful project descriptions
- [ ] Add tags/topics to repos

### Days 55-56: Resume & LinkedIn
**Tasks**:
- [ ] Update resume with new projects
- [ ] Add technical skills section
- [ ] Quantify achievements (e.g., "Built system handling 10K events/sec")
- [ ] Update LinkedIn with project details
- [ ] Write LinkedIn posts about learning journey
- [ ] Connect with recruiters and engineers

### Days 57-58: Practice Interviews
**Tasks**:
- [ ] Review system design fundamentals
- [ ] Practice explaining your projects (STAR method)
- [ ] Prepare for behavioral questions
- [ ] Practice live coding (LeetCode medium problems)
- [ ] Mock interviews with peers or Pramp

### Days 59-60: Job Applications
**Tasks**:
- [ ] Apply to 20+ positions
- [ ] Customize resume for each application
- [ ] Write compelling cover letters highlighting projects
- [ ] Reach out to referrals on LinkedIn
- [ ] Follow up on applications

---

# 📈 Progress Tracking

## Weekly Self-Assessment

| Week | Core Focus | Confidence (1-10) | Issues Faced | Time Spent |
|------|------------|-------------------|--------------|------------|
| 1 | Foundations | | | |
| 2 | DevOps & Testing | | | |
| 3-4 | Microservices | | | |
| 5-6 | Real-time Systems | | | |
| 7-8 | AI Integration | | | |

## Skills Mastery Checklist

### Backend
- [ ] Spring Boot (advanced)
- [ ] Node.js/Express
- [ ] Python FastAPI
- [ ] Go (basics)
- [ ] REST API design
- [ ] GraphQL (bonus)

### Databases
- [ ] PostgreSQL (optimization)
- [ ] MongoDB
- [ ] Redis (caching)
- [ ] TimescaleDB
- [ ] Pinecone/Weaviate

### Infrastructure
- [ ] Docker
- [ ] Kubernetes
- [ ] AWS/Azure
- [ ] CI/CD pipelines
- [ ] Monitoring & logging

### Architecture
- [ ] Microservices
- [ ] Event-driven systems
- [ ] CQRS pattern
- [ ] API Gateway pattern
- [ ] Service mesh concepts

### AI/ML
- [ ] OpenAI API
- [ ] Embeddings
- [ ] RAG implementation
- [ ] Vector databases
- [ ] Prompt engineering

### Frontend
- [ ] React (hooks, context)
- [ ] Next.js 14
- [ ] WebSockets
- [ ] Real-time updates
- [ ] Modern UI libraries

---

# 💡 Tips for Success

## Time Management
1. **Stick to schedule**: 4-5 hours daily, no excuses
2. **Use Pomodoro**: 25min focused work, 5min break
3. **Weekend catch-up**: Use weekends to review or catch up
4. **Evening reviews**: Spend 15min reviewing what you learned

## Learning Strategies
1. **Build, don't just watch**: Code along with tutorials
2. **Debug actively**: Don't skip errors, understand them
3. **Document as you go**: Write notes in project READMEs
4. **Teach to learn**: Explain concepts to rubber duck/friend
5. **Ask for help**: Use ChatGPT, StackOverflow, Discord communities

## Common Pitfalls to Avoid
1. ❌ Tutorial hell - watching without building
2. ❌ Perfectionism - done is better than perfect
3. ❌ Scope creep - stick to plan, no extra features yet
4. ❌ Skipping tests - write tests as you build
5. ❌ Poor commits - write meaningful commit messages
6. ❌ No documentation - README is part of the project

## Staying Motivated
1. Share progress on Twitter/LinkedIn
2. Join dev communities (Discord, Reddit)
3. Track your progress visually (GitHub contributions)
4. Celebrate small wins
5. Remember why you started

---

# 🎯 Success Metrics

## By End of 2 Months You Will Have:

### Portfolio
✅ 3 production-ready projects on GitHub
✅ 100+ commits across projects
✅ 10+ READMEs and documentation
✅ Live deployed applications

### Technical Skills
✅ 5+ programming languages/frameworks
✅ Microservices architecture expertise
✅ Real-time systems experience
✅ AI integration capabilities
✅ Cloud deployment knowledge

### Professional Presence
✅ Updated resume with quantified achievements
✅ Optimized LinkedIn profile
✅ Technical blog posts
✅ GitHub profile showcasing work

### Job Readiness
✅ Can explain system design decisions
✅ Can discuss trade-offs in architecture
✅ Can demonstrate projects confidently
✅ Ready for technical interviews

---

# 📚 Resource Library

## Documentation
- Spring Boot: https://spring.io/projects/spring-boot
- Node.js: https://nodejs.org/docs
- React: https://react.dev
- Next.js: https://nextjs.org/docs
- FastAPI: https://fastapi.tiangolo.com
- Go: https://go.dev/doc

## Learning Platforms
- FreeCodeCamp (YouTube)
- Traversy Media (YouTube)
- Web Dev Simplified (YouTube)
- Fireship (YouTube)
- Official docs (always start here)

## Communities
- r/webdev (Reddit)
- r/cscareerquestions (Reddit)
- Dev.to
- Hashnode
- Twitter #100DaysOfCode

## Tools
- VS Code / IntelliJ IDEA
- Postman / Insomnia
- Docker Desktop
- DBeaver (database client)
- draw.io (diagrams)

---

# 🚀 Next Steps After 2 Months

## Continue Learning
1. Advanced Kubernetes (Service mesh, Istio)
2. Advanced AI (fine-tuning, agents)
3. Mobile development (React Native)
4. DevOps deep dive (Terraform, Ansible)

## Contribute to Open Source
1. Find projects using your tech stack
2. Start with "good first issue" labels
3. Build credibility in community

## Build Side Projects
1. Monetize your learning (SaaS products)
2. Freelance with new skills
3. Contribute to open source

## Job Search
1. Apply to 10+ companies per week
2. Network actively
3. Leverage your projects in interviews
4. Consider contract/freelance first

---

**Good luck! Remember: Consistency beats intensity. Show up every day, and you'll be amazed at what you can build in 2 months.**

**Questions or stuck? That's normal. Use ChatGPT, Claude, or dev communities. Every senior engineer was once where you are.**

**Let's build! 🚀**
