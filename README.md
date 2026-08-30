# U.S. Citizenship Test — Study Web App

A standalone web page — no build tools, no server code, no login required.
Everything (progress, XP, custom questions, your preferred answers, your
"need more practice" list) is saved right on your device using the browser's
local storage.

## What's new in this version

- No login progress auto-saves to your device
- **Add your own custom questions** (Manage → My Questions)
- **Edit any official answer** to a phrasing that's easier for you to
  remember (Manage → Edit Answers) — used in both Writing mode and Learn mode
- **Need More Practice list** — any question you get wrong is automatically
  flagged; get it right once to clear it, or manage it by hand
  (Manage → Practice List). A dedicated card appears on the home screen
  whenever you have flagged questions.

## UI/UX polish — v20

This build includes a visual/UX refinement pass inspired by modern education-app patterns:

- More visual progress tracking and a clearer learning path
- A personalized **Continue learning** action on the Home screen
- Clearer context for the active 100/128-question test and selected state
- Cleaner primary study-mode cards and secondary actions
- A more focused full practice-test CTA with the correct pass threshold shown
- A redesigned Progress screen with mastery visualization and lesson-level status bars
- Manage tabs now use the custom art assets and scroll horizontally on small screens instead of squeezing five tabs across
- Dedicated Test Version / My State art is used during onboarding
- Softer shadows, better focus states, hover/tap feedback, and reduced-motion support

The quiz logic, localStorage data, separate progress for the 100/128 versions, custom questions, preferred answers, state data, and PWA behavior are unchanged.
