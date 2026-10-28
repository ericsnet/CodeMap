# CodeMap

**[English](./README.md) · [Español](./README.es.md)**

CodeMap is a lightweight dependency explorer for understanding how source files in a project relate to one another.

**[Open the GitHub Pages preview](https://ericsnet.github.io/CodeMap/)**

## What works in the current preview

- Open a project folder in your browser, or load the included demo graph.
- Detect common relative imports and `require` calls in JavaScript/TypeScript, plus basic Python imports.
- Explore a dependency graph and searchable file list.
- Inspect incoming and outgoing relationships for a selected file.
- See simple isolated-file counts and approximate dependency cycles.
- Export the detected graph and file relationships to JSON.

The first preview is a static browser application. It reads files selected by you in the browser and does not upload them to a CodeMap server. It is not yet a full parser or a replacement for language-aware analysis.

## GitHub Pages and local use

### GitHub Pages

Visit **https://ericsnet.github.io/CodeMap/**. Pages is intended as a quick, no-install preview. Use **Load demo** to try the interface without selecting a project, or select a project folder from your device.

A GitHub Pages website cannot silently read arbitrary folders on your computer. You must explicitly select the folder/files through the browser file picker.

### Run locally

1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. Choose **Load demo** or select a project folder.

No package manager, build step, server, or account is required for this preview.

## Current limitations

- Dependency detection is based on source-text patterns, not a complete language parser.
- Relative paths and common file extensions are supported; aliases, package resolution, dynamic imports, generated code, and many Python package layouts may not be resolved.
- Cycle detection is approximate and should be treated as a hint, not a formal architecture audit.
- The graph draws at most 100 files at once for readability; the file list and JSON export include all detected files.
- The Rust analysis engine and a dedicated TypeScript application architecture are future development goals, not yet integrated into this preview.

## Roadmap

1. Improve import resolution and add automated tests.
2. Build a Rust analysis core with a stable graph/report format.
3. Develop a richer TypeScript interface for large repositories.
4. Add entry-point discovery, coupling metrics, and architecture reports.
5. Expand language support and validate cycle detection.

## License

CodeMap is publicly viewable on GitHub but is **not open-source software**. All rights are reserved. Public access does not grant permission to copy, modify, redistribute, or otherwise use this project's contents except as permitted by applicable law or with prior written permission. See [LICENSE](./LICENSE).
