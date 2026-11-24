# Save, Validate, and Preview Changes \(9\)

Use this guide to understand how changes are saved in Journeys, how to validate them before moving on, and where to verify the candidate-facing result in Preview. Add screenshots in the marked locations to make each action easy to follow.

Important: Journeys uses a mix of immediate saves, field-specific API patches, and debounce saves. Wait for save feedback before navigating away, reordering content, or opening Preview.

# Instructions

## Confirmed save behavior

The Modify experience combines explicit save actions with automatic field-level updates. If a field save fails, the interface reloads the saved server value so the screen does not continue showing a false local state.

| Change | Save behavior |
| --- | --- |
| Step name | Patched for the active language immediately or when the field update completes |
| Module title | Debounce saves after approximately 500 ms of inactivity |
| Module description or content | Debounce saves after approximately 500 ms of inactivity |
| Choice text or content | Field-specific debounce or API patch |
| Choice correct state | Patched immediately through choice correctness logic |
| Choice tags | Create, update, and remove actions use tag APIs |
| Choice additional text | Patched as an additional-text setting |
| Step or module sequence | Patched after reorder |
| Step settings | Patched immediately per setting |
| Images, video, or PDF | Uses media-specific add and delete APIs |

**Screenshot placeholder:** Insert a screenshot of the Modify interface showing an edited field and visible save feedback.

## Unsaved-change precautions

- Do not close the page or navigate away while typing in a debounced field.
- Do not reorder steps or modules while an edited field is still pending save.
- Use Preview only after save feedback appears.
- Resolve anomaly and validation warnings before continuing.

If you move away too quickly, you may lose edits that were still waiting on a debounce save or API response.

**Screenshot placeholder:** Insert a screenshot of a pending or unsaved state, validation warning, or anomaly indicator.

## Validate a change

1. Review the active language.
2. Confirm the journey version and the selected step or module.
3. Review required fields and any validation messages.
4. Confirm the choice and correct-answer state.
5. Confirm media, tags, score, and property mappings.
6. Open Preview.
7. Move through the candidate-facing flow.
8. Verify the saved result is visible.

**Screenshot placeholder:** Insert a screenshot of the editor with the correct journey, step, module, and language selected.

## What happens after saving

Depending on the journey state, a saved change may have different effects.

- It may update the draft or editable journey immediately.
- It may require a review or publish step.
- It may affect the existing candidate experience or active journey behavior.
- It may update a template-linked child journey only when reset or push rules apply.

## Verify with Preview

1. Select the Preview control for the step or question, or open the Preview tab.
2. Confirm the correct journey, step, page, module, language, and version.
3. Enter test values only in a safe environment.
4. Use forward and back navigation if it is supported.
5. Verify required fields, choices, media, score, and routing.
6. Leave test submissions only in the intended test context.

**Screenshot placeholder:** Insert a screenshot of the Preview control or Preview tab.

**Screenshot placeholder:** Insert a screenshot of the candidate-facing Preview view showing the saved change.

## Practical notes

- Preview is for verifying the user experience, not for live operational data entry.
- Saving and publishing are separate actions in some journey states.
- A live journey may have warnings or restrictions that affect saving.

## Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Save feedback | Confirms or rejects a field or API change | Wait for the result before navigating away |
| Validation message | Explains missing or invalid configuration | Correct the indicated field |
| Anomaly | A detected journey or module configuration problem | Open and resolve the highlighted item |
| Unsaved or pending state | A debounce or API save is still in progress | Finish typing and wait for feedback |
| Preview control | Opens candidate-facing verification | Review layout, navigation, and interaction |
| Save, Update, Apply, or Publish | The live action used to confirm the change | Use only the exact action shown for that journey state |

## Related articles

- [Modify interface](Understanding%20the%20Modify%20Interface%20%282%29.md)
- [Manage steps](Manage%20Steps%20%285%29.md)
- [Questions and modules](Add%20and%20Configure%20Questions%20%286%29.md)
- [Preview](../03-preview/Preview%20%281%29.md)
