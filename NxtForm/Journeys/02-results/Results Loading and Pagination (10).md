# Results Loading and Pagination \(10\)

This guide explains how Results loads submissions, updates the list when search or filters change, and behaves during scrolling, selection, and error states.

**Add screenshots:** Insert screenshots in the marked callouts below. Capture the live UI wherever possible so readers can see the loading table, infinite-scroll behavior, empty states, and error handling.

#  Instructions

## Page size

The API loads **25 submissions per request**.

## Search and filter refetch

When search or filters change, Results starts a fresh fetch cycle.

- Page resets to **1**
- Loaded submissions are cleared
- The API request is rebuilt from URL/query filters
- Loading state becomes active

Search uses a **300 ms debounce**.

## Infinite scroll

Results uses a **1-pixel sentinel** near the bottom of the list to trigger loading more content.

When the sentinel becomes visible:

- The next page loads
- Page increases by **1**
- New submissions are appended
- A loading indicator appears when previous rows already exist

## Select all loaded

**Select all loaded** means all submissions currently loaded in the browser list.

It does **not** guarantee selection of every submission across:

- Pages not yet loaded
- Filter-matched pages not yet fetched

Before running bulk actions, verify that the loaded count matches what you intend to act on.

## Loading states

Results distinguishes between initial loading and loading more rows.

| State | Behavior | What the user sees |
| --- | --- | --- |
| Initial loading | First fetch or full refetch is in progress | Table loading state with placeholder or loading rows |
| Loading more | Another page is being fetched after scrolling | Loading-new-rows state while existing rows remain visible |

## No results

There are two distinct empty states:

- **No match:** Filters returned no submissions and the UI offers **Show all candidates**
- **No candidates:** The journey has no submissions in the current context

## Load failure

If loading fails:

- The table shows a load error
- **Retry** is available
- Previous submissions remain only when data had already been loaded

## Filter and query preservation

Filters are reflected in URL query parameters. Preserving filters means:

- Reopening the candidate drawer keeps filter context
- Opening or referring to the previous or next candidate preserves the route query
- Closing returns to the filtered table

## Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Loading table | Initial or subsequent fetch is in progress | Wait or retry |
| Infinite-scroll sentinel | Signal to fetch another page | Continue scrolling |
| Current page | API pagination position | Understand the loaded portion |
| No match | Filters returned no submissions | Clear filters or show all |
| No candidates | Journey has no submissions in the current context | Confirm journey or submission state |
| Retry | Refetch after a loading error | Retry once the network or API is available |

## Practical notes

- Search and filter changes can be combined.
- Infinite scroll only loads if a next page exists.
- Selection should be verified against the loaded count before bulk actions.

#  Related articles

- [Search and filters](Results-%20Search%20and%20Filters%20%283%29.md)
- [Bulk actions](Bulk%20Selection%20and%20Bulk%20Actions%20%288%29.md)
- [Troubleshooting](Results%20Troubleshooting%20%2811%29.md)
