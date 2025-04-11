# Project Management

## Development Management Methodology - Agile

The development process is built on the agile approach and Scrum framework. The work should follow the Agile Manifesto

1. Individuals and interactions over processes and tools
2. Working software over comprehensive documentation
3. Customer collaboration over contract negotiation
4. Responding to change over following a plan

That is, while there is value in the items on the right, we value the items on the left more.

**Fundamental Principles of the Agile Manifesto**

1. Our highest priority is to satisfy the customer through early and continuous delivery of valuable software.
2. Welcome changing requirements, even late in development. Agile processes harness change for the customer's competitive advantage.
3. Deliver working software frequently, from a couple of weeks to a couple of months, with a preference to the shorter timescale.
4. Business people and developers must work together daily throughout the project.
5. Build projects around motivated individuals. Give them the environment and support they need, and trust them to get the job done.
6. The most efficient and effective method of conveying information to and within a development team is face-to-face conversation.
7. Working software is the primary measure of progress.
8. Agile processes promote sustainable development. The sponsors, developers, and users should be able to maintain a constant pace indefinitely.
9. Continuous attention to technical excellence and good design enhances agility.
10. Simplicity--the art of maximizing the amount of work not done--is essential.
11. The best architectures, requirements, and designs emerge from self-organizing teams.
12. At regular intervals, the team reflects on how to become more effective, then tunes and adjusts its behavior accordingly.

## Task Prioritization

### RICE Model

For task prioritization, the RICE model is used:

- **Reach** - the number of users or transactions that the task will affect (estimated numerically)

- **Impact** - how significant the improvement is for the affected users:

  > 0.25 - Minimal impact
  > 0.5 - Low impact
  > 1.0 - Medium impact
  > 2.0 - High impact
  > 3.0 - Massive impact

- **Confidence** - how confident we are in the reach and impact estimates:

  > 50% - Low confidence (assumption)
  > 80% - Medium confidence (based on indirect data)
  > 100% - High confidence (based on direct data)

- **Effort** - implementation costs in person-weeks

Calculation formula: **RICE = (Reach × Impact × Confidence) / Effort**

The higher the final RICE value, the higher the priority of the task.

### Weighted Shortest Job First (WSJF)

Alternatively, the WSJF model can be used for task prioritization:

- **Business Value** - assessment on a scale of 1-10

- **Time Criticality** - assessment on a scale of 1-10

- **Risk Reduction / Opportunity Enablement** - assessment on a scale of 1-10

- **Job Size** - estimation in story points or person-days

Calculation formula: **WSJF = (Business Value + Time Criticality + Risk Reduction) / Job Size**

### Priority Categories

Based on the obtained RICE or WSJF estimates, tasks are assigned one of the following priorities:

- **Critical** - blocking issues affecting system operability
- **High** - important tasks necessary to achieve business goals
- **Medium** - tasks that improve the product but are not critical for current business goals
- **Low** - desirable improvements that can be postponed

### Prioritization Process

1. Evaluation of new tasks is done at the weekly Backlog Refinement
2. Re-evaluation of existing tasks is conducted at the beginning of each sprint
3. The technical leader has the right to raise the priority of technical tasks
4. Prioritization of technical debt tasks is done separately (see the "Technical Debt Management" section)
