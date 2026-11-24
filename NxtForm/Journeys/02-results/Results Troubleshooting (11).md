# Results Troubleshooting \(11\)

Use these checks before escalating candidate, filter, drawer, reminder, export, or deletion issues.

**Screenshot placement:** Add screenshots in the marked callouts below to show the exact UI state, filters, buttons, warnings, or error messages seen during troubleshooting.

# Common issues and checks

## Candidate does not appear

Check:

- active search text
- selected state filter
- referral/tag filters
- birthdate/started/updated ranges
- validation filter
- page/load completion
- candidate deleted warning

Clear or reset filters and retry loading.

## Search returns no results

Check:

- search spelling
- whether the search applies to available candidate fields
- active filter conflicts
- list loading completion

Use **Show all candidates** only after confirming filters are the reason.

## Unexpected default states

The backend or UI may preselect hidden submission states.

Check:

- state filter values
- reset behavior
- submission state configuration

## Candidate marked deleted

Check:

- soft-delete state
- deletion history or permission
- whether force-delete or soft-delete was used

Normal delete is soft-delete. The candidate or submission may still exist technically or in external systems.

## Awaiting validation

Check:

- candidate match candidates
- candidate identity fields
- validation permissions
- automatic validation job outcome

Use the validation modal, not status-only changes.

## Candidate drawer does not open

Check:

- whether the checkbox or row action was clicked instead of the row
- loading or API response
- submission route ID
- candidate fetch error
- active filter changed the submission list

## Answers missing or incomplete

Check:

- candidate steps exist
- submission full data loaded
- journey step or module relation
- answer media or choice content
- language and answer configuration

## History or notes missing

Check:

- submission occurrence API response
- selected submission ID
- note or current occurrence exists
- user or comment permission

## Validation unavailable

Check:

- user validation scope
- candidate identity input
- automatic matching state

## Reminder disabled

### Email

- journey finished
- journey does not require email
- submission has no email

### SMS

- journey finished
- journey does not require phone
- submission has no usable phone

## Bulk action disabled

Check:

- selected candidate eligibility
- deleted state
- candidate sync ID
- referral pool
- validation or NxtPlan permission
- delete scope
- export permission

## Export fails

Check:

- selected submissions
- export language
- browser download blocking
- confidentiality or permissions

## Delete restrictions

Normal delete requires delete permission and authorization.

Check:

- journey or tenant scope
- selected submission
- whether a super-admin or force-delete route is required
- callback or external workflow consequences

## Infinite scrolling does not load

Check:

- current page and last page
- active filter or search
- loading state
- sentinel visibility
- network failure
- existing no-more-results state

# Further technical assistance

Escalate when:

- repeated API or load errors occur
- a deleted submission is expected to be restored
- bulk eligibility reasons conflict with user permission
- reminder notification status is unknown
- validation candidate matching is incorrect
- NxtPlan upstream returns inconsistent errors

**Screenshot:** When escalating, include screenshots of the visible error, the affected candidate or submission state, and any relevant filter or action context.

# Elements and meanings

| Indicator | What it suggests | What to check |
| --- | --- | --- |
| Missing candidate | Search or filter issue, or deleted record | Filters, search, deleted state |
| Validation badge | Candidate identity must be checked | Validation scope and matches |
| Disabled reminder | Missing data or finished journey | Email, phone, finished state |
| Disabled bulk action | Permission or eligibility issue | Candidate pool, validation, deleted state |
| Load error | Network or API failure | Retry, filters, API status |
| No match | Filter or search combination excluded records | Clear or reset filters |
| Deleted row | Soft-delete or force-delete state | Permissions, history, database context |

# Related articles

- [Results overview](Results%20Overview%20and%20Interface%20%282%29.md)
- [Search and filters](Results-%20Search%20and%20Filters%20%283%29.md)
- [Candidate drawer](Candidate%20Drawer%20%285%29.md)
- [Status and validation](Results%20Status%20and%20Validation%20%286%29.md)
- [Bulk actions](Bulk%20Selection%20and%20Bulk%20Actions%20%288%29.md)
