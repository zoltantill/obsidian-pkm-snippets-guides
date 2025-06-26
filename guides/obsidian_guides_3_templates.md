# Obsidian Series – Part 3: Templates

## Why Use Templates?

As your Obsidian vault grows, you’ll notice that many notes of the same type (for example, projects, meetings, or books) will share similar metadata and often refer to the same parent note (using the Up:: field).  
To save time and keep your notes consistent, it’s practical to create **templates** for these recurring structures.

## What Is a Template in Obsidian?

A template is simply a regular Markdown file—just like any other note—but it contains only the common fields and structure you want to reuse. The content section is usually left empty or has placeholder text.

A file becomes a template when you place it in your designated **Templates** folder in your vault.  
Obsidian’s built-in Templates plugin can then insert the contents of this file into new notes, so you don’t have to copy and paste manually.

---

## General Template: Basic Metadata for All Notes

Before diving into specific templates for different note types, it’s useful to have a **general template** that includes the basic metadata fields common to almost all notes. This general template serves as a foundation that ensures consistency and makes it easier to manage your vault[1].

### What to include in the general template?
- **type:** The category or kind of note (e.g., project, meeting, book, idea). This helps with filtering and organization.
- **tags:** A list of tags to categorize and quickly find notes.
- **status:** The current state of the note (e.g., active, draft, completed).

### Example general template:

---
type: 
tags: []
status: 
---
Up:: 
Related::


### How to use it?
- Place this general template in your Templates folder as a base file.
- When creating specific templates for note types (like projects or meetings), start from this general template and add fields unique to that type.
- This approach keeps your metadata consistent and your notes well-structured[1].

When you build a template for a specific note type (for example, a project or a meeting), start with this general template and add the fields and structure unique to that type.  
This way, all your notes share a common foundation, and your vault stays organized and easy to manage.


## Creating and Using Templates

1. **Create a Templates folder** (e.g., `Templates`) in your vault.
2. **Make a new note** in this folder. Add the metadata and structure you want to reuse. For example:

---
type: project
status: active
tags: [work, important]
---
Up:: [[Main Projects]]
Related::


- The frontmatter contains the standard metadata.
- The Up:: field points to the common parent note.
- The Related:: field is ready for you to add links to related notes.
- The content area is left blank (or you can add headings/placeholders as needed).

3. **Enable the Templates core plugin** in Obsidian’s settings.
4. **Set your Templates folder** in the plugin’s settings.
5. **Create a new note** and use the "Insert Template" command (`Ctrl+P` > "Insert Template") to quickly add the template structure.


## Benefits of Templates

- **Consistency:** All notes of the same type will have the same fields and structure.
- **Speed:** No need to remember or copy-paste metadata—just insert the template.
- **Organization:** Makes it easier to query, filter, and visualize your notes using plugins like Dataview or Bases.


When you create a new project note, just insert this template and fill in the details.  
This ensures all your project notes are organized the same way and can be efficiently managed and linked.


**Summary:**  
- Templates are regular Markdown files containing only the shared structure and metadata.
- They become templates by being placed in your Templates folder.
- Use templates to save time, keep notes consistent, and make your vault easier to manage.


*Please note:* This was just a simple introduction to the topic—there are many more possibilities and features in Obsidian templates and note organization than what we covered here. For now, this overview gives you a solid foundation and a general picture of how things work. 
 
Later, when we dive into the Templater plugin, we’ll explore even more exciting and powerful solutions!

---

Written by https://github.com/zoltantill
