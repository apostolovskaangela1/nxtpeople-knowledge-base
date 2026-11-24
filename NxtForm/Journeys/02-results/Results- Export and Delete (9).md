# Results: Export and Delete \(9\)

Use this guide for the two most sensitive candidate-result operations in Results: exporting PDFs and deleting submissions. Add screenshots at the marked points to make the workflow easier to follow and to help readers verify they are using the correct controls.

#  Instructions

## Export PDF

**Purpose:** Export PDF creates a ZIP package for selected submissions.

**Before exporting**

1. Select only authorized candidates.
2. Confirm no real sensitive data is shared outside approved channels.
3. Confirm export language.
4. Verify selected submissions contain valid candidate information.

1. Select individual candidate rows or use **Select all loaded**.

   **\[Insert screenshot here: Results table with candidate row selection and Select all loaded option\]**
2. Open the **Export PDF** bulk action.

   **\[Insert screenshot here: Bulk actions menu showing Export PDF\]**
3. Choose a journey language.

   **\[Insert screenshot here: Export dialog with language selector\]**
4. Confirm **Export**.
5. Wait for the ZIP download.

   **\[Insert screenshot here: Export confirmation or loading state\]**
6. Verify PDF names and content, then remove or secure the file according to policy.

   **\[Insert screenshot here: Downloaded ZIP or extracted PDF naming example\]**

**Expected result:** The backend downloads a ZIP named with submissions, journey name, and date.

Do not assume one PDF exists for every selected submission. Verify the returned package and the export result.

## Delete submission

**Purpose:** Delete removes a submission from normal Results using soft deletion.

1. Open the row action or select multiple candidates.

   **\[Insert screenshot here: Row action menu or multi-select state with Delete available\]**
2. Choose **Delete**.
3. Read the confirmation count and warning.

   **\[Insert screenshot here: Delete confirmation dialog with count and warning text\]**
4. Confirm only if intended.
5. Verify rows disappear and totals decrease.

   **\[Insert screenshot here: Results table after deletion showing removed rows or updated totals\]**

**Expected result:**

- The submission soft-deletes.
- The submission remains in the database for technical or restore contexts.
- The row no longer appears in normal active Results.
- The active drawer closes if it held a deleted submission.
- Deleted status and history are recorded or logged.
- Callback or job work can be triggered.

Normal UI delete is not a super-admin force-delete.

**What not to assume**

- Deletion is reversible from the normal Results UI.
- Answers or candidate identity are erased.
- Exported PDFs are automatically deleted.
- External callbacks are automatically reversed.

## Security handling

Exported files and deleted-record actions may expose or affect personal information.

Before either action:

- Verify permissions.
- Confirm selected IDs.
- Confirm tenant and context.
- Use synthetic or test data during verification.
- Follow organizational retention and privacy policy.

## Troubleshooting

Check selection, export permission, candidate eligibility, and selected language.

Check loading or error feedback, browser download blocking, network, and server response.

Check admin or journey delete scope and selected submission authorization.

Refresh or clear stale cache, verify soft-delete response, and confirm active filters.

## Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Export language | Language used for exported PDFs | Select the intended journey language |
| ZIP package | Collection of generated candidate PDFs | Download and handle confidentially |
| Delete confirmation | Warning and count before soft deletion | Confirm or cancel |
| Soft-deleted row | Submission hidden from normal active Results | Verify it no longer appears in the active table |
| Callback or job | External follow-up triggered by deletion | Consider downstream effects |

##  Related articles

- [Bulk actions](Bulk%20Selection%20and%20Bulk%20Actions%20%288%29.md)
- [Candidate drawer](Candidate%20Drawer%20%285%29.md)
- [Troubleshooting](Results%20Troubleshooting%20%2811%29.md)
