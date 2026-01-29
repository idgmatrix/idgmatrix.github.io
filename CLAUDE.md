# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal homepage (`g-matrix`) that showcases experimental WebGL/WebGPU projects and infographics. The site is built with vanilla HTML, CSS, and JavaScript with no build process - it's designed to be opened directly in a browser.

## Repository Structure

- **Static web assets** - All pages are self-contained HTML files with embedded CSS/JS
- **index.html** - Main homepage with a card-style layout that dynamically lists all project files
- **BitNet.html** - Interactive infographic about Microsoft's BitNet 1.58-bit LLM using Tailwind CSS and Chart.js
- **Cavitation Simulation** - WebAudio-based simulation (cavitation.html)
- **Graphics demos** - Various WebGL/WebGPU experiments (`hillstate.html`, `hillstate2018.html`, `webgl3.html`, `sonar_simulator.html`, `WebGPU.html`, `WebGPU2.html`)
- **Assets** - Images (`elements.png`, `brick_wall.jpg`), audio files, and profile picture

## Key Technologies

- **CSS**: Custom styles (not a framework) for the homepage; Tailwind CSS (via CDN) for the BitNet infographic
- **JavaScript**: Vanilla JS for dynamic content generation, WebGL/WebGPU demos, and interactive visualizations
- **Visualization**: Chart.js (via CDN) for data charts in BitNet.html
- **WebGL**: Native WebGL API (not Three.js or other libraries)
- **WebGPU**: Native WebGPU API using WGSL shaders
- **Fonts**: Google Fonts (Noto Sans KR)

## Common Development Tasks

**View the homepage:**
- Open `index.html` directly in any modern web browser

**Add a new project:**
1. Create the HTML file for your project
2. Add the filename to the `htmlFiles` array in `index.html` (around line 103)
3. Add a human-readable name to the `prettify()` function (around line 113)

**Style the homepage:**
- Edit CSS in the `<style>` block of `index.html`
- Main container uses a dark theme with gradient background (`#232526` to `#414345`)
- Links use a gold accent color (`#ffa600`)
- Responsive design for mobile (`max-width: 600px` media query)

**Update BitNet infographic:**
- Uses Tailwind CSS for layout and typography
- Chart.js charts are configured in the script section at the bottom
- Chart colors are defined in the `brilliantBlues` array

## Graphics Demos

Most WebGL/WebGPU demos are self-contained with shaders embedded as script tags or template strings. The demos are experimental/educational in nature and don't follow a unified architecture pattern.