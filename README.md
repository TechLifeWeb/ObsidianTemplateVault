This is my Template Vault for Obsidian

# Folders
- I avoid folders for content. Every note is stored in the Notes folder with the exception of Daily Notes which are held in the Notes/Daily subfolder.
- Notes that are not content are stored under the Support folder. There are subfolders for the special cases of Navigation notes (some call these MOCs or Maps of Content) and Templates.
- The "Files" folder is where attachments are held.

# Bookmarks
- I have all the Navigation notes bookmarked so they appear in the list of Bookmarks. That panel I have open on the upper left and is where I start all my navigation unless I just search.
- I loosely use the ideas of PARA presented by Tiago Forte: <a href='https://fortelabs.com/blog/para/' target='_blank' rel='noopener noreferrer'>The PARA Method: The Simple System for Organizing Your Digital Life in Seconds</a>. "Projects" is too work oriented in my brain so I use "Efforts" to mean essentially the same thing for personal stuff.
	- 📥In Box: This is a list of any file this has been linked to but not yet created
	- 🗂️Resources: Things I am interested in
	- 🌐Areas: Areas of Responsibility are the **roles you take on in life** and the **hats you wear** (Spouse, Mother/Father, Team Leader, Soccer Coach)
	- 💼Efforts: Things I'm actively working on
	- 😎 Favorites: Any notes tagged "favorites" will show up here
	- 📈Stats: Uses Dataview to show the current number of files in my Obsidian Vault and has a list of the 10 most recent notes.
- Having Bookmarks always handy in the sidebar like this is very helpful for temporarily keeping notes handy. For example, if I'm on a trip I'll bookmark my "Trip to London" (or wherever) note and it is then a click or tap away when I pull up Obsidian while on the road.

# Vault Setup Notes
- I store this file at the root level of my folder structure for quick and easy access. Whenever I add or modify a plugin, I update the notes in this document accordingly. Some changes are straightforward, while others are more complex, so maintaining a record ensures clear documentation for future reference.

# Templates
- Default Template: Gets applied to all notes except Daily Notes
- Daily Notes: For Daily Notes
- Code - Subcategory List
	- This is code is magical Dataview code that pulls in a Base with a similar name. It is for displaying linked notes by Subcategory.
- Code - Category List
	- More magical Dataview code the pulls in a Base.
- The "magic" of these code snippets is that the snippet pulls in code when the note is displayed rather than actually living on the note itself. This allows me to change the design of the template ONCE and it is applied to ALL notes where this code is displayed. For example, I could change the design of a Base or add text to the template and now instantly all notes with that code have the changes rather than having to reedit all the notes.

# Plugins I Use
- Commander
	- Commander is a plugin for Obsidian which allows you to add commands to different parts of the user interface.
- Dataview
	- Create and display queries to your content. Obsidian now has the core plugin called Bases which does something similar however, I've found there are still use cases for Dataview
- Harper
	- Harper is a grammar checking plugin that doesn't violate your privacy.
- Lazy Plugin Loader
	- Load plugins with a delay on Obsidian startup, so that you can get your app startup down into the sub-second loading time.
- Linter
	- This Obsidian plugin formats and styles your notes with a focus on configurability and extensibility.
- Minimal Theme Settings
	- This plugin accompanies Minimal Theme, allowing you to customize the theme from the Obsidian Settings panel. This plugin is not required to use Minimal Theme, but highly recommended.
- Omnisearch
	- Omnisearch is a search engine that "just works". It always instantly shows you the most relevant results, thanks to its smart weighting algorithm.
- Paste image PNG to JPEG
	- The plugin automatically handles the following when the image (png jpg jpeg) is pasted into the notes
		- 1,Convert the image to jpeg format and compress it
		- 2,store the image in the current notes directory in the images folder
		- 3,Change the name of the image to the name of the current note plus a number
- Plugin Update Tracker
	- Know when installed plugins have updates and evaluate the risk of upgrading
- Style Settings
	- This plugin allows snippet, theme, and plugin CSS files to define a set of configuration options. It then allows users to see all the tweakable settings in one settings pane. Style Settings allows both toggling classes on and off the body element, as well as setting numeric, string, and color CSS variables.
- Templater
	- A templating language that lets you insert variables and functions results into your notes. It will also let you execute JavaScript code manipulating those variables and functions.

# Personal Usage Guidelines
I usually keep the following in a separate note that I keep in the Root or as a Favorite. It helps to keep handy so you can remember your decisions
- Have a purpose about why you are making the note. This helps you be more focused on noting the details and not copy/pasting things whole cloth.
- Avoid splitting content into multiple vaults.
- Avoid folders for content.
- Avoid non-standard Markdown.
- My default note template is very minimal and works for all my content.
```
---
date: <% tp.date.now("YYYY-MM-DD")%>
category: 
subcategory: 
tags: 
aliases:
---
# Details
 <% tp.file.cursor() %>
```
- ⭐**Every** singe note gets a category
- Category:
	- Category is the broad area the note refers to (Python, Obsidian, Windows)
	- These are always a **link** so the Category page
- Subcategory:
	- Subcategory is a further definition of the Category.
		- Example: Category: `[[Windows]]` Subcategory: Utilities
	- Sometimes I do make the subcategory a link.
		- Example: Category: `[[Restaurants]]` Subcategory: `[[Coffee Shops]]`
		- The reason for this is sometimes, like this case of Coffee Shops, there are many similar items in the subcategory and I might want to report on them in a different way using Bases or Dataview.
- Tags:
	- Always pluralize tags.
	- Always lower case, single word tags.
	- If multi word tags are absolutely necessary, use camelCase
	- Tags = the **type** of **note** (examples: links, meetingNotes, clippings)
	- Keep the number of tags to a minimum
		- Start with as few as possible and build from there if you come up with a *really* good use case for a new one
- Use internal links profusely.
- Use `YYYY-MM-DD` dates wherever dates are needed. <a href='https://en.wikipedia.org/wiki/ISO_8601' target='_blank' rel='noopener noreferrer'>ISO 8601 </a> exists for a reason.
- Usage Examples (you'll find these in this template vault as well):
	- You read a good book called *Daemon*
		- Name of the note: Daemon
		- category: `[[Books]]`
		- subcategory: Fiction
	- You want to save a link to a web page about Dataview in Obsidian
		- tags: links
		- category: `[[Obsidian]]`
		- subcategory: Dataview
