# superhuman-life-os storage and templates

These templates are for the receiving platform to instantiate. They are not existing user records. Keep `unset`, `unverified`, and `unknown` values honest rather than filling them to simulate completion.

## 1. Default structure and equivalent mappings

Use Markdown by default. Platforms without a filesystem may use objects they can reliably save, update, and locate. Record equivalent addresses in `system/platform.md`. Do not depend on an author's local absolute paths, account, or files outside this package.

```text
superhuman-life-os-data/INSTANCE-ID/
  system/
    RULES.md            Entry point for persistently stored operating instructions
    config.md           Effective settings and user confirmation sources
    platform.md         Actual storage mappings, capability evidence, conditions
    build-state.md      Progress, blockers, and next step
    reminders.md        Real tasks, activity completion, and invitation runs
    acceptance.md       Acceptance results and evidence
    changes.md          Chronological, append-only change record
  sources/
    index.md            Source IDs, coverage, and locations
    S-DATE-SEQUENCE.md  Original material or a reliably retrievable native reference
  wiki/
    index.md            Navigation, Focus, open items, and system metrics
    profile.md          Current background; separate self-reports and conclusions
    modules.md          This user's module registry, initially empty
    modules/            Personal module overviews created after confirmation
    topics/             Related topics created as needed
    methods/            Candidate and practically tested methods
    assets/             Candidate and confirmed asset assessments
    questions.md        Unknowns, contradictions, and open inquiries
  journal/
    daily/              YYYY-MM-DD.md
    weekly/             YYYY-Www.md, using the ISO week-numbering year
    monthly/            YYYY-MM.md
    quarterly/          YYYY-Qn.md
  decisions/
    index.md            Index of open and closed decisions
    D-DATE-SEQUENCE.md  Original decision basis and appended reviews
  inbox.md              Inputs awaiting processing; clearing does not authorize deletion
  validation/           Test material and evidence isolated from personal records
```

Initially create only navigation, system state, and necessary empty entry points. Add topics, methods, and period records during real use. Equivalent platform mappings do not require a new product design, but must preserve source, history, and confirmation requirements.

The module registry starts empty. Create modules from the current user's interview proposal after explicit adoption. Use stable instance-local IDs such as `M-0001`, with user-chosen names. A name is not an ID. Renaming preserves the ID; merging and splitting preserve mappings and original records.

Registry fields:

`ID | Name | Purpose and scope | Direction | Initiative | Lifecycle | Focus | Boundaries | User confirmation source | Overview location`

Each overview records current self-reports, desired changes or conditions to protect, related projects, reusable methods, and relationships to other modules. Unknowns stay unknown; do not create placeholder life events. Lifecycle is `draft / active / paused / archived`. Drafts do not receive proactive authority.

Direction may be growth, maintenance, exploration, recovery, or the user's own description. Initiative is `Advance / Maintain / On demand`, defaulting to On demand until confirmed. Names and direction do not automatically set initiative.

Record IDs are unique within the instance and remain stable when titles change. Use the actual date and an incrementing sequence; check for collisions before writing. Deduplicate updates and retries by source ID. Business dates use the agreed time zone, and timestamps include offsets. Unknown event time remains unknown, separate from record creation time.

## 2. System configuration template

The system fills these fields from questions and verified environment information. Personal settings carry confirmation sources. Suggested parameters are not automatically active.

| Field | Initial value |
|---|---|
| Product version | 0.1.0-beta.1 |
| Instance ID | Generate during setup; do not embed secrets |
| Platform and sole entry point | To be identified |
| Storage root and rule entry point | Create and read back |
| Build status | building |
| User direction, background, and language | Awaiting onboarding; do not infer identity or goals |
| Historical import scope | Not authorized; do not read other material by default |
| Module registry | Empty until interview confirmation |
| Focus and action limits | Unset; recommend 1–3 modules and at most 3 weekly actions, adjustable |
| Initiative per module | On demand until confirmed |
| Time zone | Unset |
| Everyday invitation date pattern and local time | Unset; suggest once daily, with user-selected days allowed |
| Weekly day and local time | Unset |
| Notification channel and task IDs | Not configured |
| Major-decision triggers | Unconfirmed and inactive |
| Relevant module risk boundaries | Unset |
| Follow-up limit | Unconfirmed |
| Recording exclusions | Ask before personal interview; user may add exclusions anytime |
| Verified supported input formats | Unverified |
| 2–3 system health metrics | Not selected |

Configuration changes:

`Time | Field | Previous value | New value | User confirmation source | Actual configuration result`

## 3. Platform and build state templates

Capability table:

`Capability | Required? | Actual tool/object | Status | Test time | Evidence location | Operating conditions | Gap and next step`

Storage mapping:

`Logical path or purpose | Actual object ID/address | Read method | Write method | Later-conversation access evidence`

Build state:

```text
Product version: 0.1.0-beta.1
Last verification: Not started
Current stage: 0
Status: building
Completed steps and evidence: None
Real task and object IDs: None
User input needed: Determine from current stage
Known capability gaps: Not yet checked
Next step: Identify current platform and existing state
```

## 4. Original source template

```text
Source ID:
Source kind: Life OS conversation / user-provided material / public source / validation
Capture time and time zone:
Event time: Known value or unknown
Original location:
Coverage: Conversation, message range, or material range
Completeness: Complete / incomplete, with the specific gap
Authorized scope and exclusions: Record boundaries without repeating excluded content
Original content or stable reference:
Corrections: Append time, explanation, and links; do not rewrite the original
Related Wiki entries and decisions:
```

Conversation sources preserve each message's role, body, identifier, and available time. If a native message ID is unavailable, generate a local one without representing it as a platform ID. Mark missing original timestamps. References must resolve at least to a message, paragraph, or document section.

For outside material, record title, author or organization where known, link, publication and access dates, and the portions used. Respect usage rights. Complete conversation retention does not authorize copying entire books or restricted sources.

## 5. Wiki entry template

```text
Entry ID / title:
Type: Self-report / fact / inference / question / suggestion / method / asset assessment
Created / last updated:
Related module IDs:
Current content:
Scope and exclusions:
Source references: Source ID plus message/paragraph/section; derived work traces to originals
Evidence state: open / supported / refuted / not_applicable
User confirmation: pending / confirmed / withdrawn / not_applicable
Confirmation source: Leave unset and marked unconfirmed when absent
Review date (review_by) or condition: Required for inferences; explicitly unresolved items enter the open-items list
Related entries and contradictions:
Change history: Append date, prior belief summary, reason, and new-version location
```

The profile separates self-reports, confirmed long-term conclusions, and interpretations awaiting evidence or confirmation. Ordinary self-reports do not need repeated approval. Automatic organization cannot confirm a long-term conclusion. Method entries also describe supporting practice, failures or counterexamples, and scope; insufficiently supported methods remain candidates.

## 6. Important decision template

```text
Decision ID:
Time recorded before the decision:
Decision content:
Status: draft / decided / in_progress / closed
User confirmation source: Mark unconfirmed if no decision has been made
Goals and constraints:
Options considered:
Basis at the time: Separate facts, self-reports, and inferences; use stable sources/snapshots
Key assumptions and expected outcomes:
Risks and worst acceptable consequences:
Conditions for exiting or reconsidering:
Review date or trigger:
Actual execution state and its source:

Appended review:
- Time and evidence:
- What actually happened:
- Which assumptions are supported, refuted, or still unknown:
- Assessment of the decision process:
- Assessment of the outcome:
- Implications for the next decision:
- If the decision changes, the user's explicit choice and its source:
```

Changes after the initial record go into the append section. Unknown expectations or triggers remain unknown with an explanation. Do not fabricate a prediction retrospectively. Drafts may be saved, but must not appear in the index as executed commitments.

## 7. Daily, Review, and navigation templates

Daily:

`Date and time zone | Source coverage | Completion and closing evidence | Self-reports and facts | Inferences and questions | Suggestion/decision links | Related modules | Wiki updates`

Review:

`Period | Status (draft/complete/pending) | Source coverage | Changes | Inferences and evidence updates | Decisions due and exit conditions | Energy/resource review | Assets and methods worth keeping | Proposed actions and tradeoffs | User confirmation | Appended corrections`

Choose useful fields for the period. Unsupported content remains unknown or not applicable. Weekly checks inferences and exit conditions; Monthly synthesizes Weekly with source access as needed; Quarterly reassesses Focus and resource use. Do not force a conclusion into every field.

Wiki navigation:

`System direction and build status | Initial/current Focus | Module entry points | Topics/methods/assets | Open decisions and questions | Recent changes | Metrics and measurement scope | Source index`

Change log:

`Time | ingest/query/lint/rule_change/correction | Sources and entries | What changed | Confirmation where required | Old/new location mapping where needed | Success or unfinished work`

## 8. Invitation and completion templates

Real tasks:

`Purpose | Real task ID | Platform state | Time zone and schedule | Next run | Rule location | State location | Last checked`

Activity state:

`Instance ID and period key | open/in_progress/complete/skipped | Completion or skip time | User statement and saved-content references`

Invitation runs:

`Instance ID and period key | Attempt ID | Trigger time | Activity state read before sending | queued/sending/sent/failed/unknown/suppressed | Delivery evidence | Reschedule authority | Next action`

Tasks must read the same completion state. Record creation, execution, and delivery separately. Postponing an invitation does not complete the activity. Ignoring a notification does not authorize another. Retries must recognize existing attempts rather than simply send again.

## 9. Acceptance report template

```text
Platform / entry point / package version:
Actual storage and rule entry point:
Required settings completed:
Results: List A01–A22 with status, time, evidence, and limitations
Verified operating conditions:
Required items still incomplete:
Optional capabilities and gaps:
Overall status: building / awaiting_input / awaiting_verification / incomplete / complete
Next step and who can perform it:
```

Use complete only after all required checks pass with actual evidence and necessary onboarding is finished. Never invent evidence, file paths, or task IDs.

## 10. Instance isolation and version information

Every source, Wiki entry, decision, task, and acceptance record belongs to one instance. Resolve relative paths only within that instance's authorized root. Do not search across instances or reuse private content without explicit authorization. A shared product template is not a shared user database.

In `system/config.md`, retain product version, data schema version, user rule overrides, and confirmation sources. This release uses schema version `1`. Before upgrading, compare changes with personal overrides, preserve a backup or restorable version, act within user authorization, and recheck affected behavior. Distribution packages must never contain personal operating-data directories.
