# GitLab Development Practices

### 1. Issue Types

- **User Story**\
  A feature or requirement from the user's perspective.

- **Incident / Defect / Bug**\
  A report on an issue that needs to be fixed, typically a defect in the system.

- **Tasks**\
  Additional development tasks, including activities like deployment, code review, or any non-feature-related tasks.

---

### 2. Labels

- **Product Backlogs**\
  Work items that are yet to be assigned to a sprint or prioritized for development.

- **Sprint Backlogs**\
  Work items assigned to the current sprint cycle.

- **In Progress**\
  Work currently being developed.

- **QA Review**\
  The task is ready for Quality Assurance (QA) testing.

- **Functional Consultant (FC) Review**\
  Tasks pending review by the Functional Consultant to ensure alignment with business requirements.

---

### 3. Handling of Issues

- **Root Cause Analysis (RCA)**\
  When an issue arises, perform an RCA to understand the underlying cause of the problem. This is essential to avoid recurring issues and to improve the overall stability and quality of the system.

---

### 4. Development Practices

- **Pull or update your local development branch**\
  The first task every morning is to ensure that your local development branch is updated with the latest changes from the remote repository.

- **One Git Branch per Ticket / Issue**\
  Each branch should be isolated to one specific ticket or issue to ensure clarity and avoid conflicts.

- **Update Local Branch before Merge Requests (MR)**\
  Ensure your local branch is up to date with the remote branch before creating a Merge Request.

- **Meet Acceptance Criteria before Merge Requests (MR)**\
  All acceptance criteria must be fulfilled and tested before submitting a Merge Request. This ensures that the work meets the required standards and is ready for review.