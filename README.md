
# F-List Page Bot
### 8th December 2017
This page is made using Markdown!
### OVERVIEW
Due to the scale of Diverse Fantasy, moving away from a room page with a single owner and editor towards a managed solution will improve productivity and efficiency. As such, I propose we place the profile page in a Markdown-formatted version-controlled repository and build a bot to automate our processes.
### GOALS
* Allow users to edit a human-readable language (Markdown)
* Provide SOI (Separation of Interest) page building, allowing for the project to be divided based on kingdoms, factions, guilds, or any other chosen division.
* Implement a version-controlled environment allowing for fast and efficient rollbacks
* Include an edit-proposal solution, allowing unauthorized users to propose changes to the document and allow a selected team to review and accept, deny, or modify the change proposal.
* Create a character page with the pull request ID on F-List to provide a preview of the changes.
### SPECIFICATIONS
The project will be held on GitHub, depending on if we want private repositories. Users will login and either edit the documents directly (if allowed) or make proposals for the changes. Custom markdown will provide users with a 1:1 conversion between user-readable Markdown and F-List-flavored BBCode.
### PROPOSAL
A bot would be created which would process a Markdown-formatted page, converting it to F-List-flavored BBCode and automatically updating the profile. This will maintain formatting and make editing the page simple as well as cutting out a large margin of error due to the non-human-readability of BBCode. Edits themselves will be done primarily through pull requests. A user will edit the document in question and, when ready, submit it for review. This process allows us to control changes to the document(s) under our control. We can have multiple documents which will be merged into one by the bot, allowing us to divide the document by project or for organization purposes.

When a document is edited and a pull request created, a unique ID is assigned to that pull request. This is shortened into a short seven-character ID which will be used by the bot to create a character on F-List. This character will provide a preview of the changes which we can then accept and merge, deny, or edit the pull request. Merging is the process of accepting the proposed edits.

This bot will also be connected to Discord so that we can be alerted about pull requests and be provided a link to the preview. Additional commands will be provided to enable us to control the bots functions, such as disabling the automatic builds or forcing a rebuild.

As a TL;DR, the bot will:
* Own the room profile,
* Be responsible for updating the profile,
* Watch for pull requests to be submitted to:
* Build preview character pages, and
* Alert staff on the Discord;
* Convert Markdown to BBCode (so we don’t have to touch it),
* Provide a command interface in the Discord so we can control it, and
* Merge multiple pages (allowing us to separate sections into multiple pages as appropriate)
### NOTES FOR EDITORS
If you are making changes to the lore page, one of two things will apply:
* Direct edit permissions: Those with permissions to push directly to the document will be able to edit the documents directly. * These changes will be logged and catalogued automatically. Users with these permissions will be responsible for reviewing and approving or denying pull requests, as well as handling any roll-backs.
* Pull request permissions: Those without permissions to edit directly will do so through the pull request system. This system allows you to edit the document freely and then submit your changes to the lore team for review. If we wish to open it up to the public (which I advocate for), then this is the permission set they will get.
**There are two terms you will need to know for this before you get started:**
* Push: A push is taking your edits and applying them to the repository without using the pull-request system. If you edit the document(s) directly, you are said to have “pushed” your changes.
* Pull: A pull is the action of taking proposed changes to the document(s) and applying them. Users without edit permissions will make pull requests, which asks the lore team to perform a pull on the changes they are proposing.
### DEVELOPER NOTES
* [x] Move this document to GitHub
* [ ] Provide a Markdown tutorial
* [ ] Include child-pages with #include “path/to/markdown.md”
* [ ] Build Collapse boxes with #collapse “Collapse Name”
  * [ ] Indent by four spaces to include in the collapse
* [ ] Build VSCode extension to preview custom Markdown
