# Orbit Icons

The official icon pack for [OrbitKanban](https://github.com/ZenPluS/OrbitKanban).

The app downloads `orbit-icons.json` from the default branch and caches it in its portable data folder. It includes a verified offline snapshot. Fork this public repository, customize the pack and add your repository in Settings > Appearance repositories.

## Format

JSON only: `format: "orbitkanban-icons"`, `version: 1`, and `packs: [{ id, name, icons }]`. Each icon is keyed by its semantic name (for example `tasks` or `pin`) and has a `family` and `layers`.

Families: line, blue, violet, teal, amber, rose, green, slate, accent. Layer styles: line, b (back), f (front), r (rounded front), d (detail), ds (detail stroke), s (front stroke), bs (back stroke). An optional numeric layer `width` controls strokes.

Each layer has `shapes: [{ tag, attrs }]`. Allowed tags: path, rect, circle, ellipse, line, polyline, polygon. Allowed attributes: d, points, x, y, x1, y1, x2, y2, cx, cy, r, rx, ry, width, height, stroke-width and fill (none/currentColor/pin only). Coordinates use a 24 x 24 viewport. The app supplies theme colors. Scripts, URLs, CSS, event handlers and external images are forbidden.

Custom packs may override only some names; missing icons fall back to Orbit. Multiple packs can live in one repository. Package IDs and icon names are lowercase kebab-case. All packs must validate before a cached version is replaced.
