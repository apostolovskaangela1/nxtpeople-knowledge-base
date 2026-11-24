# Settings Guide \(8\)

This guide explains the right-side settings available for a selected question in Journeys. Use it as a quick reference for media, scoring, tags, required-response behavior, and optional integrations.

Add screenshots at the marked points below to show the exact control location, warning messages, and preview results. This will make the guide easier to follow for new editors.

# Instructions

## Media

The selected question can usually use one media mode at a time. Switching between image, video, and PDF may remove incompatible existing media.

### Add images

1. Open the selected question.
2. Select **Add media/image**.
3. Upload or select the image.
4. Verify the image count and grid columns.
5. Remove incompatible media before switching modes.

For grids, choose 1, 2, or 3 columns if the module supports multiple images.

### Add video

1. Select **Add video**.
2. Enter or configure YouTube or Vimeo content.
3. Verify the language-specific video message if only one language has a video.
4. Remove existing incompatible media or PDF state if needed.

### Add PDF

1. Select **Add PDF**.
2. Upload or configure the PDF.
3. Verify the candidate-facing PDF control.
4. Be aware that switching between image, video, and PDF can remove incompatible existing media.

## Scoring

### Enable scoring

1. Open the selected question.
2. Enable **Has score** if the module supports it.
3. Configure the correct answer or value and score context.
4. Confirm the step score configuration.
5. Verify the result in Preview.

### Knockout question

Enable **Knockout** only when the module supports it and the candidate outcome must block or prevent progression.

If a correct-answer configuration is missing, the editor warns and blocks focus progression until corrected.

Use Knockout only when an incorrect answer should stop the candidate from moving forward.

### Guess correction

Enable guess correction for supported scored questions if guessing should be corrected in the score calculation.

When guess correction is enabled, an obligated or required-answer rule is forced, and negative-score options may appear under it.

### Allow negative score

This setting is available under supported guess-correction logic. Enable it only when negative scoring is an intended outcome.

## Tags

When module or choice tags are enabled:

- Enter a tag in the answer-choice tag field.
- Create or edit an existing tag.
- Clear the field to remove the tag relationship.
- Verify the tag format guidance shown by the interface.

## Additional settings

### New page

For supported modules, enable **New page** to place the question outside its current page context.

It is not shown or applicable in every module position, such as first-position swiper or signature contexts.

### Obligated response

Enable **Obligated** when a candidate must answer the selected module.

This setting may be forced when guess correction is enabled.

### Limit answers

Enable **Limit answers** for supported modules when response count must be constrained.

Review the warning shown if the limit conflicts with existing choices or configuration.

### Send to external package

Enable **Send to external package** only for a compatible configured integration.

Verify tenant, add-on, and callback availability before relying on external delivery.

## Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Image/media | Visual content attached to a module | Upload, replace, or remove |
| Video | YouTube or Vimeo content attached to a module | Configure or remove |
| PDF | Document attached to a module | Upload or remove |
| Has score | Enables module scoring | Configure compatible answer and scoring values |
| Knockout | Treats the answer as a progression-blocking result | Enable only where wrong answers must stop progression |
| Guess correction | Adjusts scoring for guessed answers | Use only with supported scored questions |
| Allow negative score | Enables negative score outcomes | Use with intentional negative scoring rules |
| Obligated | Requires candidate response | Enable when a required answer is intended |
| Limit answers | Restricts response count | Configure and review warnings |
| Send to external package | Sends compatible result data externally | Enable only for configured callbacks or integrations |

## Practical notes

- Media modes are generally exclusive.
- Scoring controls depend on step and question configuration.
- External package delivery depends on tenant and add-on configuration.

#  Related articles

- [Questions and modules](Add%20and%20Configure%20Questions%20%286%29.md)
- [Choices and validation](Choices%2C%20Validation%2C%20and%20Conditional%20Settings%20%287%29.md)
- [Save and Preview](Save%2C%20Validate%2C%20and%20Preview%20Changes%20%289%29.md)
