# Results: Candidate Table \(4\)

The candidate table converts submission records into a compact operational list. Use it to identify candidates quickly, review progress and status, and take row-level actions without opening every record.

**Add screenshots:** Place a screenshot immediately below each section marked Screenshot. Use cropped images that focus on the specific UI element being described.

#  Instructions

1. Use the table header to understand what each column is for and what action it supports.
2. Review candidate identity and row metadata before changing state or using row actions.
3. Use progress dots, status pills, and row menus for fast navigation and updates.
4. Check warnings, validation badges, and timestamps before taking actions that affect the submission.

## Table headers

| Header | Meaning | User action |
| --- | --- | --- |
| Selection checkbox | Select one loaded submission | Use row selection or select all |
| Candidate | Candidate identity, metadata, referral, note, tags | Open drawer or row menu |
| Journey progress | Step completion and status | Click a candidate-step dot to focus that step |
| State | Last submission state | Open status changer and select a manual state |
| Last activity | Latest update time | Hover for created and updated timestamps |
| Actions | Row-specific actions | Open details, history, reminders, copy, NxtMatch, delete |

## Candidate identity

The Candidate column can show the main identity and supporting metadata needed to confirm who the submission belongs to.

- Full name
- Age
- Deleted-candidate warning
- Awaiting-validation badge
- Entry referral context
- Forwarded referral count
- Note preview
- Candidate tags

Name is derived from submission and candidate display logic. Use the name together with row metadata to confirm identity before taking an action.

## Deleted-candidate warning

A warning icon can indicate that the candidate record, submission, or related data is deleted.

Before acting:

- Confirm whether the submission is soft-deleted
- Verify deletion permissions and record context
- Do not assume deleted means fully removed or irreversible

Deletion indicators are contextual. Always verify what is deleted before making changes or interpreting the record state.

## Awaiting validation

Clicking the warning badge opens validation directly instead of only opening the drawer.

Validation is different from submission state:

- Validation answers whether a candidate identity or candidate record should be matched or posted
- State describes the submission workflow status

## Referral metadata

The candidate row can show referral context that helps explain source and routing.

- Entry referral team name
- Referral code
- Language name
- Forwarded referral count

Forwarded referrals are additional associated referrals excluding the entry referral.

Use this context to:

- Identify acquisition source
- Understand referral forwarding
- Compare candidates from different teams or codes

## Note preview

A note preview can show the latest submission comment.

It gives quick internal context, but the full note is available in the candidate drawer's Note tab.

## Tags

Tags appear as badges in the Candidate column.

Tags are candidate or submission categories used for reporting, filtering, and review. The exact meaning of a tag depends on the journey and configuration.

## Journey progress

Journey progress is calculated from journey steps and candidate steps.

Possible statuses include:

- Not reached
- In progress
- Passed
- Failed
- Awaiting confirmation
- Other configured progress states

Each progress dot:

- Represents a step
- Can show status, completion, or score in tooltip or detail text
- Opens the associated step in Answers if a candidate step exists

A dot is disabled when no candidate step exists.

## State

State is displayed as a colored pill or badge.

Available options come from submission states.

- Manual states can be selected
- Automatic or system states may be disabled for manual selection
- Reset returns overall status recalculation rather than always selecting a specific state

Changing state creates a submission occurrence or history entry when the state changes.

## Last activity

The Last activity column shows the latest update time in a compact format.

Display behavior:

- Within seven days, relative date and time text is displayed
- After seven days, same-year date may be shown as `d MMM`
- Older date may be shown as `dd/MM/yyyy`

Hover text contains created and updated timestamps.

## Row click versus row checkbox versus row action

- Normal row click opens the candidate drawer
- Checkbox selects the submission for bulk actions
- Candidate row action menu performs one-candidate actions
- Step progress dot opens Answers and focuses that candidate step
- Status pill changes submission state without opening the drawer

These controls do different things even when they appear in the same row. Make sure you are using the correct interaction for the task.

## Practical checks before acting

1. Confirm full name and identity metadata.
2. Check the deleted-candidate warning.
3. Review referral and team context.
4. Review journey progress and state.
5. Check the validation badge.
6. Confirm whether a row action will modify a submission or only open information.

## Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Selection checkbox | Selects a loaded submission | Open bulk actions |
| Candidate name | Submission identity | Open candidate drawer |
| Referral metadata | Entry team, code, and language context | Identify candidate source |
| Forwarded count | Associated redirected referrals | Understand referral forwarding |
| Note preview | Latest internal submission note summary | Open Note tab for detail |
| Tags | Candidate or submission category badges | Identify or filter grouped candidates |
| Progress dots | Step progress and status | Open a step in Answers |
| State pill | Last submission state | Change manually where allowed |
| Last activity | Latest update time | Hover for created and updated timestamps |
| Row menu | Candidate-specific actions | Open, remind, history, copy, NxtMatch, delete |

## Related articles

- [Results overview](Results%20Overview%20and%20Interface%20%282%29.md)
- [Search and filters](Results-%20Search%20and%20Filters%20%283%29.md)
- [Candidate drawer](Candidate%20Drawer%20%285%29.md)
- [Status and validation](Results%20Status%20and%20Validation%20%286%29.md)
