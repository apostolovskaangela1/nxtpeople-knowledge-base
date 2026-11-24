# Journeys: Open a Journey and Workspace Navigation \(7\)

Use this guide to open a Journey from the overview, understand the breadcrumb behavior, and navigate the main workspace tabs. Add screenshots in the marked locations to make each step easier to follow.

#  Instructions

## Open a Journey

1. Confirm the Journey name, customer, state, language, version, and submission count on the overview card.
2. Select the complete card.
3. The Journey opens through the `/journey/:journeyId` detail route.
4. Confirm the breadcrumb is updated to **Journeys → selected Journey**.
5. Select the required tab.

## Breadcrumb behavior

The Journey detail sets the breadcrumb as follows:

- Journeys
- selected Journey name

The Journey name uses the active language, first loaded name, or loading text fallback.

## Workspace tabs

### Results

Reviews candidate submissions, candidate status, answers, history, notes, referrals, reminders, validation, export, and deletion.

Use [**Results**](../02-results/Results%20%281%29.md) after candidates are in the Journey.

### Modify

Changes Journey structure and content.

Content editing is generally available in **Draft** and **Waiting for approval** states. Ongoing, ongoing-but-hidden, and finished restrictions apply.

Use [**Modify**](../06-modify/Modify%20%281%29.md) for steps, pages, questions, settings, media, and scoring.

### Preview

Shows candidate-facing Journey content for a selected team and language.

Use [**Preview**](../03-preview/Preview%20%281%29.md) to verify modifications before or during preparation.

### Referral Codes

Creates and manages referral entries associated with the Journey.

[Referral creation](../04-referral-codes/Referral%20Codes%20%281%29.md) is generally available only for ongoing or ongoing-but-hidden journeys and permitted users.

## Header actions

Where visible, the header may include:

- approval actions
- Export, for admin scope
- Duplicate
- History
- Settings

See Icons and header actions.

## Navigating back

Use the breadcrumb **Journeys** entry or browser navigation to return to the overview.

When the overview reopens, initialization clears the selected Journey and Journey language from store state.

## Practical troubleshooting

If the wrong Journey opens, check the basics before troubleshooting deeper navigation behavior.

If the wrong Journey opens:

- confirm the card name and customer
- confirm active state and language
- verify tenant and team permissions
- open one level deeper and compare the Journey detail header and breadcrumb

If a tab is missing:

- verify role or tab permission
- verify Journey state
- verify tenant or team scope

## Elements and meanings

| Element | Meaning | Effect |
| --- | --- | --- |
| Card link | Opens Journey detail route | Selects Journey context |
| Breadcrumb | Journey navigation path (side menu) | Identifies current Journey |
| Results tab | Submission review workspace | Opens candidate and submission activity |
| Modify tab | Journey structure editor | Opens when state permits editing |
| Preview tab | Candidate-facing test view | Opens team and language Preview |
| Referral Codes tab | Journey referral management | Creates and edits referral entries |

## Related articles

- [Overview interface](Journeys%20Overview%20Interface%20%283%29.md)
- [Cards and creation](Journeys-%20Cards%2C%20Pagination%2C%20and%20Creation%20%286%29.md)
- [Results](../02-results/Results%20%281%29.md)
- [Modify](../06-modify/Modify%20%281%29.md)
- [Preview](../03-preview/Preview%20%281%29.md)
- [Referral Codes](../04-referral-codes/Referral%20Codes%20%281%29.md)
