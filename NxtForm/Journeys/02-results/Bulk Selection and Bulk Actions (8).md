# Bulk Selection and Bulk Actions \(8\)

Bulk actions let users operate on multiple submissions at once from Results. After one or more submissions are selected, a bottom action bar appears with the actions that are available for the current selection.

**Add screenshots throughout this page** to show the key UI states: selection checkboxes, the bottom action bar, disabled action reasons, Send to NxtPlan flow, Export PDF language selection, and the delete confirmation. Suggested placement markers are included below as **Screenshot:** callouts.

#  Instructions

## Select candidates

### Select one

- Use the checkbox in the candidate row.
- Click the checkbox without opening the drawer.

**Screenshot:** Candidate row with a single row checkbox selected.

### Select all loaded

- Use the header checkbox.
- It selects all submissions currently loaded.
- It does not necessarily mean every submission across every page or filter result.

Select all applies to the currently loaded rows only. Verify live behavior before assuming it includes all results across pagination or filtered datasets.

**Screenshot:** Header checkbox selecting all loaded rows in the Results table.

## Selection count

The action bar shows:

- Number of selected results
- Allowed and disabled actions
- Action-specific eligibility reasons

Selection is cleared:

- By the close control
- When leaving or unmounting Results
- According to the source store selection lifecycle

Filter and page changes do not explicitly guarantee selection persistence. Verify live behavior before running bulk operations.

**Screenshot:** Bottom action bar showing selected count and enabled or disabled actions.

## Available bulk actions

The action bar may show:

- Send to NxtPlan Pool
- Export PDF
- Delete

The system checks permissions. It disables actions for the whole or partial selection when not permitted.

**Screenshot:** Action bar with all available bulk actions visible.

## Send to NxtPlan

Send to NxtPlan transfers eligible submissions or candidates to a configured NxtPlan candidate pool.

A submission is eligible only when:

- Candidate exists
- The entry or referral NxtPlan pool exists
- NxtPlan module and pool permissions allow the operation
- Upstream pool and candidate checks succeed

The backend responds with errors for:

- Missing referral pool
- Submission not validated
- Manage-pool permission issues
- Candidate already exists
- Pool not found
- Upstream NxtPlan errors

1. Select only intended candidates.
2. Verify candidate and validation state.
3. Verify the referral pool.
4. Verify NxtPlan manage permission.
5. Review allowed and disabled reasons.

1. Wait for success or error feedback.
2. Verify candidate and pool state in NxtPlan.
3. Review submission history or activity.
4. Do not repeat immediately if an error indicates a duplicate or processing state.

**Screenshot:** Send to NxtPlan action and any eligibility or disabled reason shown to the user.

## Export PDF

Export creates a ZIP containing candidate PDFs and asks for a language.

1. Select submissions.
2. Open Export PDF.
3. Choose the export language.
4. Confirm export.
5. Download or open the returned ZIP.

The export uses selected submission IDs and the selected journey language key.

Handle exported information as confidential candidate data.

**Screenshot:** Export PDF dialog showing language selection and confirmation action.

## Bulk delete

1. Select submissions or open a candidate action.
2. Open Delete.
3. Read the deletion confirmation and count.
4. Confirm only if removal is intended.

Bulk delete:

- Authorizes delete on each submission
- Performs soft deletion
- Dispatches a match callback for deleted submissions
- Removes the rows from the current table
- Decreases the visible total count
- Closes a drawer if its submission was deleted

Deletion from normal Results is a soft delete, not a force delete. Super-admin or force-delete behavior is separate and should not be used from the normal user workflow.

**Screenshot:** Delete confirmation modal showing selected count and destructive confirmation.

## Action eligibility

A bulk action can be unavailable when:

- User lacks journey or tenant permissions
- Candidate is deleted
- Candidate sync ID is missing
- Referral pool is missing
- Candidate is not validated
- NxtPlan pool permission is absent
- Export or delete policy disallows the selected set

The action bar shows disabled reasons instead of silently attempting actions.

**Screenshot:** Disabled bulk action with visible reason text or tooltip.

## Practical verification

After any bulk action:

- Confirm selected count
- Confirm success or error notification
- Refresh or review Results
- Verify History or external system state
- Verify deleted rows and total count
- Verify export language and ZIP contents

## Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Row checkbox | Select one submission | Include it in a bulk operation |
| Select all loaded | Select all currently fetched rows | Bulk-act only on loaded submissions |
| Action bar | Available operations for selected IDs | Run send, export, or delete where allowed |
| Disabled reason | Why an action is unavailable | Correct the prerequisite or exclude the candidate |
| Send to NxtPlan | Sends validated candidate or pool data externally | Use only for eligible submissions |
| Export PDF | Creates a ZIP of selected submissions | Download securely |
| Delete | Soft-deletes selected submissions | Confirm the destructive action |

##  Related articles

- [Candidate table](Results-%20Candidate%20Table%20%284%29.md)
- [Export and delete scenarios](Results-%20Export%20and%20Delete%20%289%29.md)
- [Troubleshooting](Results%20Troubleshooting%20%2811%29.md)
