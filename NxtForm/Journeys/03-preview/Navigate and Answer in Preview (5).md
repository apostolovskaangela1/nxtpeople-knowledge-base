# Navigate and Answer in Preview \(5\)

Use this guide to verify how a journey behaves in Preview mode. Preview follows the configured candidate journey structure, but it skips normal answer submission and persistence. This makes it useful for checking navigation, layout, labels, and visible controls without treating it as proof of live save or resume behavior.

**Important:** Never use Preview as evidence that live answer saving, resume behavior, required-answer validation, or final submission logic works the same way in production.

#  Instructions

## Start at a position

Preview can begin from different places in a journey:

- step 1 / page 1 / module 1
- a specific step, page, or module selected in Modify
- a query position supplied in the URL

The candidate UI uses the step and module query parameters to set the initial location.

## Move forward

1. Enter or select test values if appropriate.
2. Select **Next**.
3. Verify that the next module, page, or step appears.
4. Continue until the expected end or until validation blocks movement.

In Preview:

- Next calls Preview routing directly
- normal page or module answer posting is skipped
- the candidate UI can still move through the configured structure

## Move backward

The **Previous** control appears unless the route is already at the first step or module position.

In Preview:

- Previous navigates directly without normal answer saving
- page and module positions determine the previous location
- step settings may restrict normal candidate navigation, but Preview route behavior may differ

## Move between pages

A step can contain modules assigned to page sequences.

When navigating a page:

- page controls or Next determine which modules are visible
- page movement may trigger normal save logic outside Preview
- Preview skips answer persistence

## Answer controls

Depending on module type, Preview can display and accept a range of answer controls:

- text and sentence fields accept free text
- number fields accept numeric values
- date fields accept dates
- radio, likert, and swiper choices represent one answer
- checkbox choices can represent multiple answers
- dropdown fields use compatible property and option values
- document, signature, and image controls handle media where implemented

## Required and optional answers

Normal candidate components validate answer obligations in live mode. In Preview, several HTML required states are disabled, so required-answer checks may behave differently.

Use Preview to verify:

- the control is visible
- the expected labels or options appear
- input data can be entered
- the live flow still needs separate validation testing

Preview is good for confirming what the candidate can see and interact with. It is not sufficient for confirming required-field enforcement in live submissions.

## Knockout and scoring

Knockout, score, and candidate success logic can be represented by the Preview UI, but preview step success behavior differs.

- Preview may treat step success as successful for display
- normal submission logic is not created

Use Preview to verify that scoring labels and options appear. Verify real score calculation through a test submission or other source-backed test evidence.

## Completion

When the final step is reached, the candidate UI can route to the journey end page.

Preview end behavior:

- resolves journey success or completion text
- uses the preview journey team for end URL and text
- can show success text, completion text, end button, and WhatsApp or share options
- does not perform normal live submission completion in the same way

## Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Step query | The selected journey step | Start or verify a step |
| Page query | The selected page within a step | Navigate or verify page grouping |
| Module query | The selected question or content block | Start Preview at that location |
| Next | Advances through configured route positions | Continue test navigation |
| Previous | Returns to an earlier module or page | Verify return behavior |
| Answer control | Candidate input or selection element | Enter synthetic test values |

## Practical notes

- Do not treat missing HTML required blocking in Preview as proof that live submissions are not validated.

##  Related articles

- [Preview interface](Understand%20the%20Preview%20Interface%20%284%29.md)
- [Validation and conditional behavior](Preview%20Validation%20and%20Conditional%20Behavior%20%286%29.md)
- [Completion and data safety](Preview%20Data%20Safety%20and%20Completion%20%288%29.md)
