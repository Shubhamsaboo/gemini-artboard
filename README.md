# Gemini Artboard - Built for Gemini 3.1 Pro

**Describe a visual, watch it come alive.**

A self-contained creative coding playground. Type a description, and Gemini writes visual code that renders instantly at 60fps. Iterate with follow-up prompts to evolve your creation.

[![Get API Key - AI Studio](https://img.shields.io/badge/Get_API_Key-AI_Studio-34a853?style=for-the-badge&logo=google&logoColor=white)](https://aistudio.google.com/)
[![Get API Key - Vertex AI](https://img.shields.io/badge/Get_API_Key-Vertex_AI-4285f4?style=for-the-badge&logo=googlecloud&logoColor=white)](https://vertexai.google.com/)

![Gemini Artboard](gemini_artboard.png)


## Features

- **Natural language to visuals**: Describe what you want to see, Gemini writes the code
- **Live streaming**: Watch code appear in real-time as Gemini generates it
- **Iterative refinement**: Follow-up prompts modify the running visual
- **Model selector**: Choose between Gemini 2.5 Flash (fast), 2.5 Pro, or 3.1 Pro (deep reasoning)
- **Preset prompts**: One-click chips for particle galaxies, Matrix rain, fractal trees, and more
- **Auto error recovery**: Automatically retries if generated code has syntax errors
- **Save as PNG**: Export your creation
- **60fps animation**: Smooth rendering with FPS counter
- **Zero dependencies**: Single HTML file, no build step, no framework

## Usage

1. Open `index.html` in Chrome or Safari
2. Paste your Gemini API key. Get it at [AI Studio](https://aistudio.google.com/) or [Vertex AI](https://vertexai.google.com/)
3. Select **Gemini 3.1 Pro** from the model dropdown (selected by default)
4. Type a description or click a preset chip
5. Watch it render on the canvas
6. Send follow-up prompts to evolve the visual

## Examples

Try these prompts:

- "An aurora borealis with flowing curtains of green and purple light across a starry sky"
- "A realistic ocean seen from above with caustic light patterns and bioluminescent plankton"
- "A 3D DNA double helix rotating with glowing nucleotide pairs and particle trails"
- "Thousands of fireflies in a dark forest that swarm toward the mouse and scatter when it moves fast"
- "A procedural city skyline at night with rain, flickering windows, and neon reflections on wet streets"
- "A cosmic nebula with swirling gas clouds and stars igniting with gravitational lensing near the mouse"

Then iterate:

- "Add a shooting star every few seconds"
- "Make the colors shift through the spectrum over time"
- "Add a reflection on the bottom half like water"

## How It Works

1. Your prompt is sent to the Gemini API with a system instruction that asks for a `draw()` function
2. The response streams back in real-time (SSE)
3. The generated code is compiled and injected into a 60fps animation loop
4. Follow-up prompts include conversation history so Gemini can modify the running code
5. If the code has errors, it automatically asks Gemini to fix them

## Models

| Model | Speed | Best For |
|-------|-------|----------|
| Gemini 2.5 Flash | ~3-5s | Quick iterations, simple visuals |
| Gemini 2.5 Pro | ~8-15s | Complex code, detailed effects |
| **Gemini 3.1 Pro** ⭐ | ~20-40s | **Deep reasoning, intricate simulations** |

## License

MIT
