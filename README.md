# Ai-Forge-
Shenex
## Prompt: Read Aloud Feature

Add a global **Read Aloud** feature to RxShield AI using the browser's built-in
Web Speech API (`speechSynthesis`). Do not use any external or paid
text-to-speech service.

### Requirements
1. Show a "🔊 Read aloud" button in the top navigation bar on every page.
2. Pressing it reads the visible content of the current page aloud, line by line.
3. Pressing it again while speaking stops playback.
4. Use the selected interface language:
   - English: `en-IN`
   - Tamil: `ta-IN`
5. If the browser does not support speech synthesis, or the page has nothing to
   read, show a clear notification instead of failing silently.
6. On the medicine detail page, also provide a separate "Read aloud" button that
   reads only the simple-language explanation.
7. The button must be keyboard accessible and have a descriptive `aria-label`.

### Safety and honesty rules
- Read only text already shown on screen. Do not generate or add new medical advice.
- Do not claim Tamil audio is medically verified. Tamil voice availability depends
  on the user's device and browser.
- Do not send any page content to an external service.

### Acceptance tests
- Pressing the button on the dashboard, schedule, and medicine pages reads that page.
- Pressing it again stops the speech.
- Switching to Tamil changes the speech language.
- In an unsupported browser, a "not supported" message appears.
