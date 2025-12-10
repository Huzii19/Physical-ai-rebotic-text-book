# Data Model: Research Paper Content

This document defines the core entities for the "AI in K-12 Classrooms" research paper.

## 1. Paper

The top-level entity, representing the entire Markdown document.

-   **Fields**:
    -   `title`: (string, required) The title of the paper.
    -   `word_count`: (integer) The total word count of the document.
-   **Relationships**:
    -   Has many `Sections`.

## 2. Section

A major part of the paper, corresponding to the 7 sections outlined in the specification (e.g., Executive Summary, ROI Analysis).

-   **Fields**:
    -   `title`: (string, required) The title of the section.
    -   `content`: (Markdown text) The body of the section.
-   **Relationships**:
    -   Belongs to one `Paper`.
    -   Contains many `Claims`.

## 3. Claim

An assertion of fact made within the paper's content.

-   **Fields**:
    -   `statement`: (string, required) The assertion being made.
-   **Validation**:
    -   Every `Claim` must be supported by at least one `Citation`.
-   **Relationships**:
    -   Is supported by one or more `Citations`.

## 4. Citation

A reference to an external, peer-reviewed source.

-   **Fields**:
    -   `key`: (string, required) A unique identifier (e.g., `Author2023`).
    -   `apa_entry`: (string, required) The full bibliographic entry in APA format.
-   **Validation**:
    -   Source must be peer-reviewed and published within the last 5 years.

## 5. ROI Metric

A specific data point used in the Return on Investment analysis.

-   **Fields**:
    -   `name`: (string, required) The name of the metric (e.g., "Teacher Hours Saved Per Week").
    -   `value`: (number or string) The value of the metric.
    -   `source`: (string) The `Citation` key that supports this metric.
-   **Validation**:
    -   Must be clearly defined and sourced.
