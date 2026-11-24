# Preview Overview \(2\)

Preview shows the journey exactly as a candidate should experience it. It is used to verify content, layout, language, answer controls, navigation, media, validation, and completion before the journey is shared or approved.

# Purpose

Preview exists to let consultants test candidate-facing behavior without relying on Modify alone.

Use Preview to:

- verify step and page order
- test questions and answers
- check required/optional behavior
- verify language and translation
- inspect media, PDFs, and videos
- confirm navigation, scoring, knockout, and return behavior
- identify changes that need correction in Modify

# Start here

1. Open the journey.
2. Select **Preview** from the Journey detail page or select Preview on a question/module.
3. Choose team context and language.
4. Open the preview in the page or as a new browser tab.
5. Move through the journey.
6. Return to Modify for corrections.
7. Open Preview again to verify the correction.

**Screenshot:** Insert a screenshot here showing how to open **Preview** from the Journey detail page.

**Screenshot:** Insert a screenshot here showing question- or module-level Preview access.

# Preview versus Modify and Results

| Area | Purpose | Candidate data |
| --- | --- | --- |
| Modify | Configures the journey structure and content | No submitted-candidate review |
| Preview | Tests the candidate-facing experience | Preview/test behavior, not normal operational submission review |
| Results | Reviews submissions and candidate activity | Real or existing submission records |

# Entry points

Preview can open:

- from the Journey detail Preview tab
- from a selected question/module control
- embedded in the Consultant interface
- in a new browser tab
- via a copied preview link

The question-level entry includes step, page, and module parameters and attempts to start at that location.

**Screenshot:** Insert a screenshot here showing the team table and language options before opening Preview.

**Screenshot:** Insert a screenshot here showing the embedded preview inside the Consultant interface.

**Screenshot:** Insert a screenshot here showing Preview opened in a new browser tab.

# Preview safety

Preview mode is identified by `preview` query parameters and a team-specific preview key.

Source-confirmed behavior:

- Preview uses a unique journey-team preview key.
- Preview keys exist on journey teams even before referrals exist.
- Preview sets the candidate UI to authenticated/preview context.
- Required HTML validation is disabled in Preview for several question components.
- Next navigation skips normal answer persistence in Preview.
- Candidate variables display synthetic test values such as John Doe for first/last name.
- Preview shows a large, repeated **PREVIEW** watermark.

Do not assume Preview is completely harmless. The exact submission/completion behavior in every journey state should be live-verified. Until then, use synthetic data and an approved test environment.

**Screenshot:** Insert a screenshot here showing the visible **PREVIEW** watermark in the candidate view.

# Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Team table | Teams associated with the journey and preview keys | Choose team context |
| Language options | Localized candidate views | Open/copy/embed a language-specific preview |
| Embedded preview | Candidate UI inside the Consultant page | Switch mobile/tablet/desktop dimensions |
| Open new tab | Opens full candidate preview | Test independently |
| Copy preview link | Copies the team/language preview URL | Share only for approved testing |
| Preview watermark | Marks the candidate view as Preview | Recognize that data/navigation is test context |

# Related articles

- [Open and choose a Preview](Open%20and%20Choose%20a%20Preview%20%283%29.md)
- [Interface and candidate structure](Understand%20the%20Preview%20Interface%20%284%29.md)
- [Navigation and answer controls](Navigate%20and%20Answer%20in%20Preview%20%285%29.md)
- [Validation and conditional behavior](Preview%20Validation%20and%20Conditional%20Behavior%20%286%29.md)
- [Media, language, and variables](Language%2C%20Media%2C%20Variables%2C%20and%20Content%20%287%29.md)
- [Completion and data safety](Preview%20Data%20Safety%20and%20Completion%20%288%29.md)
- [Testing scenarios](Testing%20and%20Verifying%20Changes%20in%20Preview%20%289%29.md)
- [Troubleshooting](Preview%20Troubleshooting%20%2810%29.md)
