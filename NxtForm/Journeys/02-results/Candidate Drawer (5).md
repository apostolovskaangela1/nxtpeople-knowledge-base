# Candidate Drawer \(5\)

The candidate drawer is the full review panel for a single submission. It opens as a slide-over panel and keeps the Results table visible in the background so reviewers can inspect details without losing table context.

#  Instructions

1. **Open the drawer** by clicking a candidate row or candidate name in Results.

   \[Insert screenshot: candidate table with the selected row or candidate name highlighted\]
2. **Confirm the correct submission** by checking the drawer title and reviewing the contact and candidate metadata in the header.

   \[Insert screenshot: open drawer header showing title and candidate details\]
3. **Review the relevant tab** by switching between Answers, History, Note, and Referrals depending on the task.

   \[Insert screenshot: drawer tabs with the active tab highlighted\]
4. **Take action if needed** using controls such as status change, validation, reminders, copy link, NxtMatch, or delete, based on permissions and available data.

   \[Insert screenshot: action area in the drawer header\]

Clicking a progress dot can open the drawer directly and focus a specific Journey step in the Answers tab.

# Drawer header

The header can display core submission identity and available actions.

- Candidate full name
- Age
- Deleted-candidate warning
- Email
- Phone
- Birthdate
- Address
- Previous and next candidate controls
- Status changer
- Validate action
- Reminders
- Copy link
- NxtMatch action
- Delete action

Birthdate appears only when a real birthdate exists, not a placeholder or dummy value.

\[Insert screenshot: complete drawer header with navigation, candidate metadata, and actions\]

# Navigation and closing

## Navigate between candidates

You can move through nearby submissions without closing the drawer.

- Use the previous chevron
- Use the next chevron
- Use **Arrow Up** or **Arrow Down** when focus is not inside an input or text control

The system loads adjacent submissions or additional rows when needed. If navigation reaches beyond the currently loaded list, infinite scrolling may load another page before opening the adjacent candidate.

\[Insert screenshot: previous/next controls in the drawer header\]

## Close the drawer

Use the drawer close control to return to the base Results table. The route preserves active filters and query parameters.

\[Insert screenshot: close control in the drawer\]

## Previous/next and filtering

Opening a drawer preserves the filtered table context. If filters change while the drawer is open:

- Previous and next availability is recalculated
- The active submission may remain if it is still loaded
- A missing submission may be fetched by ID
- Closing returns to the filtered Results route

# Drawer tabs

## Answers tab

The Answers tab loads the full submission and groups information by candidate steps.

- Fetches a full submission
- Groups information by candidate steps
- Shows step answers
- Can focus a specific step if opened from a progress dot
- Can show a loading state while full submission data is retrieved
- Shows an empty state if no candidate steps exist

Answers are associated with candidate steps and modules. Editing an answer follows the candidate-answer editing workflow and the validation or confirmation rules implemented in the drawer.

\[Insert screenshot: Answers tab with grouped steps and answers\]

## History tab

History shows the chronological record of submission occurrences, including:

- State changes
- Comments
- Answer changes
- Notifications and reminders
- Notification status
- Users who performed actions
- Reasons attached to changes

**History** is not the same as **Last activity**:

- Last activity is a compact updated timestamp in the table
- History is the detailed event and occurrence record

\[Insert screenshot: History tab showing occurrence timeline\]

## Note tab

The Note tab is for internal submission commentary.

- Displays the current submission note
- Provides a textarea for a new comment
- Strips script tags before saving
- Validates the commentary
- Posts the comment as a submission occurrence
- Shows a success notification after save

\[Insert screenshot: Note tab with current note and comment textarea\]

## Referrals tab

The Referrals tab shows referral context for the submission.

- Entry referral details: team, tenant, code, language
- Forwarded referrals: referral cards for associated forwarded referrals

Use this tab to verify candidate origin, identify the team or tenant, confirm referral code and language, and distinguish entry referral context from forwarded referral context.

\[Insert screenshot: Referrals tab showing entry and forwarded referrals\]

# Actions and meanings

The drawer can expose several actions. Availability depends on data and permissions.

- Status changer
- Validate
- Remind by mail
- Remind by SMS
- Copy candidate link
- Open in NxtMatch
- Delete

| Element | What it means | What the user can do |
| --- | --- | --- |
| Drawer title | Candidate identity | Confirm the intended submission |
| Contact details | Email, phone, birthdate, address | Review available candidate context |
| Previous/next | Move among loaded candidates | Navigate without closing context |
| Status changer | Manual submission-state control | Change or reset status |
| Validate | Candidate identity or submission validation workflow | Match or create a candidate |
| Reminder buttons | Email or SMS communication actions | Send reminders when data and permissions allow |
| Copy link | Internal candidate drawer link | Copy for authorized internal use |
| NxtMatch | Opens the candidate in external NxtMatch | Review the candidate when matched |
| Delete | Soft-delete action | Remove the active submission when authorized |
| Drawer tabs | Answers, History, Note, Referrals | Review separate information types |

# Practical notes

- Opening a drawer is a review-and-action workflow, not necessarily an editing operation.
- Status and note changes are persisted as submission occurrences.
- Candidate validation can create or match a candidate and may change submission state.
- Deleting the active submission closes the drawer if that submission is currently open.

#  Related articles

- [Candidate table](Results-%20Candidate%20Table%20%284%29.md)
- [Status and validation](Results%20Status%20and%20Validation%20%286%29.md)
- [Reminders and links](Results%20Actions-%20Reminders%2C%20Candidate%20Links%2C%20and%20NxtMatch%20%287%29.md)
