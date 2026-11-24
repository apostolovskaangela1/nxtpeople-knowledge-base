# Journeys Overview Troubleshooting \(9\)

Use this guide to identify why a Journey is missing, hidden, incorrectly sorted, or unavailable.

**How to use this page**: Start with the symptom that best matches what you see, then verify the checks in order. Add screenshots in the marked callouts to make the guide easier to follow.

# Troubleshooting scenarios

## Journey cannot be found by search

**Check:**

- Search text is correctly spelled.
- Search covers name, ID prefix, version, customer, and text content.
- Active filters are not hiding the Journey.
- The archived setting is not excluding it.
- Page 1 and the current sort are not obscuring it.
- Permission scope allows the current user to see it.

**Try:**

1. Clear the search.
2. Reset filters.
3. Set **Show archived** to **Visible**.
4. Search again.

## Search returns no records

**Possible causes:**

- Search text is too narrow.
- Type or state filters exclude all matches.
- Validation filter excludes results.
- Tenant or team permission scope excludes the Journey.
- The Journey is archived while archived items are hidden.

Clear one constraint at a time instead of changing every control at once.

## Archived Journey is missing

Set **Show archived** to **Visible**.

Archived means soft-deleted and may still require the right permission or context to open.

## Pending-validation Journey is missing

**Confirm:**

- Validation is set to **Only pending**.
- The current user is allowed to see those submissions.
- The Journey actually has pending validatable submissions.
- No type, state, or search filter excludes it.

## Sort order is unexpected

**Confirm:**

- **Last created** uses `created_at` descending.
- **Last edited** uses `updated_at` descending.
- **Amount of submissions** uses finished submissions count descending.

A card with a similar date or count can appear nearby because of ties or ongoing updates.

## Page is empty after changing filters

**Possible causes:**

- The page number is beyond the filtered total.
- The search and filter combination has no matches.
- A filter reset changed the selected state or type sets.
- Records changed while paginating.

Return to page 1 and reset filters if needed.

## Pagination behaves unexpectedly

**Check:**

- Page size is 48.
- The search, sort, and filter query is preserved.
- Records were added or removed while paging.
- A page may no longer exist after filters change.

Return to page 1 after changing search, sort, or filters.

## Journey card missing information

**Possible missing fields:**

- No customer
- No version
- No languages
- No feedback
- No pending validation count
- No finished submissions

A missing value means the Journey record or included data has no value. It does not necessarily indicate an error.

## Create button missing

**Possible causes:**

- The user lacks Journey create scope.
- The button is hidden by a permission check.
- The route action is not available for the tenant or environment.

The backend also enforces create permission. The UI is not the only control point.

## Creation validation error

**Check:**

- Journey name is required.
- Name values do not contain `/`.
- Client is valid if selected.
- A language is selected.
- An account or default team exists.
- Required backend fields are complete.

Keep the modal open and resolve the displayed field error.

## Creation fails after validation

**Check:**

- API or network response
- Default team, customer, and language validity
- Permission scope
- Server-side state or type IDs
- Duplicate or environment-specific constraints

Do not retry with blind duplicate data until you have ruled out that the Journey was actually created.

## Journey opens in wrong tenant or team context

**Check:**

- Selected card customer or team
- Journey breadcrumb
- Tenant or team permissions
- Journey state and team relationships

If the wrong context is confirmed, return to the Overview and reselect the intended card.

## Loading or API error

**Confirm:**

- Network or API response
- Search or filter request payload
- Tenant permissions
- Page and size values
- Browser or session state

Retry after session or API recovery. Escalate when the API consistently fails with a permission or server error.

# Quick reference

| Issue | Meaning | What to check |
| --- | --- | --- |
| No search result | Search, filter, or permission mismatch | Search, filters, archive setting, and tenant scope |
| Archived missing | Archived visibility is hidden | Set **Show archived** to **Visible** |
| Validation missing | No visible pending submissions or filter mismatch | Validation filter and permissions |
| Wrong sort | Selected server ordering | Sort field and direction |
| Empty page | Page, filter, and result mismatch | Return to page 1 and reset filters |
| Create missing | Create scope unavailable | Permissions and backend create scope |
| Wrong context | Card, tenant, or team mismatch | Card identity and breadcrumb |

# Related articles

- [Search and sorting](Journeys-%20Search%20and%20Sorting%20%284%29.md)
- [Filters](Journeys%20Filters%20%285%29.md)
- [Cards, pagination, and create](Journeys-%20Cards%2C%20Pagination%2C%20and%20Creation%20%286%29.md)
- [Open workspace](Journeys-%20Open%20a%20Journey%20and%20Workspace%20Navigation%20%287%29.md)
