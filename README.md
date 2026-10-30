# Mavenlink

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Mavenlink is the professional services automation (PSA) platform now shipped as Kantata OX, following the 2022 merger of Mavenlink and Kimble Applications that formed Kantata. It combines project management, resource management and forecasting, time and expense tracking, project accounting, invoicing, rate cards, and business intelligence for services organizations. The public REST API is still served from the original Mavenlink domain at https://api.mavenlink.com/api/v1/ and is documented as the "Kantata OX API" at developer.kantata.com: a Swagger 2.0 contract covering 419 operations across 218 paths and roughly 100 resource groups, authenticated with OAuth 2.0 authorization-code bearer tokens issued from app.mavenlink.com. Alongside REST the company operates an OAuth-gated remote MCP server at https://api.mavenlink.com/mcp, publishes an A2A agent card and an anonymous documentation MCP server on its developer portal, and ships a gRPC connector service definition that third parties implement to extend the Kantata Workflow Platform with custom triggers and actions.

**Areas:** Professional Services Automation · Project Management · Resource Management · Time Tracking · Expense Management · Invoicing · Project Accounting · Business Intelligence · Workflow Automation · MCP · Agent-Native · Company

## Mavenlink on APIs.io

Everything profiled for Mavenlink is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/mavenlink/](https://apis.io/providers/mavenlink/)** — or go straight to one of the APIs or properties below.

### APIs (103)

- [Kantata OX MCP Server](https://apis.io/apis/mavenlink/kantata-ox-mcp-server/) — Remote Model Context Protocol server operated by Kantata on the Mavenlink API host. Advertised anonymously through RFC 9728 protected-resource metadata at…
- [Kantata OX Developer Documentation Agent](https://apis.io/apis/mavenlink/kantata-ox-developer-documentation-agent/) — Agent surface published on the Kantata developer portal. Serves an A2A agent card at /.well-known/agent-card.json (protocolVersion 0.3.0) that advertises an…
- [Mavenlink Access Group Memberships API](https://apis.io/apis/mavenlink/mavenlink-access-group-memberships-api/) — Access Groups allow you to manage product access for users. An Access Group Membership represents the connection of a user to an Access Group.
- [Mavenlink Account Colors API](https://apis.io/apis/mavenlink/mavenlink-account-colors-api/) — Account Colors are the colors available on a user's account that can be used to style workspaces.
- [Mavenlink Account Invitations API](https://apis.io/apis/mavenlink/mavenlink-account-invitations-api/) — Account Invitations represent invitations for non-users to join a Kantata OX account.
- [Mavenlink Account Locations API](https://apis.io/apis/mavenlink/mavenlink-account-locations-api/) — Represents a location associated with an account.
- [Mavenlink Account Memberships API](https://apis.io/apis/mavenlink/mavenlink-account-memberships-api/) — Each user on an account will have an account membership that describes their relationship to the account. When you add a user to an account, create a new…
- [Mavenlink Activations API](https://apis.io/apis/mavenlink/mavenlink-activations-api/) — The Rate Card activation endpoints allow you to check whether the Rate Cards feature has been activated on the user's account. It also allows you to…
- [Mavenlink Assignments API](https://apis.io/apis/mavenlink/mavenlink-assignments-api/) — The Assignments object allows you to view and manage task assignments for named or [unnamed…
- [Mavenlink Attachments API](https://apis.io/apis/mavenlink/mavenlink-attachments-api/) — An Attachment is a file asset that is attached to another Kantata OX object. Depending on the type of object, the file is used or displayed in different…
- [Mavenlink Backup Approver Associations API](https://apis.io/apis/mavenlink/mavenlink-backup-approver-associations-api/) — A Backup Approver Association represents the relationship of a delegated approver to a range of specific dates. Approval responsibilities are delegated to a…
- [Mavenlink Billable Utilizations API](https://apis.io/apis/mavenlink/mavenlink-billable-utilizations-api/) — Represents the billable utilization target for an account member. Each record has an effective date; the active billable utilization is the one with the…
- [Mavenlink Billing Milestones API](https://apis.io/apis/mavenlink/mavenlink-billing-milestones-api/) — Billing milestones allow you to set up billable items in a project that are separate from the Task Tracker work and have invoicing rules. A set of billing…
- [Mavenlink Client Invoice Defaults API](https://apis.io/apis/mavenlink/mavenlink-client-invoice-defaults-api/) — Represents the default configuration for presenting invoices to clients.
- [Mavenlink Cost Rates API](https://apis.io/apis/mavenlink/mavenlink-cost-rates-api/) — Cost Rate represents the hourly cost for an account member, specified in a specific currency. A cost rate with the same currency as the account default…
- [Mavenlink Currencies API](https://apis.io/apis/mavenlink/mavenlink-currencies-api/) — This object allows you to view the [names, ISO codes, and symbols of currencies supported by Kantata…
- [Mavenlink Custom Branding API](https://apis.io/apis/mavenlink/mavenlink-custom-branding-api/) — The Custom Branding API from Mavenlink — 1 operation(s) for custom branding.
- [Mavenlink Custom Field Choices API](https://apis.io/apis/mavenlink/mavenlink-custom-field-choices-api/) — Custom Field Choices are possible values for `'single'` and `'multi'` type custom fields.
- [Mavenlink Custom Field Sets API](https://apis.io/apis/mavenlink/mavenlink-custom-field-sets-api/) — Custom Field Sets contain custom fields and definitions of each fields' subject type. The supported subjects are currently *Workspace*, *Story*, *User*, and…
- [Mavenlink Custom Field Values API](https://apis.io/apis/mavenlink/mavenlink-custom-field-values-api/) — If [Custom Fields](/tag/Custom-Fields) represent the fields themselves, Custom Field Values represent the values in/of those fields. The Custom Field Values…
- [Mavenlink Custom Fields API](https://apis.io/apis/mavenlink/mavenlink-custom-fields-api/) — The [Custom Fields](https://mavenlink.zendesk.com/hc/en-us/articles/202924760-Custom-Fields-Overview-#arrange) object allows you to view, create, update,…
- [Mavenlink Daily Scheduled Hours (Story Allocation Days) API](https://apis.io/apis/mavenlink/mavenlink-daily-scheduled-hours-story-allocation-days-api/) — Daily Scheduled Hours (also called Story Allocation Days) is the allocation of time for a resource to spend on a specific task, on a specific day. Daily…
- [Mavenlink Data Export Schema API](https://apis.io/apis/mavenlink/mavenlink-data-export-schema-api/) — This object allows you to export specific data sets from Kantata OX. You can view the full schema of available data sets using this endpoint. To use this…
- [Mavenlink Data Exports API](https://apis.io/apis/mavenlink/mavenlink-data-exports-api/) — This object allows you to export specific data sets from Kantata OX. You can create or cancel exports. You can also view the full schema of available data…
- [Mavenlink Estimate Scenario Resource Allocations API](https://apis.io/apis/mavenlink/mavenlink-estimate-scenario-resource-allocations-api/) — Estimate Scenario Resource Allocations contain time-related data for scenario resources, used for calculating estimated cost and scheduled hours.
- [Mavenlink Estimate Scenario Resources API](https://apis.io/apis/mavenlink/mavenlink-estimate-scenario-resources-api/) — Estimate Scenario Resources represent placeholders for unnamed resources in a specific estimate scenario.
- [Mavenlink Estimate Scenarios API](https://apis.io/apis/mavenlink/mavenlink-estimate-scenarios-api/) — An Estimate Scenario is a possible project configuration, consisting of an estimated budget, rate card, resources, and other related fields for a specified…
- [Mavenlink Estimates API](https://apis.io/apis/mavenlink/mavenlink-estimates-api/) — An Estimate represents a potential project. Estimates allow you to plan out a project's budget, resources, and allocations through associated estimate…
- [Mavenlink Event Types API](https://apis.io/apis/mavenlink/mavenlink-event-types-api/) — A change is called a [Subscribed Event](https://mavenlink.zendesk.com/hc/en-us/articles/4407962435227), and the type of change is called a *Subscribed Event…
- [Mavenlink Events API](https://apis.io/apis/mavenlink/mavenlink-events-api/) — Up to 9 days of trackable changes ("events") for an account can be accessed via the Subscribed Events API. For a list of all the event types tracked by…
- [Mavenlink Exchange Tables API](https://apis.io/apis/mavenlink/mavenlink-exchange-tables-api/) — This object allows you to view or edit foreign currency exchange rates, depending on your [Foreign Exchange Access Group…
- [Mavenlink Expense Budgets API](https://apis.io/apis/mavenlink/mavenlink-expense-budgets-api/) — Expense budgets allow you to plan for non-labor expenses.
- [Mavenlink Expense Categories API](https://apis.io/apis/mavenlink/mavenlink-expense-categories-api/) — An Expense Category represents the type of expense that is being reported. Expense categories have no attributes and consist of just their name as a string.…
- [Mavenlink Expense Report Submissions API](https://apis.io/apis/mavenlink/mavenlink-expense-report-submissions-api/) — Expense report submissions contain a set of expense line items. These expenses must be approved through an expense report submission before they can be…
- [Mavenlink Expenses API](https://apis.io/apis/mavenlink/mavenlink-expenses-api/) — Expenses are defined as costs incurred as part of a project, but not related to time. Once created, expenses can be included in generated invoices.
- [Mavenlink External Payments API](https://apis.io/apis/mavenlink/mavenlink-external-payments-api/) — An external payment is a manual record of a payment made outside of Kantata OX. An external payment can be applied to an invoice, or just recorded directly…
- [Mavenlink External References API](https://apis.io/apis/mavenlink/mavenlink-external-references-api/) — External References allows users see which objects (one of `Assignment`, `BillingMilestone`, `CustomField`, `CustomFieldChoice`, `CustomFieldSet`,…
- [Mavenlink Followers API](https://apis.io/apis/mavenlink/mavenlink-followers-api/) — Story Follows allow users to follow a task to which they are not assigned.
- [Mavenlink Holiday Calendar Associations API](https://apis.io/apis/mavenlink/mavenlink-holiday-calendar-associations-api/) — A Holiday Calendar Association represents the relationship between holiday objects and calendar objects. A Holiday can be associated with several different…
- [Mavenlink Holiday Calendar Memberships API](https://apis.io/apis/mavenlink/mavenlink-holiday-calendar-memberships-api/) — A list of all calendars associated to an individual user.
- [Mavenlink Holiday Calendars API](https://apis.io/apis/mavenlink/mavenlink-holiday-calendars-api/) — Holiday Calendars define the days in which account members are unavailable to work due to company-wide days off.
- [Mavenlink Holidays API](https://apis.io/apis/mavenlink/mavenlink-holidays-api/) — Holidays are the company-wide days off that have been added to a user's Kantata OX account.
- [Mavenlink Insights Access Group Memberships API](https://apis.io/apis/mavenlink/mavenlink-insights-access-group-memberships-api/) — [Insights Access Groups](https://mavenlink.zendesk.com/hc/en-us/articles/115002115073) allow you to manage classic Insights access for users. An Insights…
- [Mavenlink Insights Dynamic Dashboards API](https://apis.io/apis/mavenlink/mavenlink-insights-dynamic-dashboards-api/) — Built with an easy-to-use, modern, and intuitive dashboard editor, Insights dynamic dashboards are based on the same powerful data engine as classic…
- [Mavenlink Insights Report Exports API](https://apis.io/apis/mavenlink/mavenlink-insights-report-exports-api/) — This object allows you to manage scheduled exports of classic Insights reports from Kantata OX. An export of a classic Insights report that is scheduled to…
- [Mavenlink Insights Reports API](https://apis.io/apis/mavenlink/mavenlink-insights-reports-api/) — View a list of classic Insights reports.
- [Mavenlink Invoices API](https://apis.io/apis/mavenlink/mavenlink-invoices-api/) — Users can create Invoices in a Kantata OX project. An Invoice must have at least one line item (a time entry, expense, fixed fee item, or additional item).…
- [Mavenlink Line Item Locks API](https://apis.io/apis/mavenlink/mavenlink-line-item-locks-api/) — Line Item Locks provide a way for you to lock time in the past so that previous time entries cannot be edited or updated and new time entries cannot be…
- [Mavenlink Organization Memberships API](https://apis.io/apis/mavenlink/mavenlink-organization-memberships-api/) — An Organization Membership represents the connection of a user and project to an organization.
- [Mavenlink Organizations API](https://apis.io/apis/mavenlink/mavenlink-organizations-api/) — The Organizations feature in Kantata OX is composed of two independent trees: Department and Geography. Each has its own hierarchy structure. Users and…
- [Mavenlink Participations API](https://apis.io/apis/mavenlink/mavenlink-participations-api/) — A participation represents the relationship between a participant and a project, including a participant's permission level, whether they're a provider or…
- [Mavenlink Posts API](https://apis.io/apis/mavenlink/mavenlink-posts-api/) — A Post represents a message written by participants in a project that appears in the project. Replies are only included if they are directly related to a…
- [Mavenlink Project Accounting Records API](https://apis.io/apis/mavenlink/mavenlink-project-accounting-records-api/) — The [Project Accounting](https://mavenlink.zendesk.com/hc/en-us/articles/4403832107419-Project-Accounting) Records object allows you to view, create, and…
- [Mavenlink Project Snapshots API](https://apis.io/apis/mavenlink/mavenlink-project-snapshots-api/) — Project snapshots capture the state of a project at a specific point in time. Snapshots are useful for gaining a historical perspective on a project, and…
- [Mavenlink Project Template Additional Tabs API](https://apis.io/apis/mavenlink/mavenlink-project-template-additional-tabs-api/) — Project Template Additional Tabs are additional tabs configured in a project template that are added to a project when the template is applied.
- [Mavenlink Project Template Assignments API](https://apis.io/apis/mavenlink/mavenlink-project-template-assignments-api/) — Project Template Assignments(Project Template Resources) represent placeholders for task assignees in project templates. These assignments are mapped to…
- [Mavenlink Project Template Expense Budgets API](https://apis.io/apis/mavenlink/mavenlink-project-template-expense-budgets-api/) — Project Template Expense Budgets are expense budgets configured in a project template that are added to a project when the template is applied.
- [Mavenlink Project Templates API](https://apis.io/apis/mavenlink/mavenlink-project-templates-api/) — Project Templates are sets of tasks and attributes that can be applied to new or existing projects. A single template can be used on any number of projects.…
- [Mavenlink Rate Card Role (Rate for a Role) API](https://apis.io/apis/mavenlink/mavenlink-rate-card-role-rate-for-a-role-api/) — Rate Card Roles belong to a Rate Card Version and represent the bill rate, in cents per hour, for a specific Role. For example, the rate for the role of…
- [Mavenlink Rate Card Set Version (Effective version by Date) API](https://apis.io/apis/mavenlink/mavenlink-rate-card-set-version-effective-version-by-date-api/) — In the Rate Card system, Rate Card Set Versions represent snapshots of a Rate Card Set, that take effect on the set published date. A Rate Card Set Version…
- [Mavenlink Rate Card Sets (Group of Rate Cards) API](https://apis.io/apis/mavenlink/mavenlink-rate-card-sets-group-of-rate-cards-api/) — A Rate Card Set represents a group of Rate Cards with multiple currencies that can be bundled together. A Rate Card Set belongs to an account and can have…
- [Mavenlink Rate Card Table Rows API](https://apis.io/apis/mavenlink/mavenlink-rate-card-table-rows-api/) — Each Rate Card Table Row represents a role and its rates and currencies for a specific [Rate Card Set…
- [Mavenlink Rate Card Versions API](https://apis.io/apis/mavenlink/mavenlink-rate-card-versions-api/) — Rate Card Versions represent a snapshot of a Rate Card at a specified point in time. They are used to set the default rate. Rate Card Versions belong to a…
- [Mavenlink Rate Cards (Multiple Currencies) API](https://apis.io/apis/mavenlink/mavenlink-rate-cards-multiple-currencies-api/) — Rate Cards belong to a Rate Card Set and represent the currencies in that set. Rate Cards have many Rate Card Versions which represent the effective version…
- [Mavenlink Recommendations API](https://apis.io/apis/mavenlink/mavenlink-recommendations-api/) — A Recommendation suggests a User for an Unnamed Resource (or some other un-staffed position). The system recommends Users based on how well they match the…
- [Mavenlink Resource Requests API](https://apis.io/apis/mavenlink/mavenlink-resource-requests-api/) — Resource Requests are used as a method for a requestor to ask an approver to staff a resource. Resource Requests are associated to a workspace resource and…
- [Mavenlink Revenue Recognition Methods API](https://apis.io/apis/mavenlink/mavenlink-revenue-recognition-methods-api/) — Revenue recognition methods determine how revenue is recognized. Methods are configured at the account level, then each project can have an available method…
- [Mavenlink Roles API](https://apis.io/apis/mavenlink/mavenlink-roles-api/) — A Role represents the main position or title assigned to members on an account. Roles may be associated with account memberships, account invitations,…
- [Mavenlink Skill Categories API](https://apis.io/apis/mavenlink/mavenlink-skill-categories-api/) — A Skill Category represents the classification for a group of skills. Options are 'Skill', 'Language', 'Certification', and 'Other'. Skill categories are…
- [Mavenlink Skill Memberships API](https://apis.io/apis/mavenlink/mavenlink-skill-memberships-api/) — Skill Memberships represent skills that has been assigned to a specified user.
- [Mavenlink Skills API](https://apis.io/apis/mavenlink/mavenlink-skills-api/) — Skills are used in Kantata OX to describe capabilities of users for the purposes of resource planning. They can be associated with a user through a Skill…
- [Mavenlink Status Reports API](https://apis.io/apis/mavenlink/mavenlink-status-reports-api/) — A Status Report represents a snapshot of a Workspace's status across several categories at a moment in time. Status Reports are usually referred to as…
- [Mavenlink Stories API](https://apis.io/apis/mavenlink/mavenlink-stories-api/) — Stories are tasks, milestones, deliverables, or issues in Kantata OX. They belong to Workspaces, show up in the local and global task trackers, can be…
- [Mavenlink Story Dependencies API](https://apis.io/apis/mavenlink/mavenlink-story-dependencies-api/) — Story dependencies define relationships between tasks and the sequence in which they must be completed in order to close a project. A dependency is between…
- [Mavenlink Story State Changes API](https://apis.io/apis/mavenlink/mavenlink-story-state-changes-api/) — Story State Changes in Kantata OX act as an audit trail for changes to the state of a Story. Story State Changes cannot be created directly. They will be…
- [Mavenlink Story Tasks API](https://apis.io/apis/mavenlink/mavenlink-story-tasks-api/) — Story Tasks are used in Kantata OX to track a list of checklist items within a Story. This model includes a completion boolean and a position integer.
- [Mavenlink Survey Answers (Legacy) API](https://apis.io/apis/mavenlink/mavenlink-survey-answers-legacy-api/) — Survey Answers (Legacy) appear on and can be responded to through surveys. Survey Answers (Legacy) are required to have a value for the answer (i.e. answers…
- [Mavenlink Survey Questions (Legacy) API](https://apis.io/apis/mavenlink/mavenlink-survey-questions-legacy-api/) — Survey Questions (Legacy) appear on and can be responded to through surveys. **Note**: This feature requires the Surveys (Legacy) account add-on. This…
- [Mavenlink Survey Templates (Legacy) API](https://apis.io/apis/mavenlink/mavenlink-survey-templates-legacy-api/) — Survey Templates (Legacy) define a set of questions and defaults from which Survey Responses can be created. **Note**: This feature requires the Surveys…
- [Mavenlink Surveys Responses (Legacy) API](https://apis.io/apis/mavenlink/mavenlink-surveys-responses-legacy-api/) — Survey Response (Legacy) represents an instance of a particular survey that has been assigned for response. **Note**: This feature requires the Surveys…
- [Mavenlink Task Status Sets API](https://apis.io/apis/mavenlink/mavenlink-task-status-sets-api/) — Task Status Sets allow you to create custom statuses for tasks (stories) that can then be applied to projects.
- [Mavenlink Task Statuses API](https://apis.io/apis/mavenlink/mavenlink-task-statuses-api/) — Custom task statuses can be created to be used on tasks (stories). Custom task statuses are associated to task status sets, which can be applied to projects…
- [Mavenlink Time Entries API](https://apis.io/apis/mavenlink/mavenlink-time-entries-api/) — This object allows you to manage Kantata OX time entries, depending on your permissions. Creating and updating time entries allows you to include time when…
- [Mavenlink Time Off Entries API](https://apis.io/apis/mavenlink/mavenlink-time-off-entries-api/) — Time Off Entries represent the time and dates that a user has requested off from work, such as PTO or vacation days.
- [Mavenlink Timesheet Approvals API](https://apis.io/apis/mavenlink/mavenlink-timesheet-approvals-api/) — This section contains an endpoint to approve multiple Timesheet Submissions at once.
- [Mavenlink Timesheet Cancellations API](https://apis.io/apis/mavenlink/mavenlink-timesheet-cancellations-api/) — This section contains an endpoint to cancel multiple Timesheet Submissions at once.
- [Mavenlink Timesheet Rejections API](https://apis.io/apis/mavenlink/mavenlink-timesheet-rejections-api/) — This section contains an endpoint to reject multiple Timesheet Submissions at once.
- [Mavenlink Timesheet Submissions API](https://apis.io/apis/mavenlink/mavenlink-timesheet-submissions-api/) — Timesheet Submissions hold a set of time entries for a specified week, and can be approved, rejected, or canceled. You can enable timesheet submissions and…
- [Mavenlink User File Associations API](https://apis.io/apis/mavenlink/mavenlink-user-file-associations-api/) — User File Associations in Kantata OX act as a join object between Users, Workspaces, and Attachments / Google Documents.
- [Mavenlink User Group Memberships API](https://apis.io/apis/mavenlink/mavenlink-user-group-memberships-api/) — A User Group Membership represents the connection of a user to a [Workspace Group](/tag/Workspace-Groups). You must be an [Account…
- [Mavenlink Users API](https://apis.io/apis/mavenlink/mavenlink-users-api/) — Users represent the individuals that are participating in Kantata OX projects . User objects are often returned as nested JSON objects within other returned…
- [Mavenlink Vendors API](https://apis.io/apis/mavenlink/mavenlink-vendors-api/) — A Vendor is an entity to which an expense can be paid.
- [Mavenlink Workspace Allocations API](https://apis.io/apis/mavenlink/mavenlink-workspace-allocations-api/) — A workspace allocation represents a resource’s allocation over a specific period of time. A workspace allocation is always associate with a workspace resource.
- [Mavenlink Workspace Baselines API](https://apis.io/apis/mavenlink/mavenlink-workspace-baselines-api/) — A Gantt workspace baseline is a snapshot of a workspace at a particular point in time. The snapshot contains aggregate statistics and certain data about…
- [Mavenlink Workspace Groups API](https://apis.io/apis/mavenlink/mavenlink-workspace-groups-api/) — Workspace Groups (also known as groups) allow for the categorization of Kantata OX Workspaces. Workspace Groups are unique to each Kantata OX Account.
- [Mavenlink Workspace Invoice Preferences API](https://apis.io/apis/mavenlink/mavenlink-workspace-invoice-preferences-api/) — Workspace Invoice Preferences specify the default values that are applied to new invoices created for the specified project. It is only used for projects…
- [Mavenlink Workspace Resource Skills API](https://apis.io/apis/mavenlink/mavenlink-workspace-resource-skills-api/) — Workspace Resource Skills represent skills that have been assigned to a workspace resource.
- [Mavenlink Workspace Resources API](https://apis.io/apis/mavenlink/mavenlink-workspace-resources-api/) — A workspace resource is the object that is tied to assignments and allocations within a Workspace. Workspace Resources can be: - Named Resources: Resources…
- [Mavenlink Workspace Status Changes API](https://apis.io/apis/mavenlink/mavenlink-workspace-status-changes-api/) — Workspace Status Changes represent changes made to the status of a project.
- [Mavenlink Workspace Task Status Sets API](https://apis.io/apis/mavenlink/mavenlink-workspace-task-status-sets-api/) — Workspace Task Status Sets represent the connection between workspaces (projects) and task (story) status sets, which enable the use of custom task statuses.
- [Mavenlink Workspaces API](https://apis.io/apis/mavenlink/mavenlink-workspaces-api/) — Workspaces (also called projects) represent the space in which Kantata OX users plan, communicate, and collaborate.
- [Mavenlink Workweek Memberships API](https://apis.io/apis/mavenlink/mavenlink-workweek-memberships-api/) — A Workweek Membership represents the relationship of a user to a workweek.
- [Mavenlink Workweeks API](https://apis.io/apis/mavenlink/mavenlink-workweeks-api/) — Workweeks in Kantata OX are owned by an Account. They can be used as the default for an Account or can be associated to a User through a Workweek Membership.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Mavenlink Event Surface](https://apis.io/asyncapis/mavenlink/mavenlink-event-surface/)

#### MCP servers (2)

Model Context Protocol servers that expose the API to agents.

- [mavenlink-mcp.yml](https://apis.io/servers/mavenlink/mavenlink-mcp-yml/)
- [mcp](https://apis.io/servers/mavenlink/mcp/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Mavenlink Agentic Access](https://apis.io/agentic-access/mavenlink/mavenlink-agentic-access/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Mavenlink Openapi Overlay](https://apis.io/overlays/mavenlink/mavenlink-openapi-overlay/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Mavenlink Authentication](https://apis.io/security/mavenlink/mavenlink-authentication/)
- [Mavenlink Domain Security](https://apis.io/security/mavenlink/mavenlink-domain-security/)
- [Mavenlink Trust Center](https://apis.io/security/mavenlink/mavenlink-trust-center/)
- [Mavenlink Vulnerability Disclosure](https://apis.io/security/mavenlink/mavenlink-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Mavenlink Scopes](https://apis.io/scopes/mavenlink/mavenlink-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Mavenlink Plans Pricing](https://apis.io/plans/mavenlink/mavenlink-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Mavenlink Rate Limits](https://apis.io/rate-limits/mavenlink/mavenlink-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.kantata.com/)
- [Documentation](https://developer.kantata.com/)
- [Getting started](https://knowledge.kantata.com/hc/en-us/articles/202811760-Kantata-API-Overview)
- [API reference](https://developer.kantata.com/kantata/specification)
- [Pricing](https://www.kantata.com/pricing)
- [Support](https://www.kantata.com/customer-resources)
- [Blog](https://www.kantata.com/blog)
- [Terms of service](https://www.kantata.com/terms-of-use)
- [Privacy policy](https://www.kantata.com/privacy-policy)
- [GitHub](https://github.com/mavenlink)
- [Status](https://status.mavenlink.com/)

## API Evangelist rating

**Kin Score 55.2** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 56.1 |
| Contract governance | 4.5 |
| Operational transparency | 34.2 |
| Developer ergonomics | 66.1 |
| Access clarity | 46.1 |

**Agent readiness 61.7** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | conformant |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | distinct |

**Regulatory alignment 39.2** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/mavenlink/](https://apis.io/providers/mavenlink/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Mavenlink: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/mavenlink/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
