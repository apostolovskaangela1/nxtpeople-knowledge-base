# Journeys: Search and Sorting \(4\)

Use this page to explain how users find Journey records and change their order on the overview. Add screenshots in the marked placeholders to show the search field, sort options, and filtered results.

**Screenshots to add on this page:**

* [ ] Search field in the top-right filter area
* [ ] Example search results after entering text
* [ ] Sort dropdown with available options
* [ ] Example of sorting combined with active filters

# Search

Enter text in the search field at the top-right filter area.

The backend search scope checks:

- Journey ID prefix
- Journey name
- Journey version
- Customer name
- Journey text content

Name, version, and text checks are case-insensitive partial matches. The ID check is a prefix match.

After typing:

1. wait briefly for the debounce
2. page resets to 1
3. active filters remain in effect
4. matching cards reload

To find a Journey by exact name:

- enter the full name or a unique part
- include customer/version context if names overlap
- clear other filters that could hide the result

If exact spelling is uncertain:

- use a unique word from the name
- remove state/type filters temporarily
- include the customer name or ID if known

# Clear search

Clearing the field triggers a new search without a search term.

It does not itself reset sorting or filters.

# Sorting

## Last created

Orders by creation date descending.

Use for:

- new Journeys
- identifying records created recently

## Last edited

Orders by updated date descending.

Use for:

- Journeys recently modified
- follow-up after review/edit activity

The backend sends `sort=-updated_at,id` for this option.

## Amount of submissions

Orders by `finished_submissions_count` descending.

Use for:

- finding the most-used completed Journey volume

The count is of finished submissions, not all started submissions.

# Sorting with filters

Sorting does not clear search or filters.

Changing sort:

- sends the sort field to the backend
- resets page to 1
- keeps type/state/archive/validation selections

Changing search:

- sends the search query
- resets page to 1
- keeps sort/filter selections

# Troubleshooting

If an expected Journey is missing:

- confirm search text is not too narrow
- confirm type/state filters
- confirm archived switch
- confirm validation filter
- confirm page 1
- confirm tenant/team access

If a Journey still does not appear, review whether active filters or access scope are excluding it before assuming the record is missing.

# Elements and meanings

| Element | Meaning | Effect |
| --- | --- | --- |
| Search text | Partial matches across configured Journey fields | Reloads server-filtered list |
| Last created | Descending `created_at` sort | Puts newest Journeys first |
| Last edited | Descending `updated_at` sort | Puts recently changed Journeys first |
| Amount of submissions | Descending finished-submission count | Puts higher completed volume first |
| Page reset | Search/sort interaction reset | Starts returned list at page 1 |

# Related articles

- [Overview interface](Journeys%20Overview%20Interface%20%283%29.md)
- [Filters](Journeys%20Filters%20%285%29.md)
- [Paging](Journeys-%20Cards%2C%20Pagination%2C%20and%20Creation%20%286%29.md)
