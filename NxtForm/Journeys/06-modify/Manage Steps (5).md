# Manage Steps \(5\)

Use the step three-dot menu and step settings to add, edit, duplicate, reorder, reset, template, configure, and remove steps.

# Instructions

This guide covers the actions available for journey steps and highlights where behavior depends on permissions, journey editability, or template configuration.

## Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Step name | The label for one journey section | Edit and identify the step |
| Grip handle | Drag control for reordering | Move the step only in an editable journey |
| Three-dot menu | Step-specific actions | Duplicate, template, reset, open settings, or remove |
| Step settings | General behavior and timing configuration | Configure return, confirmation, score, duration, and answer behavior |

## Add a step

Live add-step control and creation modal require screenshot verification.

1. Open **Modify**.
2. Confirm the journey is editable (it is not active).
3. Choose the intended position.
4. Use the available add or create-step control.
5. Enter the step name for the active language.
6. Add the first question or page content.
7. Configure settings if required.
8. Verify the step in the sidebar and Preview.

Adding a step creates a separate step sequence that can contain pages and modules. Verify later routing and dependencies.

## Edit a step name

1. Select the step.
2. Select the step name field in the main editor header.
3. Enter the new name.
4. Leave the field or continue so it patches the active language.
5. Switch language tabs and verify translations.

## Reorder steps

1. Hold the step grip handle.
2. Drag to the intended position.
3. Release and verify the normalized sequence.
4. Verify candidate navigation in Preview.

## Duplicate a step

1. Open the step three-dot menu.
2. Select **Duplicate step**.
3. Wait for success or failure notification.
4. Open the duplicated step.
5. Review titles, modules, choices, settings, scoring, and templates.

## Delete a step

1. Open the step three-dot menu.
2. Select **Remove step**.
3. Read the confirmation warning.
4. Confirm only when the step and its candidate data dependencies are intentional.
5. Verify the journey structure and Preview.

## Save-as-template, reset, and master templates

Actions shown depend on template permissions:

- **Save as template**: create template content from the selected step.
- **Edit step template**: update an existing master template.
- **Push template**: send master-template changes to associated child journeys.
- **Reset step**: restore step content from the template.

Only users with template permissions see all template actions. Reset and push actions can affect associated journeys, so review warnings before confirming.

## Configure step settings

Open **Step settings** from the three-dot menu.

- **Step name**: Edit the name for the active language.
- **Can return**: Controls whether the candidate can return to a prior area. Availability depends on state and configuration.
- **Consultant must confirm**: Adds consultant confirmation behavior. Enabling it also enables end text.
- **End text**: Controls whether end text is shown. It may be disabled or forced by consultant-confirmation behavior.
- **Candidate can edit answers**: Allows candidates to edit answers in supported flows.
- **Has score**: Enables step scoring and exposes score configuration.
- **Maximum duration**: Toggles a step time limit. Enter `HH:MM:SS`; overflow is normalized and the value is stored in milliseconds.
- **Must succeed to proceed**: Requires step success only in the supported scoring context.

Step settings patch immediately. If a save fails, the interface reloads the saved server value.

#  Related articles

- [Navigate steps and pages](Navigate%20Steps%20and%20Pages%20%283%29.md)
- [Edit language content](Edit%20Language%20Content%20%284%29.md)
- [Questions and modules](Add%20and%20Configure%20Questions%20%286%29.md)
