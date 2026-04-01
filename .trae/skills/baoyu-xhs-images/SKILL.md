---
name: "baoyu-xhs-images"
description: "Generates Xiaohongshu (RedNote) style infographic series. Invoke when the user asks to create an XHS post, RedNote images, or a social media carousel from text content."
---

# Baoyu XHS Images Generator

This skill converts textual content or markdown into a Xiaohongshu (RedNote) style infographic series using the methodology from the `baoyu-skills` project. It breaks down content into 1-10 cartoon-style infographics with a specific Style and Layout system.

## How to use

When the user requests a Xiaohongshu-style image series, follow these steps:

1. **Analyze the input content**: Read the provided text or markdown file.
2. **Determine the Style**:
   Styles (visual aesthetics):
   - `cute` (default)
   - `fresh`
   - `warm`
   - `bold`
   - `minimal`
   - `retro`
   - `pop`
   - `notion`
   - `chalkboard`

3. **Determine the Layout**:
   Layouts (information density):
   - `sparse`: 1-2 pts (Best for Covers, quotes)
   - `balanced`: 3-4 pts (Best for Regular content)
   - `dense`: 5-8 pts (Best for Knowledge cards, cheat sheets)
   - `list`: 4-7 items (Best for Checklists, rankings)
   - `comparison`: 2 sides (Best for Before/after, pros/cons)
   - `flow`: 3-6 steps (Best for Processes, timelines)

4. **Break down the content**:
   Divide the source text into 1-10 logical pages, matching the chosen Layout density for each page.
   
5. **Generate the output**:
   Since Trae cannot directly call the Claude Code CLI plugin, you should either:
   - Provide a highly detailed Markdown storyboard for the user describing each page's visual elements, text, and layout.
   - Generate an HTML/CSS template mimicking the Xiaohongshu card style, allowing the user to view the result in a browser.
   - If an image generation tool/API is available in the workspace, use it to generate the images.
