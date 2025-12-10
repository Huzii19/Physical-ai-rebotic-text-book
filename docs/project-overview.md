---
sidebar_position: 2
---

# Project Overview

This document provides an overview of the "Gemini CLI Book" project structure and its key components.

## Project Directories

*   **`ai-k12-paper/`**: Contains resources related to the AI-K12 research paper.
    *   `paper.md`: The main content of the research paper.
    *   `sources/references.bib`: Bibliography for the research paper.

*   **`my-website/`**: This directory hosts the Docusaurus-based documentation website.
    *   `docs/`: Markdown files that make up the main documentation sections.
    *   `blog/`: Markdown files for blog posts.
    *   `src/`: Contains React components and styling for the website.
    *   `docusaurus.config.ts`: Configuration file for the Docusaurus site.
    *   `sidebars.ts`: Defines the structure and order of the documentation sidebars.

*   **`specs/`**: This directory contains specifications and plans for various features and modules within the project. Each subdirectory under `specs/` corresponds to a specific feature or module.
    *   `001-ros2-tutorial/`: Specifications for the ROS2 tutorial module.
    *   `002-ai-k12-paper/`: Specifications for the AI-K12 paper generation and management.

*   **`.gemini/`**: Contains configuration and scripts specific to the Gemini CLI agent.

*   **`.specify/`**: Contains templates and scripts used for spec-driven development.

*   **`history/prompts/`**: Stores prompt history records, documenting interactions with the Gemini CLI agent.
