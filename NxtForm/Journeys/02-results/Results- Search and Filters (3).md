# Results: Search and Filters \(3\)

Use Results search and filters to narrow the submissions shown in the table. Search and filter selections affect the loaded results and are reflected in the URL query, which makes views easier to revisit or share.

**What to capture in screenshots:** Add screenshots beside the moments where a reader benefits most from visual confirmation: the search field, the more-filters panel, the active-filter summary, and an empty or error state.

#  Instructions

## Search candidates

Use the candidate search field to filter the submission list.

**Screenshot: Candidate search field with example query entered\]**

1. Confirm which candidate field is visible in the table.
2. Enter the candidate name or searchable identifier.
3. Wait for the list to update after typing pauses.
4. Review the result count and active-filter summary.

If no match exists, use **Show all candidates** or clear or reset the active filters.

## Open and apply filters

The more-filters panel requires confirmation before draft filters are applied.

**\[Screenshot: More-filters panel open, showing draft selections before Apply\]**

1. Open the filter panel.
2. Change state, referral, tag, date, or validation values.
3. Review the draft selection.
4. Confirm or apply the changes.
5. Review the active-filter summary.

Applied changes remain associated with the URL query.

## Filter reference

### State filter

The State filter selects submission states that remain after last submission state id filtering. States are loaded from the submission state API, and multiple states can be selected.

Reset can return the state filter to hidden or default source-code selections rather than to a fully unfiltered list.

When interpreting a state:

- State belongs to the submission, not the candidate record alone.
- State color and name come from SubmissionState configuration.
- Manual states can be selected manually.
- Automatic or system states may exist but be disabled for manual changes.

### Referrals

The referrals filter uses referrals associated with the selected journey. Displayed options combine referral code, tenant name, and team name.

Use referral filtering to:

- Locate candidates entering through a referral.
- Compare referral sources.
- Investigate redirected or entry referral activity.

### Tags

Tags come from candidate submission and tag configuration.

- Supports multiple selected tags.
- Uses the journey's available tag options.
- May be absent if no tags are configured.

Tags are candidate or result metadata, not submission-state labels.

### Birthdate

Birthdate filtering uses a from and until date range.

Use it only when:

- Candidate birthdate information exists.
- Dummy or hidden birthdate values should not be interpreted literally.

The date picker limits the latest date to today.

### Started

Started represents the submission creation date range.

Use it to:

- Find candidates who started in a period.
- Investigate campaign or onboarding periods.
- Compare submission volume.

The minimum date is the Journey creation date.

### Last update

Last update represents the submission `updated_at` date range.

Use it to:

- Find candidates recently acted on.
- Identify stale or idle submissions.
- Separate creation time from most recent activity.

### Validation filter

Validation options are **All** and **Only pending**.

**Only pending** means the submission is eligible for validation workflow.

## Active-filter summary and reset

The active-filter summary shows selected filters and counts. It can allow users to clear one condition, clear all filters, or restore broader results.

**\[Screenshot: Active-filter summary showing selected filters and counts\]**

Reset preserves search while clearing many filters, clears referral and tag selections, and resets submission states to configured hidden or default states.

Before resetting:

- Record which filters you applied.
- Confirm whether hidden states are intentionally default.
- Verify that search remains active.

## Empty and error states

If filters match nothing:

- The table offers **Show all candidates**.
- Clearing filters removes the narrower result set.

If loading fails:

- The table shows a load error.
- **Retry** refetches submissions.
- If previous rows exist, loading behavior differs from a first-load failure.

**\[Screenshot: Empty state with Show all candidates action\]**

**\[Screenshot: Error state with Retry action\]**

## Practical scenarios

### Find candidates waiting for validation

1. Open Results.
2. Open more filters.
3. Select **Only pending** in Validation.
4. Apply.
5. Review candidates with the Validate badge.

### Find candidates from a referral

1. Open the referral filter.
2. Select the referral code and team combination.
3. Apply.
4. Open matching rows and review entry referral context.

### Find a candidate updated recently

1. Open the Last update filter.
2. Enter from and until dates.
3. Apply.
4. Review rows and hover over Last activity timestamps.

## Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Search field | Free-text submission search | Enter text and wait for debounce reload |
| State filter | Selected submission states | Select multiple states and apply |
| Referral filter | Selected referral, team, and code context | Narrow submissions to referral relationships |
| Tag filter | Selected candidate tags | Include submissions carrying configured tags |
| Birthdate range | Candidate birthdate range | Select from and until values |
| Started range | Submission creation range | Select from and until dates |
| Last update range | Submission update range | Select from and until dates |
| Validation switch | All or pending-only submissions | Switch validation filtering |
| Apply or confirm | Applies draft filter selections | Confirm a filter change |
| Reset | Restores default states and clears special filters | Return to a broader or default list |

#  Related articles

- [Results overview](Results%20Overview%20and%20Interface%20%282%29.md)
- [Candidate table](Results-%20Candidate%20Table%20%284%29.md)
- [Candidate drawer](Candidate%20Drawer%20%285%29.md)
- [Status and validation](Results%20Status%20and%20Validation%20%286%29.md)
- [Troubleshooting](Results%20Troubleshooting%20%2811%29.md)
