# Journeys: Common Overview Workflows \(8\)

This guide combines search, filter, sort, paging, and opening actions into practical first-time-user workflows. Add product screenshots at the marked points to make each flow easier to follow.

**How to use screenshot markers:** Replace each **\[Screenshot\]** note with a real image of the UI state described. Prefer cropped screenshots that highlight the exact control, filter, card state, or result list the reader should recognize.

#  Instructions

## Find a Journey by exact name

1. Open Journeys.
2. Select the search field.
3. Enter the full or distinctive Journey name.
4. Wait for the list to refresh.
5. Open the matching card after confirming customer, state, language, and version.

**\[Screenshot\]** Search field with a Journey name entered and the filtered result cards visible.

## Find a recently created Journey

1. Open Journeys.
2. Select **Last created** in Sort.
3. Confirm page 1.
4. Review the newest cards.
5. Use search if a customer or name is known.

**\[Screenshot\]** Sort control set to **Last created** with the first page of cards shown.

## Find a recently edited Journey

1. Select **Last edited**.
2. Review page 1.
3. Open candidates changed recently.

**\[Screenshot\]** Sort control set to **Last edited** and cards ordered by recent changes.

**Note:** Last edited uses `updated_at`, not submission count or creation date.

## Find a high-volume Journey

1. Select **Amount of submissions**.
2. Review the top cards.
3. Confirm the finished-submission count shown on each card.

**\[Screenshot\]** Sorted cards showing highest finished submission counts first.

**Note:** This sort uses finished submissions count, not all submissions or validation count.

## Combine type and state filters

**Example:** find an ongoing Influx Journey.

1. Open more filters.
2. Select **Influx** under Journey type.
3. Select **Ongoing** under Journey state.
4. Apply the selections by confirming the server list.
5. Review matching cards.

**\[Screenshot\]** Expanded filter panel with **Influx** and **Ongoing** selected.

Unselected types and states are excluded.

## Find pending validation work

1. Open more filters.
2. Select **Only pending** under Validation.
3. Review the cards that have pending validation totals.
4. Open a matching Journey.
5. Enter Results and use the Validation filter if needed.

**\[Screenshot\]** Validation filter set to **Only pending** with matching cards visible.

## Find an archived Journey

1. Open more filters.
2. Switch **Show archived** to **Visible**.
3. Combine state or type filters if needed.
4. Review dimmed cards and archived messages.
5. Open only when the intended record and permission are confirmed.

**\[Screenshot\]** Archived toggle enabled with dimmed archived cards in the results.

## Return to the default overview

1. Open **Reset filters**.
2. Confirm all types and states are restored.
3. Confirm archived is **Hidden** and validation is **All**.
4. Re-enter search if needed.
5. Confirm sort and page if the reset result is unexpectedly different.

**\[Screenshot\]** Default overview state after filter reset.

Reset keeps search in the implementation, so clear it separately if a full reset is intended.

## Navigate through pages

1. Review the page footer.
2. Select another page.
3. Verify search, filters, and sort remain applied.
4. Open the intended card.

**\[Screenshot\]** Pagination controls in the page footer with another page selected.

The Overview requests 48 records per page.

## Create and open a Journey

1. Confirm create permission.
2. Select the plus button.
3. Enter Journey name.
4. Optionally select a customer.
5. Confirm the primary language.
6. Create.
7. Confirm redirect to Modify first step or page.
8. Verify the Journey appears in Overview and has **Draft** state.

**\[Screenshot\]** Create Journey entry point, then the creation form.

**\[Screenshot\]** Newly created Journey opened in Modify/Edit and later visible in Overview with **Draft** state.

## Distinguish similar Journey names

When multiple Journeys have similar names, compare:

- customer
- state
- language list
- version
- finished submissions count
- tenant or team context

**\[Screenshot\]** Two similar cards side by side, with the identifying fields clearly visible.

## Elements and meanings

| Workflow | Meaning | Expected result |
| --- | --- | --- |
| Search by name | Finds matching Journey text | Matching cards |
| Find recently created | Created\_at descending | Newest first |
| Find recently edited | Updated\_at descending | Recently changed first |
| Find high volume | Finished submission count descending | Highest finished volume first |
| Filter pending validation | Journey has accessible pending submissions | Workload-focused cards |
| Find archived | Includes soft-deleted Journeys | Archived or dimmed cards |
| Create Journey | Creates Draft record | Redirect to Modify/Edit page |

##  Related articles

- [Overview interface](Journeys%20Overview%20Interface%20%283%29.md)
- [Search and sorting](Journeys-%20Search%20and%20Sorting%20%284%29.md)
- [Filters](Journeys%20Filters%20%285%29.md)
- [Cards, pagination, and create](Journeys-%20Cards%2C%20Pagination%2C%20and%20Creation%20%286%29.md)
- [Open workspace](Journeys-%20Open%20a%20Journey%20and%20Workspace%20Navigation%20%287%29.md)
