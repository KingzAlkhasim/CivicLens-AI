# TASK-01: Chat screen

**Estimate:** 2-3 hours. **Branch:** `feat/task-01-chat-screen`. **Files:** `frontend/src/` only.

## Goal
A simple, mobile-first screen where a user types a question and sees a reply bubble.
Use the data in `/mock/ask.answered.json` (import it) as the "reply". No real server yet.

## Build
1. `ChatScreen` component: message list + text input + Send button.
2. When Send is pressed: show the user's message, a "Thinking..." state for ~1 second, then show the mock answer text.
3. Empty state: friendly hint text when there are no messages.
4. Input clears after sending, Send is disabled when the input is empty.

## Acceptance criteria
- [ ] Looks good at 375px wide (phone) and on desktop
- [ ] Text is large enough to read (min 16px) and buttons are easy to tap (min 44px)
- [ ] Loading state is visible
- [ ] `npm run build` and `npm run lint` pass
- [ ] Screenshot of the screen on a phone-width window in the PR

## Not in this task
Citations, language switching, audio, review page. Those are later tasks. Do not call any real API.

## Hint
Keep it simple: one component, `useState` for messages. Ask the maintainer if stuck for more than 1 hour.
