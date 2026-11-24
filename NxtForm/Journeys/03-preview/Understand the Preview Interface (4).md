# Understand the Preview Interface \(4\)

# Journeys: Understand the Preview Interface

Preview uses the Candidate UI inside a dedicated preview route. The visible interface represents the journey rather than the consultant editing controls.

## Preview warning

Preview shows a large repeated **PREVIEW** watermark over the candidate-facing interface.

This indicates:

- the route is in preview mode
- the preview key is active
- candidate-facing test context is being used

## Team/language table

This table is the first screen shown after opening the **View preview** tab. It is not the candidate-facing questionnaire itself.

The table shows:

- tenant color indicator
- tenant/team name
- team email
- embedded Preview eye action
- open-new-tab external-arrow action
- copy-link action

Each team row offers configured Journey languages through action menus.

The screenshot currently showing a Name/E-mail table with no Journey steps or questions is the correct initial Preview state.

## Candidate-facing journey structure

A Journey consists of:

- steps — higher-level sections
- pages — positions within a step
- modules/questions — candidate-facing content or interaction blocks

Preview renders the configured structure for the selected team/language.

## Candidate elements

Depending on module type, Preview can show:

- text or content blocks
- text inputs
- checkboxes
- radio choices
- dropdown choices
- number/date inputs
- likert scales
- swiper choices
- signature controls
- document upload controls
- images
- videos
- PDFs
- navigation buttons
- progress indicators
- required/invalid answer feedback
- end text or final screen

Not every element appears in every journey.

## Navigation elements

Available controls depend on journey configuration:

- Next
- Previous
- step progress/navigation
- page navigation
- finish/submit/end control

The Previous control is hidden at the first step/module context. Live candidate navigation can save answers; Preview navigation skips normal answer posting/persistence.

## Validation elements

A question can show:

- missing required answer message
- invalid format message
- answer limitation message
- knockout indication
- server/store validation feedback

In Preview, HTML required validation is disabled for several question components. That means Preview may permit navigation differently than a normal live submission. Verify server-side and real-candidate behavior separately.

## End screen elements

The candidate end page can show:

- thank-you text
- completed text
- success or failure text
- configured end button
- external end URL
- WhatsApp or share options

Preview resolves end URL and text through the selected preview journey team.

## Synthetic variables

Candidate variables in Preview use test values where implemented:

- first name: John
- last name: Doe

Other variables depend on journey and tenant context.

## Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Preview watermark | Marks the candidate route as Preview | Recognize test mode |
| Step/page | Candidate journey position | Move/verify current location |
| Question/module | Candidate-facing content or answer block | Enter test values or review content |
| Navigation | Moves through pages/steps | Continue/back where permitted |
| Validation feedback | Missing/invalid answer information | Observe normal vs preview validation |
| End screen | Completion/return context | Verify text, button, URL, and share options |

## Practical notes

- [Preview](Open%20and%20Choose%20a%20Preview%20%283%29.md) is candidate-facing; it is not the modify editor.
- The embedded preview and new-tab preview should shot the same journey but at different presentation size/contexts. Read [this](../06-modify/Save%2C%20Validate%2C%20and%20Preview%20Changes%20%289%29.md) for clarification.
- A missing element may indicate [configuration, language, state or routing](Language%2C%20Media%2C%20Variables%2C%20and%20Content%20%287%29.md) - not a broken page.

## Related articles

- [Open and choose a Preview](Open%20and%20Choose%20a%20Preview%20%283%29.md)
- [Navigate and answer ](Navigate%20and%20Answer%20in%20Preview%20%285%29.md)
- [Validation ](../06-modify/Save%2C%20Validate%2C%20and%20Preview%20Changes%20%289%29.md)
- [Media and language](Language%2C%20Media%2C%20Variables%2C%20and%20Content%20%287%29.md)
