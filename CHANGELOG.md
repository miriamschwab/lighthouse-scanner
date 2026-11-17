# Changelog

## 2.4.0 — 2026-11-17

- Removed: the Angie MCP server (the `angie/` folder and its admin script). The plugin's WordPress Abilities expose the same three tools (get URLs, get history, run scan) to any MCP client, including through the MCP Adapter. The removed script also passed the stored Google API key into admin-page JavaScript; that no longer happens.

## 2.3.12 — 2026-08-10

- Changed: Removed the "Enable write abilities" settings checkbox for the Abilities API. The run-scan ability is now always registered and marked destructive (it consumes external PageSpeed API quota) — confirmation happens via the AI client, not a site-wide toggle.

## 2.3.11 — 2026-08-05

- Security: the inline settings data printed into the admin page is now hardened against breaking out of its script context. Server and request values are sanitized, and several type and unreachable-code issues were fixed. WordPress coding-standards cleanup.

## 2.2.0 — 2026-05-21

- Added: REST API (`lighthouse-scanner/v1`) for AI agent and external tool integration.
- Added: `GET /urls`, `GET /history`, `GET /history/{id}`, `POST /scan`, `DELETE /history` endpoints.

## 2.1.0

- Added: Admin-bar "Scan this page" shortcut — scans the current frontend page with one click.
- Added: Autocomplete post/page search to add URLs to the scan list.

## 2.0.0

- Added: Scan history with up to 20 saved entries and score trend graph.
- Added: Regression alert admin notice fires automatically after plugin or theme updates.
- Added: Copy report for Claude — formatted, AI-ready export of scan results.
- Added: CSV export.
- Added: Setup wizard on first activation (auto-populate vs manual URL list).
- Added: Strategy selector (Mobile / Desktop).

## 1.0.0

- Initial release.
