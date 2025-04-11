# API

## Documenting API

1. Documentation standard

   - OpenAPI (Swagger) for REST API
   - GraphQL Schema for GraphQL API
   - gRPC Protocol Buffers for gRPC API

2. Mandatory elements of API documentation

   - General API description and its purpose
   - Authentication and authorization
   - Data models and their description
   - Endpoints and methods with parameters and responses
   - Error codes and their handling
   - Limitations and rate limits
   - Versioning and compatibility

3. API documentation process
   - API documentation is created before development begins
   - Documentation testing as part of API testing
   - Automatic generation of documentation from code
   - Regular verification of documentation relevance

## Updating Documentation

1. Documentation is updated synchronously with code changes
2. PR should include necessary changes in documentation
3. Code review includes checking the relevance of documentation
4. Responsibility for documentation relevance lies with the entire team

## Documentation Quality Metrics

1. Completeness - coverage of all aspects of the system
2. Relevance - correspondence to the current version of the system
3. Clarity - readability and accessibility of presentation
4. User feedback - evaluation of documentation by users

## API Design

### API Design Principles

1. API First - designing API before starting development
2. Consistency - uniformity of interfaces
3. Developer Experience - ease of use for developers
4. Evolvability - possibility of development without breaking compatibility
5. Security by Design - security as a core principle

### REST API Standards

1. Resource naming

   - Using plural nouns (users, posts)
   - Resource hierarchy through nesting (/users/{id}/posts)
   - Using kebab-case for URL paths
   - Not using verbs in URLs (except for special actions)

2. HTTP methods

   - GET - retrieving resources
   - POST - creating resources
   - PUT - complete resource update
   - PATCH - partial resource update
   - DELETE - resource deletion

3. HTTP status codes

   - 2xx - successful execution
   - 3xx - redirection
   - 4xx - client error
   - 5xx - server error
   - Proper use of codes (201 for creation, 204 for deletion)

4. Query parameters

   - Filtering: ?filter\[field\]=value
   - Sorting: ?sort=field,-created_at
   - Pagination: ?page=2&per_page=25
   - Field selection: ?fields=name,email,created_at
   - Data expansion: ?include=author,comments

5. Response format

   - Standard response structure
   - Unified error format
   - Using snake_case for JSON fields
   - Including metadata (pagination, total count)

6. Versioning
   - Semantic versioning
   - Version in URL (/api/v1/users)
   - Backward compatibility within the main version

### GraphQL API Standards

1. Schema structure

   - Clear division into Query, Mutation, and Subscription
   - Using fragments for repeating fields
   - Combining related operations in one request

2. Naming

   - camelCase for fields and arguments
   - PascalCase for types
   - Descriptive operation names

3. Error handling

   - Standard error format
   - Informative error messages
   - Using extensions for error metadata

4. Security

   - Limiting query complexity
   - Rate limits by complexity, not by number of requests
   - Input data validation

5. Optimization
   - Using DataLoader to solve N+1 problem
   - Caching results
   - Pagination for large data sets

## API Security

1. Authentication

   - OAuth 2.0 and OpenID Connect
   - JWT tokens with limited lifetime
   - Token revocation when compromised

2. Authorization

   - RBAC (Role-Based Access Control)
   - Detailed permissions at the resource level
   - Centralized access policy management
   - Deny-first approach

3. Attack protection

   - Rate limits and DoS protection
   - Validation and sanitization of all input data
   - CORS (Cross-Origin Resource Sharing) settings
   - Content Security Policy

4. Transport security
   - Using only HTTPS
   - HSTS (HTTP Strict Transport Security)
   - Modern TLS versions (minimum TLS 1.2)

## API Testing

1. Automated testing

   - Unit tests for business logic
   - Integration tests for API
   - Load testing
   - Fuzzing for vulnerability detection

2. Testing tools

   - Postman/Newman collections for functional testing
   - Swagger UI for interactive testing
   - JMeter/Locust for load testing

3. API monitoring
   - Logging all requests and responses
   - Tracking response time
   - Monitoring errors and exceptions
   - Alerts for abnormal behavior

## Documenting API

1. Automatic documentation generation

   - OpenAPI/Swagger for REST API
   - GraphQL Introspection for GraphQL API
   - Postman Collections for demonstrating examples

2. Documentation content

   - General API description and its purpose
   - Authentication and authorization
   - Detailed description of all endpoints
   - Examples of requests and responses
   - Error handling
   - Limitations and rate limits

3. Interactive documentation
   - Ability to execute requests directly from documentation
   - Sandbox for API testing
   - Client code generation for different languages
