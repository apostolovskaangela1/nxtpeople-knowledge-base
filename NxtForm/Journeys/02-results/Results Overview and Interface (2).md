# Results Overview and Interface \(2\)

The Results tab is the operational review area for submissions completed or in progress for one selected Journey. It connects candidate information, Journey progress, submission state, answers, history, notes, referrals, reminders, validation, exports, and deletion.

**Purpose:** Use Results to review real submission records and perform operational actions for a selected Journey.

# Purpose

- Find a candidate submission
- Review progress and answers
- Check a submission state
- Validate candidate identity or submission information
- Send a reminder
- Review referral and candidate context
- Export or delete submissions where authorized

**Do not confuse Results with other Journey areas:**

- **Modify** changes Journey structure and content.
- **Preview** tests the candidate-facing experience.
- **Results** reviews existing submission records and operations.

# Start here

1. Open a Journey.
2. Select **Results**.
3. Review the search and filter controls.
4. Identify the relevant candidate row.
5. Open the row to use the candidate drawer.
6. Verify the outcome in the table or drawer.

# Screen structure

- Search field
- Filter confirmation panel
- Active-filter summary
- Select-all checkbox
- Candidate table
- Journey progress
- Submission state
- Last activity
- Row actions
- Bulk action bar
- Candidate drawer
- Loading, empty, and error states
- Infinite-scroll loading sentinel

# Elements and meanings

| Element | Meaning | What to do |
| --- | --- | --- |
| Candidate | Submission identity, name, and related metadata | Open or select the row |
| Search | Text search for the submission list | Enter text and allow the delayed search |
| Filters | Constraints applied to submissions | Confirm draft filters, apply, reset, or clear |
| Active-filter summary | Shows filters currently affecting the list | Review or remove individual conditions |
| Journey progress | Candidate progress across configured Journey steps | Hover or click dots to identify step state |
| State | Last submission state | Review or manually change if permitted |
| Last activity | Relative or formatted submission update time | Hover for created and updated timestamps |
| Three-dot menu | Candidate-specific actions | Open, remind, copy, history, delete, or NxtMatch |
| Bulk action bar | Actions for selected submissions | Use only for permitted selected records |
| Candidate drawer | Full candidate and submission detail panel | Review tabs and perform drawer actions |

# Candidate versus submission

A candidate is a person-level identity. A submission is one Journey participation record for that person or candidate context.

**Important distinctions:**

- One candidate can be associated with multiple submissions.
- Progress belongs to a particular submission and candidate-step context.
- State belongs to a submission.
- History belongs to submission occurrences and events.
- A note is stored on the submission's latest comment occurrence.
- Referral attribution can differ between entry and forwarded referrals.

# Submission state

A submission state describes operational progress. It is different from Journey progress, validation status, candidate identity, and candidate answer completeness.

The last submission state is stored on the submission and can change through candidate flow, consultant actions, callbacks, or other system events.

# Practical notes

- Opening a row does not itself change the submission.
- Changing status or validation can update records and history.
- Reminder and external actions create real communications or external updates.
- Deletion is destructive and permission-controlled.

# Related articles

- [Search and filters](Results-%20Search%20and%20Filters%20%283%29.md)
- [Candidate table](Results-%20Candidate%20Table%20%284%29.md)
- [Candidate drawer](Candidate%20Drawer%20%285%29.md)
- [Status and validation](Results%20Status%20and%20Validation%20%286%29.md)
- [Reminders and links](Results%20Actions-%20Reminders%2C%20Candidate%20Links%2C%20and%20NxtMatch%20%287%29.md)
- [Bulk actions](Bulk%20Selection%20and%20Bulk%20Actions%20%288%29.md)
- [Troubleshooting](Results%20Troubleshooting%20%2811%29.md)
