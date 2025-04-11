# Security

## General Security Principles

1. **Security by Design** - security is considered at all development stages
2. **Defense in Depth** - multi-layered protection
3. **Least Privilege** - minimization of access privileges
4. **Fail Secure** - secure behavior during failures
5. **Keep It Simple** - simplicity as a security principle

## Security Process

1. Requirements - defining security requirements at the planning stage
2. Threat modeling - identifying potential attack vectors
3. Secure development - following secure coding practices
4. Code checking - code analysis for vulnerabilities
5. Security testing - regular penetration testing
6. Monitoring - detection and response to incidents

## Web Application Security Requirements

1. Authentication and authorization

   - Multi-factor authentication for critical operations
   - OAuth 2.0 and OpenID Connect for federated authentication
   - RBAC (Role-Based Access Control) for access management
   - System log of all actions with elevated privileges

2. Protection against main vulnerabilities

   - XSS (Cross-Site Scripting) - validation and output escaping
   - CSRF (Cross-Site Request Forgery) - tokens and Origin verification
   - SQL Injection - using parameterized queries
   - SSRF (Server-Side Request Forgery) - URL validation and whitelisting
   - Path Traversal - normalization and path validation
   - Command Injection - avoiding command execution from user input

3. Data protection

   - Encryption of data at rest
   - Encryption of data in transit
   - Secure password storage (bcrypt, Argon2)
   - Masking sensitive data in logs
   - Data storage and deletion policy

4. Infrastructure security
   - TLS 1.3 for all communications
   - HTTP Security Headers (CSP, HSTS, X-Content-Type-Options)
   - Using WAF (Web Application Firewall)
   - Regular updating of dependencies
   - Monitoring and logging security events

## Security Development Lifecycle (SDL)

1. Training - regular training of developers in security basics
2. Planning - defining security requirements
3. Threat modeling - analysis of potential threats
4. Development - following secure coding practices
5. Verification - automated and manual code analysis
6. Testing - penetration testing
7. Release - checking readiness for release
8. Response - incident response plan

## Security Checklist Before Release

1. Code

   - Code analysis for vulnerabilities conducted
   - All dependencies checked for known vulnerabilities
   - Secrets and keys not stored in the code

2. Data

   - All sensitive data encrypted
   - Secure password storage implemented
   - Proper logging without sensitive data established

3. Configuration

   - No default accounts and passwords
   - Necessary HTTP Security Headers configured
   - Latest TLS versions used

4. Infrastructure
   - Security monitoring configured
   - Backup configured
   - Incident response plan developed
