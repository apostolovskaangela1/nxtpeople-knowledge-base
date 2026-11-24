# Journeys: Cards, Pagination, and Creation \(6\)

This guide explains how Journey cards work, how pagination behaves in the overview, and how Journey creation starts from the overview. Add screenshots in the marked places to make the flow easier to scan.

#  Instructions

1. Review Journey cards to understand what each visual element means.
2. Use the overview pagination controls to move through results and confirm page behavior.
3. Create a Journey from the floating plus button and verify the redirect and defaults.

**Screenshot placement:** Add screenshots at each Screenshot marker below. Prefer cropped screenshots that show only the relevant UI area.

# Journey cards

The Journey card is the entry point into an individual Journey. It summarizes the most important identifying and status information before a user opens the Journey.

It can display:

- customer or tenant logo/name
- Journey name
- pending-validation count
- finished submissions count
- configured languages
- version
- feedback indicator
- current Journey state
- archived status

## Journey name

The card uses the active consultant locale if available. If not, it falls back to the first language in the card data.

Use the name together with the customer, team, and status to distinguish Journeys with similar names.

## Customer

The customer represents the associated organization or business context for the Journey. This can differ from the tenant or team context shown elsewhere in the product.

## Pending validation count

The orange badge shows the number of submissions waiting for validation that the current user is allowed to see.

This count is based on aggregate submission validation permissions, not only on the Journey state.

## Finished submissions

The users icon and number show `finished_submissions_count`.

This reflects finished submissions only, not all submissions that were started or are still in progress.

## Languages

Each configured language code is shown on the card, for example NL, FR, or EN.

## Version

If a version exists, it is shown after the language area.

## Feedback

An orange comment icon indicates reviewer feedback or comments.

### Feedback and validation

The orange comment icon is the card-level feedback indicator. It is separate from the orange pending-validation badge on the card.

When a candidate submission is awaiting validation, the orange submission or validation indicator opens the **Validate data** workflow.

> Screenshot pending: capture and redact the orange pending-validation indicator on a Journey card together with the live Validate data dialog. The screenshot must show the submitted-data column, candidate match list, Candidate details, Cancel, and Validate controls.

#### What the Validate data dialog is for

The dialog appears when data entered by the candidate matches one or more candidate records already in the system.

It asks the employee to decide which candidate identity the submission concerns:

- select an existing candidate whose data matches
- or choose **New candidate** if the entered person is not one of the listed matches

#### Entered by candidate by form

The left column shows the candidate data entered in the Journey submission.

The displayed fields can include:

- First name
- Surname / last name
- E-mail
- Telephone
- Date of birth
- Official address

These values are copied from the submission and are used for candidate matching.

A missing value is not necessarily an error; it means the submission or registration form did not provide that value.

#### Name

The middle column shows candidate matches already known to the system.

Each match can display:

- candidate name
- matching address or other identifying context

The employee should compare the submitted values with the existing candidate records before selecting.

**New candidate** creates or posts a candidate from the entered submission data instead of linking the submission to an existing match.

#### Candidate

The right column shows the currently selected candidate record and available identity details.

Depending on candidate data, it may show:

- candidate name/initials
- reference
- postal code
- birthplace or birthdate

The details help the employee confirm the correct person before validating.

## Complete the validation workflow

1. Open the Journey and enter Results.
2. Find a submission with the orange pending-validation indicator.
3. Open **Validate data** from the candidate/action area.
4. Review **Entered by candidate by form**.
5. Compare the submitted values with the candidate matches shown under **Name**.
6. Select the correct existing candidate.
7. If no match is correct, select **New candidate**.
8. Review the right-side **Candidate** details.
9. Select **Cancel** to close without validating.
10. Select **Validate** only after confirming the candidate identity.

## What happens after validation

If an existing candidate is selected, the submission's candidate identity/sync ID is updated to that candidate and validation is completed.

If **New candidate** is selected, the submission is posted to create a candidate record and linked to the submission, then validation is completed.

After successful validation:

- the modal closes
- success feedback is shown
- the pending-validation badge/flag is updated
- the candidate drawer/link and NxtMatch availability can change
- the submission leaves pending-validation filtering

## Before validating

Do not validate on name alone if other identity fields conflict.

Compare:

- first name and surname
- email
- telephone
- birthdate
- address/postal code
- existing candidate details

A mismatch may require choosing New candidate or further investigation.

## Safety and privacy

The modal can display personal data.

- Use it only for authorized validation tasks.
- Do not copy or share the entered candidate values.
- Do not select an existing candidate merely because the name is similar.
- Confirm enough identifying information before choosing.

## State badge

The card shows the translated Journey state together with a configured color.

- Draft — grey
- Waiting approval — orange
- Ongoing — green
- Ongoing but hidden — pale green
- Finished — red

## Archived card

If `deleted_at` exists, the card is dimmed and shows an archived message across the bottom.

Archived styling changes visibility, but the card still needs to be interpreted using the same core fields such as name, customer, and state.

# Open a card

The full card behaves as a RouterLink to the Journey detail page.

Before opening a Journey, verify:

1. the name
2. the customer or team context
3. the state
4. the language and version
5. the pending-validation and submission counts

# Pagination

The frontend requests 48 records per page. Although the API default may be 20, the overview explicitly sends 48.

When the page changes:

- the page query updates
- server results reload
- search, filter, and sort are preserved
- the overview scrolls back to the top

Search and sort changes reset the page to 1. Filter changes call the server, and page behavior should be verified for edge cases.

If no records match:

- the grid shows a no-results message
- page controls and totals may not provide a useful next page

# Create a Journey

The floating plus button is visible only when the user has the Journey create scope.

Creation opens `/journey/create` as a modal.

Verified fields:

- Journey name — required
- Client or customer — optional and searchable
- Language — required selection, defaulting to the first returned language

Verified backend defaults:

- state = Draft
- type = Influx
- required registration fields default to email, first name, last name, phone, address, and birthdate
- team = current or default team
- selected language is attached as the Journey language

The backend requires:

- name array
- each name value cannot contain `/`
- language ID
- Journey state and type IDs
- optionally customer, redirect Journey, WhatsApp or share, callback, landing page, registration, and settings fields

After creation:

- the API creates the Journey
- the Journey language is set
- permissions are set for the current user or default team
- the created Journey is returned
- the modal redirects to `/journey/:journeyId/edit-page/step=1/page=1`

Expected result: a newly created Journey opens directly on the first Modify page and should appear in Draft state.

# Creation errors and cancel behavior

The modal disables the Create button while the request is posting.

Confirmed client validation:

- Journey name is required
- customer is nullable

Server-side fields and live wizard behavior still require verification for exact labels, optional choices, and environment-specific defaults.

Cancel resets the name and customer fields and returns to the overview route if a Journey has not yet been created.

After successful creation, the `hide` callback should not return to the overview because `createdJourney` is set.

# Practical checks

* [ ] Confirm create permission is available
* [ ] Confirm the default team is correct
* [ ] Confirm the customer selection
* [ ] Confirm the primary language
* [ ] Confirm the Journey name does not contain `/`
* [ ] Confirm redirect to the first Modify page after creation
* [ ] Confirm the Journey appears with Draft state
* [ ] Confirm the primary language and permissions

# Elements and meanings

| Element | Meaning | Effect |
| --- | --- | --- |
| Card | One Journey summary and navigation record | Opens the detail workspace |
| Customer | Associated customer context | Helps distinguish and identify the Journey |
| Submission count | Finished submissions count | Describes completed volume |
| Pending validation badge | Visible pending-submission workload | Supports validation triage after opening the Journey |
| Page | One server page of 48 UI records | Moves to another result set |
| Create + | Journey creation entry point | Opens the creation modal when permitted |
| Creation language, name, customer | Primary setup values | Defines the initial Journey record |

#  Related articles

- [Overview interface](Journeys%20Overview%20Interface%20%283%29.md)
- [Search and sorting](Journeys-%20Search%20and%20Sorting%20%284%29.md)
- [Filters](Journeys%20Filters%20%285%29.md)
- [Opening and workspace](Journeys-%20Open%20a%20Journey%20and%20Workspace%20Navigation%20%287%29.md)
