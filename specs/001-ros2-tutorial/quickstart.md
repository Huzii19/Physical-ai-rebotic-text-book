# Quickstart: Creating a New Tutorial Chapter

This guide explains how to add a new chapter to the ROS 2 tutorial within the Docusaurus site.

## 1. Create the Markdown File

Navigate to the `my-website/docs/ros2-tutorial/` directory. Create a new Markdown file for your chapter (e.g., `chapter4-new-topic.md`).

## 2. Add Front Matter

At the top of your new file, add the following front matter to configure the chapter's title and position in the sidebar. The `sidebar_position` determines the order.

```markdown
---
sidebar_position: 4
---

# My New Chapter Title
```

## 3. Write Your Content

Write your chapter content using standard Markdown. You can include text, headings, lists, and code blocks.

### Code Blocks

To add a code snippet, use fenced code blocks with the appropriate language identifier:

````markdown
```python
import rclpy

def main():
    print("Hello, ROS 2!")

if __name__ == '__main__':
    main()
```
````

## 4. Add Citations

Ensure any factual claims are backed by citations formatted in APA style. You can add a "References" section at the end of your chapter.

## 5. Preview Your Changes

Run the Docusaurus development server to see your new chapter live:

```bash
cd my-website
yarn start
```

Navigate to `http://localhost:3000` and find your new chapter in the "ROS 2 Tutorial" section of the sidebar. The site will hot-reload as you make changes to the file.

## 6. Commit Your Work

Once you are satisfied with your new chapter, commit the file to your feature branch.

```bash
git add my-website/docs/ros2-tutorial/chapter4-new-topic.md
git commit -m "feat(docs): add chapter 4 on a new topic"
```
