---
"y-partyserver": patch
---

Add `callbackOptions.autoSave` (default `true`). With `autoSave: false`, `YServer` doesn't call `onSave` on its debounce timer, so a subclass can schedule saves itself, e.g. from a Durable Object alarm. A pending `setTimeout` keeps a hibernatable Durable Object in memory, so with the debounce a room is billed for the whole time anyone types; an alarm doesn't stop hibernation.
