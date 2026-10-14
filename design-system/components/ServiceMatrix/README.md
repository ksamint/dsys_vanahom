# ServiceMatrix

A comparison grid: hongtu-red column heads, red-wash row heads, `cell` grey content cells, 8px gaps instead of rules.

**Consumer provides:** column titles (business lines or audiences), row labels (服务内容, 核心价值, 痛点与挑战, 选择我们…), and cell text or short lists.

- Up to 4 columns. Text centred, `label` size, ink-soft.
- The red header row is the page's red budget; keep other red off the same view.
- Use `table`, `th scope="col"`, `th scope="row"` so it reads as a table. On phones wrap it in `<div class="vh-matrix-scroll">` so it scrolls sideways instead of squashing.
