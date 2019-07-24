# Noteworthy (notes, notepad World of Warcraft addon)

Current version:        2.0-alpha  
Author:                 Ghost Dancer (aka ZathrasEU)  
Contributing author:    Dejan Josifović (aka Turuvid, Argent Dawn)  
Web:                    https://github.com/28/Noteworthy  

## Description

Noteworthy is a feature rich, configurable notepad with full LDB support.

Overview of features:
- Separate notes page for each character plus a Shared and Quick Notes page (see below).
- All notes pages are accessible by all characters.
- Drag & drop items, spells and macros, creating linkable tooltips (if applicable).
- Insert game info, including character location, target name and chat logs via pop-up Edit menu.
- Change colour of selected text via pop-up Edit menu.
- Quick Notes pop-up menu adds location, target name and chat logs, even when notepad is closed.
- Reminder system can show alerts for each character.
- Notepad window toggled via minimap/floating button, slash commands, macro or as LDB plug-in.
- Notepad behavior controlled via comprehensive settings.
- Full LDB support.

## Instructions & notes

- The notepad window can be toggled opened/closed in a number of ways:
  left-click minimap/floating button, Broker plugin, '/noteworthy' or via a macro.
- All windows and buttons are draggable.
- General EditBox features:
  - Each notes page can store up to 5000 letters.
  - Spells, inventory items and merchant items can be dragged onto the notes window to insert a link.
  - Click links to view it's tooltip.
  - Right click in editbox for the pop-up Edit menu:
	- Insert Info -> Current Location: Inserts current zone and coordinates in Tom Tom format.
	- Insert Info -> Character Name: Inserts current character name.
	- Insert Info -> Target Name: Inserts name of current target.
	- Insert Info -> Date: Inserts current date.
	- Insert Info -> Date and time: Inserts current date and time.
	- Insert Chat Log: Inserts a specified number of entries from the chat log (from all major player initiated channels).
	- Text Colour: Set selected text to one of preset colours.
	- Clear Formatting: Remove colours and hyperlinks. If no selection will apply to whole page.
	- Close Menu: Close the pop-up menu.
  - The Save button saves all notes and settings, and then closes the window.
  - The Cancel button closes the window, losing all changes since opening it
	(see also 'Save on auto close' checkbox below)
  - Press Esc or click outside notepad window to remove focus from notepad (e.g. to type in chat) and close pop-up menus.
- Character Notes tab:
  - This tab is for storing notes specific to each of your characters.
  - It defaults to the current logged on character and can be changed via the drop down menu.
  - Each character's notes page is created the first time you log on with that character.
  - Setting a reminder for a character will show an alert window when logging on with that character:
	- Open Notes button: Close alert window and open notepad window.
	- Remind Again button: Close alert window and leave reminder enabled for next login.
- Shared Notes tab:
  - This page is for storing general notes.
- Quick Notes tab:
  - This is a special page where notes are added via the quick notes system.
  - Add quick notes by right-clicking minimap/floating button or via QuickNotes macro.
  - By default, a character & date prefix will be added to each quick note.
  - Quick notes are added to top of page unless notepad opened on this page, in which case the text is inserted at the cursor.
  - Quick notes options can be found on the Settings tab.
  - Quick Notes menu
	- Location: Saves current zone and coordinates in Tom Tom format.
	- Target Name: Saves name of current target.
	- Chat Log: Saves a specified number of entries from the chat log (from all major player initiated channels).
	- Edit Quick Notes: Opens notepad window on Quick Notes tab.
	- Edit My Notes: Opens notepad window on Character Notes tab and selects the current character.
	- Close Menu: Close the pop-up menu.
- Settings tab (General):
  - Remember last session checkbox: Remember page and cursor between sessions
	- Enabled: Remembers last page and cursor position when you log off.
	- Disabled: First use each session will open on the current character's page.
  - Auto focus checkbox: Focus text area when opening note tabs
	- Enabled: Whenever a notes page is opened, the cursor is focused in the text area.
	- Disabled: To edit text, you must click in the text area.
  - Close on combat checkbox: Close window when entering combat
	- Enabled: If you enter combat, the notepad window will automatically close.
	- Disabled: The notepad window remains open when entering combat.
  - Save on auto close checkbox: Save changes when closed by toggle, log off and combat
	- Enabled: Closing the window by toggling, logging off or entering combat will save all changes.
	- Disabled: Any changes will be lost if the window is closed via the above methods.
  - Save on page change checkbox: Save changes when changing page
	- Enabled: Changes to notes and settings are saved whenever you change tab/page.
	- Disabled: Changes are only saved when the Save button is clicked.
  - Sound effects checkbox: Play sound effects when changing pages and saving
	- Enabled: Sounds effects are played.
	- Disabled: Sounds effects are not played.
  - Sound effects checkbox: Play sound effects when changing pages and saving
	- Enabled: Sounds effects are played.
	- Disabled: Sounds effects are not played.
- Settings tab (Performance):
  - Chat logging: Disabling will prevent chat log copying but MIGHT improve performance
	- Enabled: Enables copying of chat logs using message filters.
	- Disabled: Disables message filters required for copy chat logs feature.
- Settings tab (Buttons):
  - Minimap button checkbox: Show minimap toggle button
	- Enabled: Enables a minimap button to toggle the notepad window.
	- Disabled: Disables the minimap button.
  - Floating button checkbox: Show floating toggle button
	- Enabled: Enables a floating button to toggle the notepad window.
	- Disabled: Disables the floating button.
  - Create Macros button: Creates Noteworthy and QuickNotes macros.
- Settings tab (Quick Notes):
  - Add prefix checkbox: Add date and character info line before each quick note
	- Enabled: Adds blank line and info line with date, time & current character name.
	- Disabled: No additional information is added.
  - Auto edit checkbox: Edit quick note after it is saved to notepad
	- Enabled: Opens quick notes tab in window after quick note has been saved.
	- Disabled: Displays notification in chat.
  - Add at cursor: Insert quick note at cursor if notepad opened on that page (must save changes manually)
	- Enabled: If notepad opened on quick notes tab, quick notes will be inserted at cursor position.
	  Note that when added this way, you must manually Save any changes to the text.
	- Disabled: Quick notes will always be added at the top and will be automatically saved.

NOTE: If you are updating to V1.1 (or higher) from an earlier version, please
delete your old Noteworthy folder first (your settings and data will be unaffected).
This is just to clear out some old files that are no longer being used.
Or use the one of the scripts from the [tools](/tools).

## Dependencies

All dependency libs are packaged with Noteworthy.

- GhostLib:

An utility library made by Ghost Dancer.
- CallbackHandler:

CallbackHandler is a back-end utility library that makes it easy for a library
to fire its events to interested parties.
Last updated on 24.07.2019. from [here](https://www.curseforge.com/wow/addons/callbackhandler).
- LibDataBroker:

LibDataBroker is a small WoW addon library designed to provide a MVC interface
for use in various addons.
Last updated on 09.10.2018. from [here](https://www.curseforge.com/wow/addons/libdatabroker-1-1).
- LibDBIcon:

LibDBIcon is a small library you can throw in your LDB addon that will create
a small minimap icon for you and nothing more.
Last updated on 24.07.2019. from [here](https://www.curseforge.com/wow/addons/libdbicon-1-0).
- LibStub:

LibStub is a minimalistic versioning library that allows other libraries
to easily register themselves and upgrade.
Last updated on 24.07.2019. from [here](https://www.curseforge.com/wow/addons/libstub).

## Tools

There are a couple of helpful things located in the [tools](/tools) directory.

- local_deploy.ps1 - A script for Windows that moves all required Noteworthy files
to the WoW installation directory. The root of install directory should be passed as a
script parameter (enclosed in quotes) or the environment variable *WOWIL* can be set to
the same value.
- package.ps1 - Packages the whole project to an archive. Name of the archive can be specified
as a parameter.

All scripts must be run from the *tools* directory.
