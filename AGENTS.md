# Repository Guidelines

## Project Structure & Module Organization

- `index.html` contains the entire Japanese-language site: HTML sections, inline CSS, harvest datasets, and Chart.js configuration. Edit presentation styles in `<style>` and chart behavior in the final `<script>` block.
- `README.md` describes the project, data source, and published GitHub Pages URL.
- There are no separate source, test, or asset directories. Chart.js loads from jsDelivr; no dependencies are vendored locally.

## Build, Test, and Development Commands

- `python3 -m http.server 8000 --bind 127.0.0.1` — serve the repository locally; open `http://127.0.0.1:8000/` to preview changes.
- `git diff --check` — check tracked changes for whitespace errors before committing.
- `git diff -- index.html README.md` — review site and documentation changes together.

No build step, package installation, or automated test command is configured. GitHub Pages serves the static page. Internet access is needed to load the chart library from its CDN.

## Coding Style & Naming Conventions

Use two-space indentation and match the surrounding HTML, CSS, and JavaScript. Keep HTML attributes double-quoted and JavaScript strings single-quoted; use semicolons and `const` for unchanged bindings. Use kebab-case CSS classes and custom properties, such as `.kpi-card` and `--primary-color`, and camelCase JavaScript identifiers or element IDs, such as `harvestChart`. Reuse existing color variables. Preserve Japanese visible text and `lang="ja"`. No formatter or linter is configured; avoid unrelated reformatting.

## Testing Guidelines

No testing framework or coverage threshold exists. After changing the page, preview desktop and narrow mobile widths. Confirm that all four fruit series render, legend toggles work, tooltips show Japanese labels and 千トン units, and the browser console has no errors. Check headings, KPI cards, and explanatory sections for overflow or inconsistent values.

## Data & Content Updates

Keep every fruit array aligned with `years` and use thousands of tonnes consistently. Verify changed statistics against the cited Ministry of Agriculture, Forestry and Fisheries crop statistics. Update chart values, KPI cards, date ranges, source attribution, and README claims together where affected.

## Commit & Pull Request Guidelines

Recent documentation commits use `docs: <short description>`; follow that pattern for documentation changes and use concise, descriptive subjects elsewhere. Keep commits focused. Pull requests should describe the change, record browser checks, link related issues when applicable, and include screenshots for visual changes. Explain the source and calculations for statistical revisions.
