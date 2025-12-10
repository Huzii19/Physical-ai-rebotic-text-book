# Quickstart: Contributing to the Research Paper

This guide explains the workflow for adding content and citations to the research paper.

## 1. Setting up the Citation Manager

1.  Choose and install a citation manager like Zotero or Mendeley.
2.  Create a new library for this project.
3.  As you find peer-reviewed sources, add them to your library. Ensure the metadata (author, year, title, etc.) is correct.

## 2. Adding Content to the Paper

1.  Open the `ai-k12-paper/paper.md` file in a Markdown editor.
2.  Navigate to the appropriate section where you want to add content.
3.  Write your content. When you make a factual claim that requires a source, you must add a citation.

## 3. Adding a Citation

1.  In your citation manager, find the source you want to cite.
2.  Copy the citation key (e.g., `Author2023`).
3.  In the `paper.md` file, insert the citation key in parentheses at the end of the sentence making the claim. For example:
    > AI-driven tools can reduce teacher grading time by up to 50% (Author, 2023).

## 4. Updating the Bibliography

1.  Periodically, export your entire library from the citation manager to a BibTeX file (`.bib`).
2.  Save this file as `ai-k12-paper/sources/references.bib`, overwriting the old one.
3.  We will later use a script to automatically generate the final "References" section of the paper from this `.bib` file, ensuring all in-text citations are listed and formatted correctly in APA style.

## 5. Committing Your Work

Commit your changes to `paper.md` and `references.bib` to your feature branch.

```bash
git add ai-k12-paper/paper.md ai-k12-paper/sources/references.bib
git commit -m "feat(paper): add section on personalized learning with sources"
```
