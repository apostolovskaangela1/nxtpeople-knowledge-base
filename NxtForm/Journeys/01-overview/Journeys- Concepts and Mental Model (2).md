# Journeys: Concepts and Mental Model \(2\)

This page explains what a Journey is, how to interpret Journey types and states, and where each concept appears in the interface.

**Screenshot placement:** add screenshots at the marked locations below using the exact UI visible in your environment.

A Journey is a structured candidate workflow that guides a person through configured steps, pages, questions, and outcome or content screens.

# What a Journey Represents

## Consultant perspective

- Operational purpose
- Journey type
- Lifecycle state
- Teams and tenant context
- Candidate languages
- Steps and modules or questions
- Preview and referral routes
- Submissions and candidate results

## Candidate perspective

The Journey is the questionnaire or application experience shown in the candidate UI.

# Journey Type

The seeded types are:

| Type | Meaning | Practical use |
| --- | --- | --- |
| Influx | Candidate inflow or recruitment-flow type | A Journey used to receive candidates into the workflow |
| Administration | Administrative or process-oriented Journey | A Journey with administrative purpose |
| Registration | Registration-focused Journey | A Journey primarily used to collect registration data |

Journey types can be configuration-controlled and may have translated names. The frontend fetches the available types from the API, so do not assume every tenant or environment exposes exactly the same descriptions.

# Journey State

The seeded states are:

| State | Meaning | Practical effect |
| --- | --- | --- |
| Draft | Journey is being prepared | Content editing is permitted |
| Waiting for approval | Journey is submitted for approval | Candidate visibility is waiting for reviewer action |
| Ongoing | Approved and open for candidates | Candidates can use it; content editing may be restricted |
| Ongoing but hidden | Open for candidates but hidden from normal listings | Candidate access can exist while overview visibility is hidden |
| Finished | No longer open for candidates | Candidate filling should stop; finished-state patch is limited after approval flow |

“Draft” and “Waiting” for approval support content editing. “Ongoing” and “Ongoing but hidden” are approved or open states. Finished is no longer open for filling.

State transitions are permission- and add-on-dependent. With Journey reviewing enabled, ongoing, hidden, finished, and draft transitions are restricted to permitted reviewing paths.

## Draft versus ongoing

A Draft Journey is prepared and editable.

An Ongoing Journey is approved and open for candidates. Ongoing can still be previewed and managed, but content editing is no longer generally allowed.

Ongoing but hidden is open operationally but hidden from listings or normal visibility logic.

## Waiting for approval

Waiting for approval means a reviewer or add-on workflow may be involved.

Users with the feature and review permissions can request approval, approve, reject, cancel review, or return an ongoing or finished Journey to draft according to allowed transitions.

# Archived versus Trashed

Journey deletion is soft deletion. The UI has a Show archived switch that sends `trashed=with`.

- **Hidden:** archived or trash records are excluded.
- **Visible:** trashed or archive records are included by the backend scope.
- A soft-deleted Journey can remain visible in technical retrieval and restore workflows.
- Normal overview cards can show archived state with lower opacity and an archived message.

# Validation Context

The Journey-level validation filter does not mean the Journey itself is being validated. It means the Journey has submissions that are pending validation.

If permission allows seeing all pending submissions, it compares against the total pending count. Otherwise it compares against the submissions the current user can see.

Only pending validation is therefore a workload or visibility filter, not a Journey state.

# Relationships

A Journey relates to:

- Customer, team, or tenant context
- Languages
- Journey type and state
- Steps
- Modules or questions
- Referrals
- Submissions
- Candidates and candidate steps
- Results and referral reporting

The overview is the entry point. It does not edit Journey structure; it finds and opens the Journey workspace.

# Elements and Meanings

| Element | Meaning | Effect |
| --- | --- | --- |
| Journey | Candidate workflow record | Determines candidate steps, content, state, and results |
| Journey type | General Journey category | Influences purpose, filtering, and configuration context |
| Journey state | Lifecycle or approval state | Controls visibility, editing, candidates, and transitions |
| Team or tenant | Organizational ownership context | Determines access and operational scope |
| Validation | Pending candidate or submission validation context | Applies a Journey-level workload filter |
| Archived | Soft-deleted Journey context | Hides or includes Journey in list scope |

# Related Articles

- [Overview interface](Journeys%20Overview%20Interface%20%283%29.md)
- [Search and sorting](Journeys-%20Search%20and%20Sorting%20%284%29.md)
- [Filters](Journeys%20Filters%20%285%29.md)
- [Cards, pagination, and creation](Journeys-%20Cards%2C%20Pagination%2C%20and%20Creation%20%286%29.md)
