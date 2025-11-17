# Copilot / AI Agent Instructions for this repository

This repository is a Jekyll-based website (GitHub Pages) for the "Professional Practice" site. The goal of these instructions is to give an AI coding agent the immediate, actionable context needed to be productive.

Quick summary

- **What this is**: A static site built with Jekyll. Source content lives in markdown and YAML files; the generated site is in `_site/`.
- **Primary build**: `bundle exec jekyll build` (root `package.json` exposes `npm run build` which runs `bundle exec jekyll build`).
- **Local preview**: run Jekyll serve (see examples below).

Quick start (commands)

- Install Ruby and Bundler, then: `bundle install` (the repo already vendors `vendor/bundle/` but running `bundle install` is recommended when Ruby versions change).
- Build site: `bundle exec jekyll build` or `npm run build`.
- Serve locally: `bundle exec jekyll serve --port 4002` (the site `port` is configured in `_config.yml`).
- Deploy: `npm run deploy` or `npm run build-n-deploy` — deployment uses `rsync` as configured in `package.json` (`deploy:site`).

Key files & directories (what to edit)

- `index.md`: front page (root editable page).
- `_config.yml`: Jekyll configuration (permalink, url, port, plugins). The repo sets `permalink: /:title/` — filenames and titles affect final URLs.
- `_posts/`: chronological blog/posts content output by Jekyll.
- `_layouts/`, `_includes/`: Liquid templates and partials used across pages.
- `_data/`: YAML/CSV used to generate lists and data-driven pages (e.g. `course-info.yml`, `employers.csv`, `portfolioreviews.yml`).
- `css/` and `_site/css/`: site styles; the source is `css/styles.css`.
- `vendor/bundle/`: vendored gems. This is currently present in the repo — avoid manual edits unless you intentionally update gems.
- `_site/`: build output — do not edit generated files here; commit only source files.

Project-specific patterns and conventions

- Permalinks: `_config.yml` sets `permalink: /:title/`. New pages should include `title` in front matter to ensure the expected URL.
- Data-driven pages: Templates read `_data/*.yml` and `_data/*.csv`; to update lists (e.g., employers or course info) update the corresponding file in `_data/`.
- Posts: Use the Jekyll naming convention `YYYY-MM-DD-title.md` in `_posts/` to create a post.
- Vendor bundling: The repository includes a `vendor/bundle/` directory — this means CI or local runs may not require a fresh `bundle install`, but when updating gems use Bundler and update `Gemfile`.

Build & deploy specifics

- `package.json` scripts (root):
  - `build-site`: `bundle exec jekyll build`
  - `build-n-deploy`: runs `build` then `deploy` (which uses rsync to `keycdn:fieldwork/`).
- Deployment uses `rsync` configured in `package.json`; verify `deploy:site` target and SSH/remote access before running.

What not to change

- Do not edit files in `_site/` — they are generated.
- Avoid changing `vendor/bundle/` unless you intentionally update Ruby gems. If you update gems, run `bundle install` and test a local build.

Examples (common tasks)

- Edit homepage: modify `index.md` and run `bundle exec jekyll build` to preview.
- Add a new page: create a markdown file at repository root or a subfolder with YAML front matter (`---\ntitle: "My Page"\n---`).
- Add a course or employer entry: update the appropriate file in `_data/` and the site templates will render it on next build.

Where to look for patterns

- Look at `_layouts/default.html` and `_includes/aside.html` to see how templates render data and pages.
- See `_data/portfolioreviews.yml` and the `_posts/` pages for examples of content structure and front matter fields.

If you need clarification

- Ask for the specific task (edit, add page, update data). Point to the target file(s) and I'll propose exact changes and a small test plan.

— End of instructions —
