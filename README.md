# Storyline 360 QA Tool

Internal tool for QA-checking published Storyline 360 HTML5 courses.

## Usage

1. Open https://storyline-qa-tool.vercel.app
2. Upload a published Storyline 360 **zip** (HTML5 export)
3. Optionally upload the **Translation Export .docx** for TOC matching
4. Click **Run QA Analysis**

## Checks Performed

- Spell check (es/en dictionaries)
- Grammar check (LanguageTool API)
- Paragraph alignment (>2 lines must be left-aligned)
- Missing final period in sentences
- "Cliq" → "click" detection
- English word italic rules (italic in Spanish sentence, plain when standalone)
- Navigation flow mapping
- TOC detection & title matching
- Screenshot quality analysis
- Slide settings (Reset to Initial State)
- Disabled triggers on active objects
- Uninitialized variables at timeline start
- Layer reset settings
- Auto-advance trigger detection
- Risky nav trigger patterns
- Page/slide number detection (must be removed)
- TOC quality (untitled/duplicate slides)
- Image accessibility (alt text)
- Content validation vs Translation Export

## Dependencies

All client-side. Loads dictionaries from `dictionaries/` folder.
