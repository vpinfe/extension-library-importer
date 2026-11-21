# Importing a Library

A short tour of the import, page by page.  The [wiki page](https://github.com/vpinfe/vpinfe/wiki/Importing-a-Library) has every label, state and message.

The import reads your PinballX, PinballY or PinUP Popper library, or a folder of tables, and makes a game folder for each table.  It shows what it is going to do before it does anything.  Most answers are filled in for you, and a page with nothing to ask is skipped.

## Before you start

- Point the import at the program's own folder.  For PinballX and PinballY that is the one holding `Databases`.  For Popper it is the one holding `PUPDatabase.db`.
- Your old library is not changed unless you choose **Move**.  The default is **Copy**, so your old frontend keeps working.

## The pages

1. **Importing From**: pick PinballX / PinballY, PinUP Popper or A Folder of Tables.  Give the program's folder for the first two.
2. Where things live: tables, media, ROMs, sound and color, music, PUP Packs, saved scores and play history.  Clear one to leave it out.
3. **Tables**: choose which to import.  A game already in VPinFE is left alone unless you select it, and then it is only given what it is missing.
4. **Games to Match**: shows the games that could not be matched to the Virtual Pinball Spreadsheet (VPS), the community's table database.  A match gives a game its proper name, media and update notices.  **Change Match...** picks another entry.  A game you leave comes in as **Not matched**.
5. Names and details: take names and details from VPS or keep your source's.
6. **Media**: say whether your PinballX wheel pictures are **Wheels** or **Logos**, and what to do with folders VPinFE has no slot for.  **Keep as extra files** is the safe choice.
7. **ROMs and more**: a switch for each of ROMs, high scores and game settings, sound and color sets, music and PUP Packs.
8. **Copy or Move**: and the **Library Folder** the games go in.
9. **Summary**: everything above in rows.  Read it before you press the button, which says what it will do, such as **Copy 40 tables**.

## While it runs

The import runs as a job, so you can leave the page.  The foot of the left menu names the game it is on.  **Stop** ends it after that game, and what it made stays.

## The report

When it ends, **View report** opens a to-do list in the order you would work down it.

- **Not Imported** lists games that failed.  **Try These Again** runs just those.
- **Need a ROM** lists tables whose ROM is missing, with **Add the ROM**.
- **Not Matched to VPS** has **Match**, and **Nothing for the Wheel** has **Add a Wheel**.
- **Already in VPinFE, Left Alone** has **Add What These Are Missing**.

Fix a game and its row moves down, so you keep your place.  You can run an import again at any time.

## When something looks wrong

- **Import a Library** is missing.  Check that Library Importer is on under **System > Extensions**.
- "Nothing this build can read is in that folder".  Pick the folder holding `Databases` or `PUPDatabase.db`.
- Every game is **Not matched**.  VPS may be out of reach or matching may be off.  The summary says which.
- "Needs {size}, but only {free} is free".  Choose a **Library Folder** with room.
- To import a few tables, press **Select None** on the **Tables** page and select the ones you want.
