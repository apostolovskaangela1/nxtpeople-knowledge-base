# Testing and Verifying Changes in Preview \(9\)

Use Preview as a repeatable verification step after Modify changes. This page outlines practical test journeys and shows where to add screenshots so reviewers can quickly validate expected candidate-facing behavior.

**How to use this page:** Follow the relevant scenario, capture evidence in the marked screenshot locations, and compare Preview behavior with the current Modify configuration.

# Instructions

## Scenario 1 — Verify a step name

**Goal:** confirm candidate-visible step name.

1. Change step name in the active language in Modify.
2. Open Preview.
3. Confirm the team and language.
4. Navigate to the step.
5. Compare name and layout.

**If incorrect:**

- Confirm active language.
- Confirm step name save feedback.
- Reopen Preview or reload the preview route.

## Scenario 2 — Verify question order

**Goal:** confirm modules appear in intended order.

1. Reorder in Modify.
2. Open Preview.
3. Enter the first module.
4. Continue one module or page at a time.
5. Compare with the Modify structure.

**If order differs:**

- Verify drag-and-reorder save.
- Reload Preview.

## Scenario 3 — Verify required answer

**Goal:** confirm an obligated field’s live behavior.

1. Configure obligated setting in Modify.
2. Open Preview.
3. Leave the question empty and continue.
4. Record Preview behavior.
5. In an approved live or test submission, verify normal required validation.

Preview may not block empty HTML-required fields because required validation is intentionally disabled for preview mode.

## Scenario 4 — Verify choices

**Goal:** confirm answer labels and correct choice behavior.

1. Edit choices in Modify.
2. Open Preview.
3. Check labels and language.
4. Select valid and invalid options.
5. Continue and return.

Verify scoring and knockout separately in a controlled test submission.

## Scenario 5 — Verify language

**Goal:** confirm all user-facing text in one language.

1. Open team and language Preview.
2. Review step names, questions, choices, media, and end text.
3. Repeat for every configured language.
4. Return to Modify for missing translations.

## Scenario 6 — Verify media

**Goal:** confirm images, video, or PDF presentation.

1. Add or change media in Modify.
2. Open Preview.
3. Check loading and layout.
4. Test on desktop and mobile embedded dimensions.
5. Verify language-specific media if applicable.

## Scenario 7 — Verify conditional behavior

**Goal:** confirm a trigger answer changes the candidate path.

1. Confirm the conditional rule exists in Modify or source evidence.
2. Open Preview.
3. Choose the trigger answer.
4. Continue and confirm affected content.
5. Choose a non-trigger answer.
6. Compare the two paths.

If no conditional engine is confirmed for the Journey, document it as pending live or source verification.

## Scenario 8 — Verify completion

**Goal:** confirm end text and navigation.

1. Open Preview.
2. Move to the end using synthetic test answers.
3. Verify completed text, success text, end button, and external URL.
4. Do not trigger irreversible real integrations.

## Scenario 9 — Verify no unintended submission

**Goal:** confirm Preview remains test-only.

1. Enter synthetic values.
2. Complete a Preview route.
3. Check Results only if approved test monitoring is available.
4. Confirm no real candidate personal data was created.

# Elements and meanings

| Test element | What it verifies | Expected result |
| --- | --- | --- |
| Step name | Active language and step configuration | Correct visible name |
| Module order | Page or sequence configuration | Correct candidate sequence |
| Obligated field | Required-answer setup | Live behavior must be separately verified |
| Choice set | Labels, correctness, and configuration | Correct options and outcome |
| Language | Localization | Correct translated content |
| Media | Image, video, or PDF association | Correct render and layout |
| Conditional path | Trigger and target behavior | Trigger and non-trigger paths differ when configured |
| End screen | Completion text and actions | Correct destination and text |

# Troubleshooting checklist

- Preview opens wrong journey: confirm ID and preview key.
- Wrong step: confirm step, page, or module query parameters.
- Wrong team: choose the correct team preview row.
- Wrong language: choose the correct language menu.
- Missing content: confirm Modify save and active language.
- No navigation: check journey state, module position, and required live validation separately.
- Change not visible: reopen or reload Preview after save feedback.

# Related articles

- [Modify overview](../06-modify/Modify%20%281%29.md)
- [Preview overview](Preview%20Overview%20%282%29.md)
- [Validation](Preview%20Validation%20and%20Conditional%20Behavior%20%286%29.md)
- [Troubleshooting](Preview%20Troubleshooting%20%2810%29.md)
