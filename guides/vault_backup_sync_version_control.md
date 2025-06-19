# Obsidian Backup, Sync, and Version Control

## Obsidian Vault Location

I prefer to store my documents, code, images, Obsidian vaults, and other materials in directories with short, simple paths.

**Path Best Practices**
- Keep paths short to avoid Windows’ MAX_PATH limitation (260 characters).
- Avoid spaces, accented, and special characters for maximum compatibility.
- Use lowercase and clear, descriptive folder names.

This approach makes automation scripts, backups, and cross-platform compatibility much easier.

The order and naming of folders within the path is also important for clarity and scalability.

Below I share my concept, but feel free to simplify or adapt it to your needs.


## Parts of the Path

A typical path for my Obsidian vault looks like this:
`D:\drive\vcs\ds\obsidian`

Let’s break down the reasoning behind each part:


### Cloud Service Local Folder

Backup is essential, so I place the Obsidian folder inside my local cloud sync folder.  
I use Google Drive because it’s also accessible on my phone, making it easy to keep my Obsidian vault in sync across devices.

I move the Drive folder outside of my Documents folder to make the path shorter and simpler.  
The cloud software handles automatic backups and retains deleted files for recovery if needed.

I recommend moving your cloud sync folder (Google Drive, Dropbox, OneDrive, etc.) to the root of a data drive (e.g., `D:\drive`) and renaming it according to the best practices above.


### Version Control Folder

Since Obsidian notes are simple text files (Markdown), version control can be easily applied to them without any special configuration or extra software.

Using a version control system (VCS) provides two main advantages:

- **Restorability:**  
    You can always review or restore previous states of your notes, ensuring that no important information is lost—even if you accidentally delete or overwrite something.

- **Change Tracking:**  
    You can precisely see when, in which file, and what modifications were made. This helps you understand the evolution of your notes and makes it easy to trace back when you wrote down a particular idea.
   
For version control, I recommend using **JJ** together with Git. 
Git is robust and compatible with many tools (such as WinMerge for deep comparison).  
**GG** provides a simple graphical interface for JJ, making version control accessible even for those less comfortable with the command line12.

I've created several scripts and guides for setting up this workflow, which you can find here:  
**[JJ Jujutsu GG Script Collection on GitHub](https://github.com/zoltantill/jj_jujutsu_gg_script_collection)**

This collection includes scripts for:
- Initializing version control before first use
- Automated version-saving (run at every Windows startup for daily snapshots)
- GG launcher script

If you want to track the version history of your vault, I recommend this setup.  
All related scripts and instructions are in the linked collection.

Inside the cloud folder, I create a dedicated folder for version-controlled content—primarily my Obsidian vault and files to be synced with my phone: `D:\drive\vcs`

This is where I initialize the version control system (VCS) and store the related scripts.

You can exclude specific folders, subfolders, file types, or individual files from version control using the `.gitignore` file. This allows you to use the sync solution without including unwanted files in version control.

**Note:**  
If you want to sync other files (e.g., ebooks, media) that should not be versioned, use a `.gitignore` file to exclude them from Git tracking.

**Sample `.gitignore` for an Obsidian vault:**

```text
# Ignore attachments and cache
.obsidian/
.trash/
attachments/
*.DS_Store

# Ignore system files
Thumbs.db
*.log
.tmp.*
```

All version control files are stored at this level.


### Sync solution

The simplest option is to subscribe to Obsidian Sync, but I have no personal experience with it.

Instead, I use the **DriveSync** app on my phone, which syncs my vault with a single tap in just a few minutes. After syncing, Obsidian on Android takes about half a minute to re-index the vault.

I primarily use Obsidian on Android for reading. For quick note-taking, I prefer Todoist, but I extract and organize information in my Obsidian knowledge base.

I connect DriveSync to the ds folder:
`D:\drive\vcs\ds`


### Obsidian vault

The key point is that I do not place the vault directly in the sync folder, but rather in a dedicated subfolder.  
Within the vault, files can be organized at the root level or in subfolders, as needed.

`D:\drive\vcs\ds\obsidian`


### ebooks vault

If I want to sync ebooks to my phone, I do not place their folder inside the Obsidian vault. Instead, I create a separate folder for ebooks at the same level as the Obsidian vault, within the `ds` directory.

`D:\drive\vcs\ds\ebooks`


## Summary

By organizing your Obsidian vault and related files in a structured, version-controlled, and cloud-synced way, you gain:

- Reliable backup and restore options
- Easier automation and scripting    
- Cross-platform compatibility  
- Peace of mind for your notes and knowledge base    

---

Feel free to adapt this template to your workflow, and expand on any section as needed! If you have specific tools or scripts you use, you can document those as well.

---

Written by https://github.com/zoltantill

