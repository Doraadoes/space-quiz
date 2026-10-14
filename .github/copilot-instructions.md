# Copilot instructions

## Project structure and architecture

Keep the entire quiz in a single `index.html` file, using plain HTML, CSS, and JavaScript. Do not add external libraries, dependencies, or a server.

The script keeps quiz state (`questionIndex`, `score`, and `answered`) in its closure. `renderQuestion()` builds the current question and answer buttons from the `questions` array; `selectAnswer()` locks in an answer, updates the score and feedback, and enables progression; `showResults()` switches to the results view. The restart handler resets state and renders the first question. Keep changes to the question data and these state transitions consistent with each other.

## Project-specific conventions

- Each question has `question`, `answers`, `correct`, and `fact` fields. `correct` is a zero-based index into that question's `answers`; the quiz length is derived from the array.
- Use `textContent` for dynamic question, answer, fact, and result text.
- Keep the quiz accessible and keyboard-navigable: preserve native buttons, ARIA progress and live feedback, visible focus, focus transfer, and reduced-motion support.
- Respect the user's `prefers-color-scheme` setting. Theme colors use CSS custom properties with light and dark values.
- Make only the requested changes; do not modify unrelated features.

## Build, test, and lint

There are no configured build, test, or lint commands. Test changes in a browser: complete the quiz, check correct and incorrect answers, view results, and restart.
