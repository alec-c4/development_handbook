# Technical Debt Management

## Definition of Technical Debt

Technical debt is a metaphor reflecting accumulated technical compromises made during development that can slow down future development. Technical debt includes:

- Architectural debt - architectural issues that make system expansion difficult
- Code debt - low code quality, duplication, violation of SOLID principles
- Test debt - insufficient test coverage or low test quality
- Documentation debt - absence or outdated documentation
- Infrastructure debt - outdated technologies, libraries, tools

## Identifying Technical Debt

- Regular audit - quarterly audit of the codebase and infrastructure
- Code quality metrics - automated monitoring of code quality through static analysis
- Technical radar - periodic assessment of technologies and tools used
- Retrospectives - recording technical problems identified during development

## Accounting for Technical Debt

1. Technical debt is recorded in the task tracker with the tech-debt tag

2. For each element of technical debt, the following is indicated:
   - Problem description
   - Impact on development (speed, reliability, scalability)
   - Assessment of elimination costs
   - Risk assessment

## Prioritizing Technical Debt

For technical debt prioritization, the formula is used:

**Priority = Impact × Risk / Cost**

where:

- **Impact** - assessment of development slowdown on a scale from 1 to 10

- **Risk** - probability of problems on a scale from 1 to 10

- **Cost** - assessment of labor costs for elimination in person-days

## Managing Technical Debt

- At least 20% of each sprint's time should be allocated to working with technical debt, for example, every Friday there is a feature freeze and the entire day is devoted to closing technical debt
- Critical technical debt is eliminated first
- When developing new functions, it is forbidden to increase technical debt
- When changing code, the developer must follow the "scout rule" - leave the code in a better state than it was found

## Preventing Technical Debt

- **Clear code standards** - compliance with standards and guidelines
- **Code review** - mandatory code review by other developers
- **Automated checks** - linters, static analysis, auto-tests
- **Refactoring budget** - allocating time for regular refactoring
- **Architectural committee** - periodic reviews and discussion of architecture
