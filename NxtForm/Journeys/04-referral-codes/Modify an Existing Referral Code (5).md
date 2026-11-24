# Modify an Existing Referral Code \(5\)

Modify a referral only after identifying the exact row and confirming whether the referral is shareable. Shareable referrals allow general row editing; non-shareable referrals allow only language and email updates.

Always confirm the correct referral row before editing. Several fields save immediately or through field-specific API patches, so changes may apply as soon as you make them.

#  Instructions

## Open in-row editing

1. Open a journey and select **Referral codes**.
2. Find the referral under **Existing referral codes**.
3. Confirm the **Code**, **Tenant – Team**, **Referral type**, **Language**, and **pool**.
4. Select the edit icon on the right side of the row.
5. Review the inline fields.
6. Change only the intended values.
7. Select the check/done icon to finish in-row editing.

**Screenshot placement:** Add a screenshot after step 1 showing where to find **Referral codes**. Add another after step 4 showing the row in edit mode with the inline fields visible.

Changing supported fields saves immediately or uses field-specific API patches. Wait for validation or save feedback before leaving the row.

## Editable fields for shareable referrals

| Field | Behavior |
| --- | --- |
| Tenant – Team | Changes the journey-team relationship and saves immediately. |
| Email | Uses a debounced save and supports comma-separated valid email values. |
| Referral type | Changes the referral category immediately. |
| Language | Changes the referral language immediately. |
| NxtPlan pool | Lets you search for and select a manageable pool, then updates immediately. |
| Auto-send to NxtPlan | Toggles automatic-send behavior immediately. |

## Editable fields for non-shareable referrals

Non-shareable referrals can update only:

- Language
- Email

They cannot change tenant/team, referral type, or other general shareable fields through the shareable edit rules.

## Edit specific fields

### Edit the tenant/team

Use the **Tenant – Team** selector only when the selected shareable referral is permitted.

Before changing it:

- confirm the row's candidate or submission context
- confirm the journey-team relationship is intended
- confirm the target team's email exists
- verify reporting and ownership implications

The patch reloads team and tenant display information after success.

**Screenshot placement:** Add a screenshot here showing the **Tenant – Team** selector open.

### Edit the email

The editable email value falls back to the team email if the referral has no separate email.

Accepted behavior:

- one or more valid email addresses
- comma-separated values are supported for patch payloads
- invalid email input triggers validation
- an empty field may return to the team email behavior

After editing:

- wait for the debounce save
- correct any invalid-email message
- verify the table display

**Screenshot placement:** Add a screenshot here showing a valid multi-email example and, if useful, a validation message example.

### Change referral type

Changing referral type updates the referral type immediately and refreshes the row display.

Considerations:

- **QR** type enables QR download actions for shareable rows.
- **NxtMatch** is hidden or system-oriented and is not normally intended as a manual shareable channel.
- Channel type can affect reporting and usage context.

### Change language

Changing language updates the language ID and row display immediately.

Confirm that:

- the journey supports the language
- candidate-facing content exists in it
- the referral's expected destination is aligned

### Change NxtPlan pool

Only users with NxtPlan module access can edit or manage pool selection when pool visibility and permissions allow it.

The pool selector searches manageable pools and shows the pool name plus board name.

If the referral has a pool name and ID, or neither value:

- the pool field may be editable
- if only an ID is hidden because of pool permission, a hidden state can be shown

Before saving:

- confirm the pool belongs to the intended NxtPlan context
- confirm the pool is manageable
- verify any existing candidate send rules

**Screenshot placement:** Add a screenshot here showing the pool search dropdown with pool name and board name.

### Change auto-send to NxtPlan

The **Auto-send to NxtPlan** toggle is available during edit mode when pool permissions allow it.

Automatic sending requires:

- an NxtPlan pool ID
- auto-send enabled on the referral
- a candidate sync ID
- the submission to be in the configured **Ready to start** state for the scheduled check

Do not enable auto-send unless the pool configuration and candidate synchronization workflow are intentional.

## Verify the modification

1. Confirm the check/done action completed.
2. Confirm the row display changed.
3. Review tenant/team, email, type, language, pool, and toggle values.
4. Verify candidate links and reporting context.
5. Test only in a safe non-production scenario if sending behavior changed.

**Screenshot placement:** Add a screenshot here showing the saved row after editing.

## What cannot be changed

- non-shareable referrals cannot change team, referral type, or general shareable fields
- shareable field editing can depend on role or admin scope
- pool editing depends on NxtPlan module access and pool management permission
- a team with no email may block tenant/team changes
- existing candidate or submission history is not removed by changing referral configuration

## Troubleshooting

- **Invalid email:** fix comma-separated address formatting.
- **Missing team email:** choose a valid team or restore the team email through the relevant admin or team process.
- **Pool hidden or not found:** verify NxtPlan pool access and pool status.
- **Change not visible:** confirm the row exited edit mode and wait for the API refresh.
- **QR options missing:** confirm a shareable QR referral type and sufficient admin scope.

## Practical notes

- Review the exact row before editing.
- Field patches happen individually, not as one full referral save.
- Use the done/check icon to leave edit mode, but verify that field-specific API calls succeeded.

## Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Edit icon | Opens inline editing for an existing row | Start modification |
| Done/check | Leaves editing mode after field patches | Finish and verify the row |
| Tenant – Team | Shareable referral ownership | Change it if permitted and if the team email exists |
| Email | Direct notification email or team fallback | Enter a valid address or list |
| Referral type | Shareable channel or category | Change to a permitted type |
| Language | Candidate language for the referral | Select a configured journey language |
| NxtPlan pool | Candidate pool destination | Search for and change to a manageable pool |
| Auto-send toggle | Sends eligible submissions automatically | Enable only when the pool and state are intended |

##  Related articles

- [Create a referral](Create%20a%20Referral%20Code%20%283%29.md)
- [Review existing referrals](Review%20Existing%20Referral%20Codes%20%284%29.md)
- [NxtPlan and pool behavior](Referral%20Fields%20and%20Business%20Rules%20%286%29.md)
- [Troubleshooting](Journeys%20Referral%20Troubleshooting%20%287%29.md)
