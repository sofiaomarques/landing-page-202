# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Fan-made, non-commercial landing page for an imaginary Tame Impala tour in Brazil. All page copy is in Brazilian Portuguese (`lang="pt-BR"`); English song-lyric phrases are wrapped in `<span lang="en">`. The README is written in Portuguese with subtle Tame Impala song references woven into the prose — keep that tone when editing it.

Everything lives in `index.html` (inline CSS and JS, no build, no tests). Run it with `open index.html`.

## Rules for `index.html`

- **Progressive enhancement:** a `<head>` script adds the `js` class to `<html>`, and hidden/animated states are only applied under `.js ...` selectors so content stays visible without JS. Gate new animated content the same way.
- **Reduced motion:** every new animation must be disabled under `@media (prefers-reduced-motion:reduce)`.
- **Timeline:** the zigzag thread and the hourglass are drawn from the measured positions of the `.tl-node` spheres. Call `onTimelineChange()` after anything that changes the timeline's layout.

## Content constraints

- Must stay clearly a fan concept: no ticket sales, no official affiliation claims, fictional dates/venues, and no official album covers or band imagery — all art is original SVG/CSS.
- When adding or renaming sections, update both the nav links and the README's "What's inside" list.
