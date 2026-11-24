# Choices, Validation, and Conditional Settings \(7\)

Use this guide to manage answer choices, correctness, tags, additional text, and conditional behavior in choice-based questions. Add screenshots at the marked points to make the steps easier to follow.

Do not publish guessed conditional logic settings. Only document or configure controls that have been verified in the live Modify interface.

# When to use this guide

This page applies to compatible checkbox, radio, likert, text-like, and configured choice questions where answers are used as selectable values.

# Add an answer choice

1. Open a compatible checkbox, radio, likert, text-like, or configured choice question.
2. Select **Add option** beneath the choices.
3. Enter the option text for the active language.
4. Set correct-answer state if supported.
5. Add an image, tag, or additional text if available.
6. Verify the choice in Preview.

The interface limits choices according to the module type’s maximum and minimum number of choices.

# Edit choice text

1. Select the choice text field.
2. Enter or edit text.
3. Wait for the field-specific debounce save.
4. Switch languages and verify translation.

Number choices accept numeric values. Dot and comma separators are handled and normalized before patching.

# Mark a choice correct

Radio, swiper, digital likert, and supported single-correct question types use radio-style correct selection.

Checkbox and configured question types may support one or multiple correct choices depending on module rules.

Never mark a choice correct without verifying the question’s expected scoring or knockout behavior.

Once a correct choice exists:

- other choices are synchronized to incorrect or neutral states according to module configuration
- unchecking the final correct choice makes it neutral, not necessarily wrong

# Add a tag

When tags are enabled:

1. Enter a tag name in the choice tag field.
2. If no tag exists, the tag is created and linked.
3. Editing a tag updates it.
4. Clearing the field removes the tag relationship.

Tag formats follow the NxtPlan/tag guidance shown in the interface.

# Add additional text

When **Text field** is supported:

1. Select the **Text field** option beside the choice.
2. The candidate can enter additional text alongside that choice.
3. Verify the text field in Preview.

# Reorder choices

1. Hold the choice grip handle.
2. Drag to the intended position.
3. Wait for sequence patch and refresh.
4. Verify answer order in Preview.

# Delete a choice

1. Select the trash icon beside the choice.
2. The system checks whether candidate answers already use the choice.
3. If answers exist, read and confirm the deletion warning.
4. If no answers exist, deletion may happen immediately.
5. Verify minimum-choice limits and Preview behavior.

Deleting a choice can affect existing candidate answers, correct-answer state, validation, and reporting.

# Conditional and dependency behavior

Verified source behavior includes candidate-variable validation and text or content anomalies, but a complete conditional-logic UI has not been live-captured.

When conditional controls are visible:

- identify the triggering answer or field
- identify the affected step, page, or module
- confirm whether the target appears, hides, is required, or is changed
- verify the full candidate path in Preview

# Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Choice text | Label shown to the candidate | Add or translate the answer |
| Correct selector | Marks the answer as correct for configured scoring | Select or review correctness |
| Tag | NxtPlan reporting or category value for the choice | Create, edit, or remove |
| Text field | Adds free-text input beside a choice | Enable only where additional information is needed |
| Image | Optional visual attached to a choice | Add or remove only when supported |
| Grip handle | Reorders choices | Drag within enabled list |
| Trash icon | Deletes a choice | Confirm if candidate answers exist |

# Practical notes

- Minimum-choice limits prevent deletion below the configured minimum.
- Template-linked choices may be restricted.
- A deleted choice can affect existing candidate answers.
- Use Preview after every choice, score, or conditional change.

# Related articles

- [Questions and modules](Add%20and%20Configure%20Questions%20%286%29.md)
- [Media and scoring](Settings%20Guide%20%288%29.md)
- [Save and Preview](Save%2C%20Validate%2C%20and%20Preview%20Changes%20%289%29.md)
