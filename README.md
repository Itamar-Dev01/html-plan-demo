# Generative UI HTML plan

An interactive example of the `html-plan` method by Thariq Shihipar, applied to the existing Generative UI demo.

This is a plan for a proposed change, not the implemented feature. No live model calls or paid services run here.

## Use

Open `index.html` in any browser, including offline. Expand a numbered claim to see its mockup, code and decisions. Select options, comment, and press **Respond**. Copy the response back to the person reviewing the plan. The page does not send anything; changes are stored in that browser's local storage.

## Project grounding

- Source project: https://github.com/Itamar-Dev01/generative-ui-demo/pull/1
- Source branch: `demo/generative-ui-chat`
- Source commit: `bbdb2dd8f011393105749eafce508d3e63dc949a`
- Proposed feature: a real-model reply path, with runtime validation, retry states and a retained offline mock mode.
- New file paths and code marked `sketch` are proposals, not existing code.
- Existing source excerpts include file paths, line numbers and the source commit.
- The original project was not modified.

## Build

`index.html` is the packed, self-contained output. The editable source is `plan.html`.

```sh
node runtime/pack.mjs plan.html --root ../generative-ui-demo -o index.html
```

The source checkout must use the commit above. One pack warning is expected: the three proposed new paths do not exist yet. The plan shows their sketches, not invented existing code.

## Credits

Runtime copied from the `html-plan` plugin at https://github.com/anthropics/claude-plugins-community, upstream commit recorded in `UPSTREAM.md`. The repository's Apache-2.0 license is included. Changes: example-specific content, viewport metadata, and mobile spacing/touch-target overrides. No private conversations or credentials appear in the page.

## Live example

https://html-plan-demo.vercel.app/

Verified at 1440px, 390px and 320px. Decisions update the Respond export. State changes update the screen mockup. No page errors or horizontal page overflow were found.
