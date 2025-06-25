# Obsidian Series – Part 2: Note structure, Metadata, Markdown syntax

In Obsidian, each note typically consists of two main parts:

## 1. Frontmatter

The **frontmatter** is a special section at the very top of the note, enclosed by three dashes (`---`).
**Nothing should appear before the frontmatter**—it must be the very first part of your note.

It contains metadata about the note as key-value pairs separated by colons.

**Example:**
---
type: project
due_date: 2025-06-22
tags: [work, important]
status: active
---

- **Metadata** is best placed in the frontmatter.  
- The fields **type**, **tags**, and **status** are useful for almost every note type—you’ll likely want to include them in most of your notes for better organization and filtering.
- These key-value pairs are essential for aggregations, filtering, and displaying notes in tables or databases using plugins like Dataview or Bases.
- **Date fields** should always use the ISO format: `YYYY-MM-DD`  
- **Lists (for tags, etc.)** can be written in two ways:
  - **Inline array (in square brackets):**
    ```
    tags: [work, important, project]
    ```
  - **Multi-line list (each item on its own line, with a dash):**
    ```
    tags:
      - work
      - important
      - project
    ```
  Both forms are valid in YAML and recognized by Obsidian and its plugins.

- **Spaces in keys:**  
  You can use spaces in metadata keys (e.g., `due date`), but for best compatibility with plugins and queries, it’s often better to use single words or underscores (e.g., `due_date`).

## 2. Content

The **content** is the main body of your note, where you write your actual text, ideas, lists, and information.

- **Links to other notes** should always be placed in the main content, not in the frontmatter.

This is a link to [[Another Note]].

This way, links are visible, clickable, and properly integrated into Obsidian’s graph view and navigation.

**Best practice:**  
Directly under the frontmatter, it’s common to use two special fields for navigation and context, using the double colon syntax (`::`). This format is especially useful because plugins like Dataview and Breadcrumbs recognize these as structured fields, making them easy to query and automate.

- **Up::** Place a link here to the top or parent note in the topic.

Up:: [[Top Note]]

- **Related::** List links to other related notes here.

Related:: [[Related Note 1]], [[Related Note 2]]

Using the double colon (`::`) makes these fields machine-readable and queryable, supporting advanced workflows and visualizations in Obsidian.


---

## Markdown Formatting Marks

Markdown uses simple symbols to format your text in a readable and editable way:

- `#` for headings (more `#` means a smaller heading)
- `-`, `*`, or `+` for bullet lists
- Numbers followed by a dot for numbered lists
- `**text**` for bold
- `*text*` for italic
- `[[Note Name]]` for internal links
- `[Link Text](URL)` for external links
- `> ` for blockquotes
- `` `code` `` for inline code
- Triple backticks for code blocks

These formatting marks keep your notes easy to read and edit, while allowing for rich structure and organization.

---

**Summary:**  
- Place metadata in the frontmatter using colon-separated key-value pairs.
- Use ISO dates and lists for fields like tags.
- Put links and main content in the body of the note.
- Use Markdown formatting for structure and emphasis.

---

*Please note:* This was just a simple introduction to the topic—there are many more possibilities and features in Obsidian note structure, metadata, and Markdown than what we covered here. For now, this overview gives you a solid foundation and a general picture of how things work.

Later, we’ll explore the use of inline code snippets, which can automate and further enhance your notes!


---


Written by https://github.com/zoltantill

.