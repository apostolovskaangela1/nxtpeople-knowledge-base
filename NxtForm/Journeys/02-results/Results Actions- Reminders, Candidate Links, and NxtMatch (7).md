# Results Actions: Reminders, Candidate Links, and NxtMatch \(7\)

Use this guide to understand when reminder, candidate link, and NxtMatch actions are available in Results, what they do, and how to use them safely. These actions can contact candidates directly or open external systems, so they should be used with care.

**Important:** Reminder actions trigger real external communication. Do not send a reminder as a test using real candidate details.

#  Instructions

## Remind by mail

Email reminders are available only when all required conditions are met.

- Submission journey is not finished
- The journey has email configured as a required registration field
- The submission contains an email address

1. Open the candidate drawer or row menu.
2. Select **Remind by mail**.
3. The system sends the configured submission reminder email.
4. A submission occurrence can be recorded with the notification type and status.

When this action is unavailable:

- Finished journey
- Journey does not require registration email
- Candidate submission has no email

## Remind by SMS

SMS reminders are available only when all required conditions are met.

- Journey is not finished
- Phone number is required in journey registration fields
- The submission contains a usable phone number

1. Open the candidate drawer or row menu.
2. Select **Remind by SMS**.
3. The backend builds the language-specific SMS text.
4. SMS is sent immediately by the configured SMS provider.
5. A notification occurrence, status, and reference are recorded.

When this action is unavailable:

- Finished submission
- No phone registration requirement
- No candidate phone number

## Verify a reminder

After sending a reminder, confirm that the action completed as expected.

1. Check History for the reminder event and status.
2. Verify the notification medium, type, and status.
3. Confirm the candidate contact data was correct.
4. Check for failed or unavailable notification status.

## Copy candidate link

The candidate link action builds a drawer URL for the selected submission. Copying the link does not change candidate or submission data.

The copied link includes:

- Current origin
- Journey ID
- Candidate or submission drawer route

Before copying the link:

- Confirm the candidate is the intended person
- Confirm the recipient is authorized
- Treat the link as confidential

## Open in NxtMatch

This action is available only when the submission can be matched safely to a NxtMatch candidate.

- Submission is not deleted

1. Select the NxtMatch icon or action.
2. The browser opens the candidate in the configured NxtMatch base URL.
3. Verify the candidate ID and context.

If the action is unavailable:

- Candidate may not be validated yet
- Candidate may not exist
- Submission may be deleted

Reminder actions use candidate email or phone data together with journey reminder templates and create notification history or occurrences.

#  Reference

## Reminder consequences

- Trigger external communication
- Use candidate email or phone data and journey reminder templates
- Create notification history and occurrences
- May expose candidate contact data

## Access and confidentiality

- Authorized NxtForm access is required
- Valid candidate contact data is required
- Appropriate tenant and user permissions are required
- Links and exported contact information must be handled safely

Do not share candidate links, reminders, or NxtMatch routes with unauthorized people.

## Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Remind by mail | Sends configured reminder email | Use when journey and email requirements allow |
| Remind by SMS | Sends configured reminder SMS | Use when journey and phone requirements allow |
| Disabled reminder | Reminder unavailable because of state or data | Read the reason and correct the prerequisite |
| Copy candidate link | Copies internal submission drawer URL | Share only with authorized users |
| Open in NxtMatch | Opens matched candidate in NxtMatch | Review external candidate when available |
| Notification history | Email or SMS occurrence and status record | Verify reminder delivery context |

## Related articles

- [Candidate drawer](Candidate%20Drawer%20%285%29.md)
- [Status and validation](Results%20Status%20and%20Validation%20%286%29.md)
- [Bulk actions](Bulk%20Selection%20and%20Bulk%20Actions%20%288%29.md)
- [Troubleshooting](Results%20Troubleshooting%20%2811%29.md)
