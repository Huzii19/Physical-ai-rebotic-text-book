# Data Model: Tutorial Content

This document defines the core content entities for the ROS 2 Tutorial. As this is a content-focused feature, the "data model" refers to the structure of the Markdown documents and their components.

## 1. Chapter

A `Chapter` is a distinct Markdown file representing a major section of the tutorial.

-   **Fields**:
    -   `title`: (string, required) The main heading of the chapter.
    -   `sidebar_position`: (integer, required) The order of the chapter in the sidebar.
    -   `content`: (Markdown text) The body of the chapter.
-   **Relationships**:
    -   A `Tutorial` has many `Chapters`.

## 2. Section

A `Section` is a logical subdivision within a `Chapter`, denoted by a level 2 or 3 Markdown heading (`##` or `###`).

-   **Fields**:
    -   `title`: (string, required) The heading of the section.
    -   `content`: (Markdown text) The body of the section.
-   **Relationships**:
    -   A `Chapter` has many `Sections`.

## 3. Code Snippet

A `Code Snippet` is a block of code embedded in the content, using Markdown's fenced code blocks.

-   **Fields**:
    -   `language`: (string, required) The programming language (e.g., `python`, `xml`, `bash`).
    -   `code`: (string, required) The code to be displayed.
-   **Validation**:
    -   Code must be well-formatted and syntactically correct for the specified language.
    -   Code snippets used in examples should be runnable and tested.

## 4. Citation

A `Citation` is a reference to an external source, formatted in APA style.

-   **Fields**:
    -   `text`: (string, required) The formatted citation text.
-   **Validation**:
    -   Must conform to APA citation style guidelines.
    -   The source must be reliable and published within the last 5 years, as per the specification.
