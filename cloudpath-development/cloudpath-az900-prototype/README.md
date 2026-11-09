# CloudPath — AZ-900 Learning Companion (Prototype)

A responsive, browser-based prototype for the AZ-900 hackathon.

## Run it
Open `index.html` in a modern browser. No installation or API keys are required.

## Included
- Dashboard with progress, quiz accuracy and review count
- Three-path learning roadmap with expandable modules and checkable units
- Original sample multiple-choice questions with feedback
- Flashcards with flip interaction
- Prepared-example tutor interface (not a live AI integration)
- Progress saved to local browser storage

## Important
This is a front-end prototype, not yet a full-stack production application. Progress is local to the browser; there is no authentication, cloud database, or live AI connection. The syllabus structure is seeded from the supplied Azure Badge Links outline. One networking unit title is explicitly flagged for verification because it appears misplaced in the outline. Practice questions are original study questions, not real Microsoft exam questions.

## Planned next steps
1. Confirm exact path/module/unit structure from the user's source document.
2. Move syllabus and question data into structured files or Supabase tables.
3. Add unit-specific learning notes, diagrams, flashcards and original questions.
4. Add authentication and persisted progress if needed.
5. Integrate a secure AI tutor through a server-side function.
6. Add tests, accessibility checks, and deployment setup.
