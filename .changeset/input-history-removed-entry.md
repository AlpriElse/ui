---
"@ui-sdk/core": patch
---

`createInputHistory` with `getEntryKey` keeps its place when the entry brought back is removed, like a message deleted while it's shown: ArrowUp goes to the entry before it, ArrowDown to the one after, and ArrowDown past the newest still brings back what was being typed. Before, the next ArrowUp saved the removed entry's text over the draft, so the draft was lost.
