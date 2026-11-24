# Journeys Overview Interface \(3\)

This page describes the Journeys overview screen and includes clearly marked placeholders for screenshots to be added during visual documentation.

# Purpose

The Journeys overview is a list-and-navigation screen. It helps users locate Journey records and move into a selected Journey. It does not directly edit a selected Journey.

# Suggested screenshots

* [ ] **Screenshot 1:** Full overview page with the major areas labeled
* [ ] **Screenshot 2:** Search field in use with visible results
* [ ] **Screenshot 3:** Sort selector options expanded
* [ ] **Screenshot 4:** More-filters panel expanded
* [ ] **Screenshot 5:** Journey grid showing cards and paging footer
* [ ] **Screenshot 6:** Floating plus button visible for a user with create permission

# Page areas

| Area | Purpose |
| --- | --- |
| Left navigation | Opens Journeys and the main product areas |
| Search field | Searches Journey name, ID, version, customer name, and text content |
| Sort selector | Requests a server-side ordering |
| More-filters panel | Selects Journey type, state, archive, and validation filters |
| Journey grid | Displays paged Journey cards |
| Paging footer | Moves among 48-record UI pages |
| Floating plus | Opens creation when permitted |

# Screenshot placeholders

# Search field

The search field sends `filter[search]` to the backend.

**Screenshot placement:** Add a search example showing a typed query and the resulting filtered grid.

Confirmed search scope:

- Journey ID prefix
- Journey name, case-insensitive partial match
- version, case-insensitive partial match
- customer name
- Journey text content

Search is debounced for approximately 500 ms.

Behavior:

- page resets to 1
- active sort and filters remain in effect
- clearing the field searches with no search term
- empty results show a no-results message

Search is case-insensitive for supported text fields in the backend scope.

# Sort selector

Sorting is server-side.

**Screenshot placement:** Add an image of the open sort menu with all options visible.

| Option | Direction |
| --- | --- |
| Last created | descending |
| Last edited | descending |
| Amount of submissions | descending |

Changing sort resets page to 1. Filters and search remain active.

The submission-count sort uses finished submissions count, not all submissions.

# More-filters panel

**Screenshot placement:** Add the expanded filter panel with Journey type, Journey state, Show archived, and Validation switches visible.

The panel includes Journey type, Journey state, Show archived, and Validation switches.

Type and state checkboxes update the filter arrays immediately and trigger a backend request.

Reset restores:

- all configured Journey types
- all configured Journey states
- archived Hidden
- validation All
- existing search remains because the reset implementation does not clear `searchValue`

Reset also does not explicitly reset the sort value.

# Journey grid

**Screenshot placement:** Add a grid image that shows responsive cards and, if available, a separate loading-state image.

The grid is responsive and renders cards in columns with at least 350 px per card.

While loading, it renders 100 loading cards. The page later replaces them with Journey cards or an empty state.

# Paging

**Screenshot placement:** Add an image of the paging footer and a second image if needed showing a later page selected.

The frontend requests 48 records per API call, and the page control uses API total/page metadata.

Changing page:

- updates the URL page query
- preserves search/filter/sort
- clears/refills Journey cards
- scrolls the overview container to the top

# Create button

**Screenshot placement:** Add a screenshot of the floating plus action for a user with create permission. If useful, add a second screenshot of the creation modal entry point.

The plus action appears only if the user has Journey create permission.

It routes to a creation modal. Cancellation returns to the Journey overview route.

# Elements and meanings

| Element | Meaning | Effect |
| --- | --- | --- |
| Search | Text search in Journey fields | Filters server-backed records |
| Sort | Server sort field/direction | Reorders cards and resets page 1 |
| More filters | Type/state/archive/validation controls | Narrows cards |
| Grid card | One Journey summary/navigation link | Opens Journey detail |
| Paging | 48-record page navigation | Loads another server page |
| Create + | New-Journey wizard entry | Creates Draft Journey if permitted |

# Related articles

- [Search and sorting](Journeys-%20Search%20and%20Sorting%20%284%29.md)
- [Filters](Journeys%20Filters%20%285%29.md)
- [Cards and pagination](Journeys-%20Cards%2C%20Pagination%2C%20and%20Creation%20%286%29.md)
- [Create a Journey](Journeys-%20Cards%2C%20Pagination%2C%20and%20Creation%20%286%29.md)
