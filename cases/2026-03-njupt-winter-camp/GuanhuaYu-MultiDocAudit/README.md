# Global Comparison: Intelligent Multi-Doc Audit & Analysis System

[中文版本](./README_ZH.md)

## Project Overview

This project is an automated document processing pipeline powered by Ollama (Qwen3-Coder:30B). It addresses the challenges of analyzing lengthy texts and performing manual cross-document audits by utilizing sliding window chunking and a multi-stage synthesis logic to generate cohesive summary and comparison reports.

## Activity Information <!-- required -->

- **Competition / Workshop:** 2026 NJUPT Winter Battle
- **Awarded:** Excellence Award

## Environment

- **Base Image:** Basic GPU Environment (aup-learning-cloud)
- **Extra Dependencies:** None

## Quick Start

1. In aup-learning-cloud, select **Basic GPU Environment** and set the Git URL to this repository
2. Navigate to `cases/<activity-folder>/<your-folder>/`
3. Open `main.ipynb`
4. Run all cells from top to bottom

## Technical Highlights

- Cascading Processing Architecture: Implements a "Chunk Analysis -> File Summarization -> Global Comparison" pipeline, effectively bypassing the context window limitations of standard LLMs.
- Intelligent Sliding Window: Utilizes a $15,000$ character chunk size with a $500$ character overlap to maintain semantic continuity across text segments.
- Asynchronous Streaming Interaction: Leverages httpx and ipywidgets for non-blocking UI updates, allowing users to see the model's reasoning(<\Thought>tags)in real-time.
- Deterministic Auditing: Configured with temperature: 0.0 to ensure rigorous, reproducible, and fact-based auditing results suitable for professional reporting.

## Results / Demo

*For each of below texts, press Ctrl+A on the webpage, then copy them into a .txt file for testing.Below are two links to the videos of the test results.*

**demo videos**
- https://youtu.be/0PLYf2nHbMc *Multi‑Doc Audit of Lisa Su (Wikipedia & AMD Site)*
- https://youtu.be/XbgoRW6SBXw *Multi‑Doc Audit of CES News*

**source used**
- https://en.wikipedia.org/wiki/Lisa_Su
- https://www.amd.com/en/corporate/leadership/lisa-su.html
- https://www.amd.com/en/newsroom/press-releases/2025-1-6-amd-announces-expanded-consumer-and-commercial-ai-.html
- https://www.amd.com/en/newsroom/press-releases/2026-1-5-amd-expands-ai-leadership-across-client-graphics-.html

## References

- Model: Qwen3-Coder-30B (via Ollama)
- Libraries: Httpx, IPyWidgets
