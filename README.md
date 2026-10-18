# Brotherhood Check-In | AppADay 164

A private weekly accountability practice for men's groups and accountability partners. Answer a short set of questions about the week, mark whether you kept last week's commitment, name one concrete step for the week ahead, and copy a summary to share with your brothers. Nothing leaves your phone.

**Live app:** https://augustineiacopelli.github.io/appaday-164-brotherhood-check-in/
**Portfolio:** https://augustineiacopelli.github.io/appaday/

Category S (Spirituality). No AI, no accounts, no network calls.

## Features

**This Week.** One card per question. Each card shows the prompt, last week's commitment with Kept it and Missed it buttons, your answer, and your commitment for next week. Fields save when you leave them, and a Save button sits at the bottom of the tab. The week selector steps back through earlier weeks.

**Patterns.** A dot grid of every question across eight weeks, where a filled dot is kept, a hollow ring is missed, and a dash is not marked. Tap a question to compare weeks side by side (two columns on a phone, four on a wider screen) with a kept rate for the eight weeks shown.

**Summary.** Choose which questions to include, generate a plain text summary, and copy it. Questions marked private (Honesty and Purity by default) start unchecked every time and are never remembered as included, so each week begins private again. When a private answer is included, a warning appears above the text.

**Settings (gear).** Edit, reorder, add, and delete questions, mark any question private, restore the six defaults, export or import a JSON backup (merge or replace), and erase all data. Destructive actions ask for a second tap instead of a pop up.

## Default questions

Prayer, Honesty (private), Purity (private), Work, Family, and Service. They are seed values only and are fully editable.

## Privacy model

Everything is stored in this browser's localStorage under the key `appaday-164-brotherhood`. The app makes no network requests for your data and has no analytics. The only thing shared is the text you choose to copy. Clearing browser data removes your entries, so export a backup from Settings if you want to keep them.

## Data format

```json
{
  "version": 1,
  "questions": [
    { "id": "prayer", "label": "Prayer", "prompt": "...", "sensitive": false, "order": 0 }
  ],
  "weeks": {
    "2026-10-11": {
      "prayer": { "answer": "...", "kept": "yes", "next": "...", "savedAt": 1792297800987 }
    }
  }
}
```

Week keys are the local Sunday that starts the week, so a Saturday night entry lands in the right week regardless of UTC. `kept` is `yes`, `no`, or empty. Deleting a question removes it from the list but keeps its past answers in `weeks`.

## Tech

One self-contained `index.html` with inline CSS and vanilla JavaScript, system fonts, and no dependencies. Designed for a 375px phone screen first with 44px tap targets, and it installs to the home screen with its own icon through the shared AppADay save bar.

Part of [AppADay](https://augustineiacopelli.github.io/appaday/), one complete app every day.
