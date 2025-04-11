# Development Approach

## Task Definition

1. Tasks are taken from the tracker and only from it. If a task arrives via email or messenger - it must be transferred to the tracker
2. If a task is not in the tracker, it does not exist. **[In rare cases]** a task can be described after the fact, but it must be described and documented
3. A task **[must]** have a quality description - the purpose of the task, input values, the process, and what should be the output. If there is no description - the task is sent for reformulation.
4. Tasks that require frontend development must have a design. If there is no design - the task is sent for reformulation
5. A task must have a start date and completion date (planned and actual)
6. The duration of a task should be no more than 1 day; if the task is longer, it should be broken down into smaller tasks
7. A task must have a priority. Tasks should be performed according to priority
8. All tasks must be described in the tracker in a uniform format
9. It is forbidden to create meta-tasks without clear completion criteria
10. Each task must have a unique identifier

## Task Description Format

1. **Title** - brief but informative task name (no more than 80 characters)
2. **Description** - detailed description of the task, including:
   - Business justification (why it's important)
   - Technical context (what needs to be known for implementation)
   - Expected result (what should be produced)
3. **Design link** - link to mockups in Figma/Zeplin/etc. (in case of frontend tasks)
4. **Input parameters and conditions** - preconditions for task execution:
   - Initial system state
   - Required user permissions/rights
   - Data sources
   - Preliminary conditions (for example, the user must be logged in, service connected, etc.)
5. **Output parameters** - what should change as a result:
   - Final system state
   - Changes in the database
   - Changes in the user interface
   - API responses
6. **Positive scenarios** - description of system behavior when the user performs all actions correctly
7. **Negative scenarios** - description of system behavior with incorrect user actions or during failures:
   - Reaction to incorrect input data
   - Exception handling
   - Error messages
8. **Data validation criteria** - rules for checking the correctness of input data:
   - Input format requirements
   - Value constraints
   - Validation rules (for example, password complexity, allowed characters in login, etc.)
9. **Interface texts** - texts for interface elements in all supported languages:
   - Button texts
   - Notifications
   - Error messages
   - Email notification texts
10. **Accessibility requirements (a11y)** - requirements for ensuring interface accessibility:
    - Contrast
    - Scalability
    - Screen reader support
    - Keyboard control
11. **Role access** - for which user roles the functionality should be available
12. **Acceptance criteria** - clear and measurable criteria by which it can be determined that the task is completed
13. **Definition of Done** - list of requirements for the quality and completeness of the task
14. **Complexity assessment** - in story points (1, 2, 3, 5, 8, 13) - Fibonacci sequence
15. **Priority** - according to the accepted prioritization system
16. **Dependencies** - which tasks the implementation depends on and which tasks depend on the current one
17. **Tags/labels** - for categorization and filtering
18. **Executor** - who is responsible for task execution
19. **Auditor** - who checks task execution
20. **Deadlines** - deadline and estimated execution time

## Bug Description Format

1. **Title** - brief but informative name of the problem (no more than 80 characters)
2. **Date and time of the event** - when the problem was discovered
3. **Environment information**:
   - Device type and model (for mobile applications)
   - Browser and its version (for web applications)
   - Operating system version and type
   - Application version
   - Network environment (WiFi/mobile network/VPN)
4. **Reproduction steps** - sequential actions to reproduce the problem:
   - Initial state (for example, "User is authorized")
   - Numbered steps to reproduce the bug
   - Parameters used during reproduction (for example, specific field values)
5. **Actual result** - what happened in the end:
   - Text description of the problem
   - Screenshots or videos demonstrating the problem
   - Logs or error messages
6. **Expected result** - how the system should have worked correctly
7. **Reproducibility** - how consistently the problem reproduces:
   - Always (100%)
   - Often (about 75%)
   - Sometimes (about 50%)
   - Rarely (less than 25%)
8. **Scale of the problem**:
   - On how many devices it repeats
   - How many users it affects
   - Whether there is a workaround
9. **Severity**:
   - Critical - blocks system operation
   - High - seriously disrupts functionality
   - Medium - makes usage difficult
   - Low - minor issues
10. **Priority** - how urgently a fix is required
11. **Additional materials**:
    - HAR files for web applications
    - Memory dump
    - Session/request identifiers
    - Username/account (if necessary)

## Task Execution (Daily Plan)

1. Before starting work, read the task, mark your participation in the tracker
2. Clarify - is there anything preventing the work, if something is hindering - request help or information from colleagues
3. Start a new feature in git flow
4. Take a STANDARD solution-library-platform from those used in the company (see in the corresponding section), if not found - agree with the senior technical leader on using another solution
5. If there is ready-tested code (check for availability in the code library) - use it
6. Check - whether any of the developers on the project has written code that can be reused. Avoid duplicating functionality.
7. Write tests for the code and run them
8. Test the implemented task
9. Test the application functions that may be affected by the work done
10. Document the work
11. Check for performance (if it's frontend, use [Lighthouse](https://developers.google.com/web/tools/lighthouse))
12. (if applicable) Check for i18n compliance
13. (if applicable) Check for A11y compliance
14. Run automated code check - linter, profiler, etc., fix code if necessary
15. Mark the task as completed in the tracker
16. Remove unnecessary and test data from the code, ensure there are no hardcoded configuration values, keys, and passwords in the code
17. Upload code to GitHub using [pull request (PR)](https://rustycrate.ru/%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%B0/2016/03/07/contributing.html) mechanisms, assign the technical leader responsible for auditing the written code
18. Deploy completed tasks to test and staging zones (if auto-deploy is not configured) as agreed with the technical leader
19. At the end of the day, even if tasks are not completed - upload all code to GitHub with a wip (work in progress) label
20. Remove unnecessary branches
21. If implementation deadlines did not match expectations - note this and indicate the reason
22. Report on completed work, encountered problems, and additional requirements to the project manager and technical leader at the end of the working day for all completed tasks

## Additional Provisions

1. Code that can be used on other projects should be saved in the archive/library of source code. Solutions to non-standard problems found on forums and blogs (with a link to the source) should also be saved there
2. If part of the project code can be in demand and refined in other projects (including by developers from other companies), then an open source project should be released on the company account and the senior technical leader should be contacted to promote the repository
3. If some tasks are regularly repeated, it makes sense to use automation tools, for example - make a template
4. Commits in git should comply with the style [https://www.conventionalcommits.org](https://www.conventionalcommits.org) Before starting the project, a list of all available scopes should be compiled
5. For each release, a Changelog should be written, conforming to the standard [https://keepachangelog.com/](https://keepachangelog.com/)

## Release Policy

The recommended approach is frequent releases with small functionality. Each release before being deployed to the production server must be tested on the staging server to ensure that there are no critical issues. Release frequency - 1 time per day, that is, on the first day they are tested on the staging server, on the second day the release is published on the production server. Deployment happens using the release train approach (<https://habr.com/ru/companies/dododev/articles/706158/>). In the future, the duration of the release cycle may be increased, depending on the needs of the team and product growth.
