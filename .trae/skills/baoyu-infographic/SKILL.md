---
name: "baoyu-infographic"
description: "Generates professional infographics with various layouts and styles. Invoke when user asks to create an infographic, visual summary, or data visualization based on text content."
---

# Baoyu Infographic Generator

This skill converts textual content or markdown into professional infographics using the methodology from the `baoyu-skills` project.

## How to use

When the user requests an infographic, follow these steps:

1. **Analyze the input content**: Read the provided text or markdown file.
2. **Determine the best Layout**:
   Choose one of the following layouts based on the information structure:
   - `bridge`: Problem-solution, gap-crossing
   - `circular-flow`: Cycles, recurring processes
   - `comparison-table`: Multi-factor comparisons
   - `do-dont`: Correct vs incorrect practices
   - `equation`: Formula breakdown, input-output
   - `feature-list`: Product features, bullet points
   - `fishbone`: Root cause analysis
   - `funnel`: Conversion processes, filtering
   - `grid-cards`: Multiple topics, overview
   - `iceberg`: Surface vs hidden aspects
   - `journey-path`: Customer journey, milestones
   - `layers-stack`: Technology stack, layers
   - `mind-map`: Brainstorming, idea mapping
   - `nested-circles`: Levels of influence, scope
   - `priority-quadrants`: Eisenhower matrix, 2x2
   - `pyramid`: Hierarchy, Maslow's needs
   - `scale-balance`: Pros vs cons, weighing
   - `timeline-horizontal`: History, chronological events
   - `tree-hierarchy`: Org charts, taxonomy
   - `venn`: Overlapping concepts

3. **Determine the best Style**:
   Default to `craft-handmade` unless specified. Other options include: `technical-schematic`, `corporate-memphis`, `blueprint`, etc.

4. **Determine Aspect Ratio**:
   - `landscape` (16:9)
   - `portrait` (9:16)
   - `square` (1:1)

5. **Generate the Prompt**:
   Create a detailed visual prompt describing the layout, specific data/labels, visual relationships, semantic colors, style characteristics, and aspect ratio.

6. **Create SVG/HTML or use external tools**:
   Since Trae cannot directly call the Claude Code CLI plugin, you should either:
   - Generate Mermaid/PlantUML code representing the infographic.
   - Generate an SVG or HTML file with CSS to render the infographic locally.
   - If an image generation tool/API is available in the workspace, use the generated prompt to call it.
