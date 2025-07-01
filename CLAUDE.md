# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Hugo static site generator blog using the TeXify3 theme, focused on personal writing with sections for Reads, Reflections, and Poetry. The site uses the gruvbox color scheme with LaTeX-style typography and supports math rendering with KaTeX.

## Build Commands

- **Development server**: `hugo server` or `hugo serve -D` (includes drafts)
- **Production build**: `hugo`
- **Clean public directory**: `rm -rf public/`

No package.json scripts are defined, but PostCSS dependencies are available for CSS processing.

## Content Structure

Content is organized into three main sections defined in `hugo.toml`:
- `/reads/` - Book reviews, article summaries, and reading notes
- `/reflections/` - Personal blog posts and thoughts  
- `/poetry/` - Creative writing and poems
- `/drafts/` - Unpublished content

Content files use either TOML (`+++`) or YAML (`---`) front matter. The `draft` parameter controls publication status.

## Theme Architecture

Uses `hugo-texify3` theme as a git submodule in `/themes/`. Key customizations:
- Custom JavaScript in `/static/js/main.js` with GSAP animations
- Comment engine configured (Remark42)
- Math rendering enabled site-wide
- Custom menu structure with SVG icons

## Key Configuration

- Base URL: `https://edwritesmediumform.com`
- Theme: `hugo-texify3` (git submodule)
- Math: Enabled via KaTeX
- Comments: Remark42 integration
- Search: DuckDuckGo search box enabled
- Root font size: 105%

## Development Notes

- Hugo version requirement: 0.115.1+ (currently using 0.144.2)
- Uses PostCSS for CSS processing with autoprefixer
- GSAP CDN loaded for animations
- Custom SCSS files in `/assets/sass/layouts/`
- Generated CSS is fingerprinted and minified
- Public directory contains the built site