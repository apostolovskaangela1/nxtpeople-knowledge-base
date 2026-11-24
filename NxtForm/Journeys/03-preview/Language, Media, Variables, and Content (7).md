# Language, Media, Variables, and Content \(7\)

Use Preview to verify localized content and the candidate-facing experience, not just navigation. This guide shows what to check and where to add screenshots for a complete visual reference.

**Use Preview for presentation checks.** Confirm language, variables, branding, media, and end-state content as the candidate will see them.

#  Instructions

## Language selection

When opening Preview through the Consultant Preview table:

1. Choose the team.
2. Open the language menu.
3. Select a configured journey language.

The Candidate UI looks for that language and falls back to the first configured journey language if it is not available.

**Verify:**

- titles
- descriptions
- questions
- choices
- end text
- buttons
- variables

## Team and tenant presentation

The preview team determines tenant presentation through the journey-team context.

**Check:**

- tenant or team name
- tenant branding and color scheme
- end URL and end text
- WhatsApp or external references if visible

A preview can work without a normal referral because preview keys live on journey teams.

## Text variables

Candidate text supports variables in some fields.

In Preview:

- candidate first name may display as `John`
- candidate last name may display as `Doe`
- customer or tenant values depend on the loaded journey and team context

Check variables in headings, descriptions, success text, completion text, and buttons.

## Images

For image modules, verify the following:

- the image loads
- single-image versus image-grid layout displays correctly
- the selected grid columns render as expected
- language-specific media appears when configured
- fallback or empty media state is appropriate

Do not use real candidate or customer data in test images.

## Videos

Video modules can use YouTube or Vimeo.

**Check:**

- video URL and configuration
- language-specific video availability
- empty or error state
- page layout around the video

## PDFs

PDF modules show a document viewer or control.

**Check:**

- the PDF opens
- the document title and file association are correct
- the page layout remains usable
- upload or download controls behave only in a safe test context

## Tags

Tags attached to choices or modules can affect reporting and candidate categorization.

Preview can show where tags exist, but operational tag verification belongs in Results or in test submission evidence.

## Practical testing

For each language:

1. open a team and language Preview
2. review text and variables
3. check media
4. move through one full page
5. verify navigation labels
6. verify end text and end button

* [ ] Confirm language selection
* [ ] Confirm variables resolve to expected test values
* [ ] Confirm image, video, and PDF presentation
* [ ] Confirm end-state content and action button

## Troubleshooting

- **Wrong language:** confirm the configured journey languages.
- **Missing text:** confirm the active language has the translated field.
- **Variable shows placeholder name:** Preview may intentionally use `John` and `Doe` test values.
- **Missing image, video, or PDF:** check Modify media association and the active language.
- **Wrong tenant:** confirm the selected preview team and journey-team context.

## Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Language | Active candidate text language | Open, select, and verify translations |
| Variable | Dynamic candidate, customer, or tenant text | Verify the resolved test value |
| Image | Candidate-facing visual content | Verify loading and layout |
| Video | YouTube or Vimeo content | Verify URL, language, and presentation |
| PDF | Candidate document | Verify opening and layout |
| End text/button | Completion copy and action | Verify destination and tenant context |

##  Related articles

- [Open a Preview](Open%20and%20Choose%20a%20Preview%20%283%29.md)
- [Interface](Understand%20the%20Preview%20Interface%20%284%29.md)
- [Validation](Preview%20Validation%20and%20Conditional%20Behavior%20%286%29.md)
- [Troubleshooting](Preview%20Troubleshooting%20%2810%29.md)
