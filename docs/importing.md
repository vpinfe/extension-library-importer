# Importing a Library

This page goes through the import page by page.  The same walkthrough is on the VPinFE wiki.

If your tables are in PinballX, PinballY or PinUP Popper, VPinFE can read that library and make a game folder for each table, with the media, ROMs and play history that go with it.  It also takes a plain folder of tables.

You do this once when you move to VPinFE, or again to import a second library.  The import asks a few questions and shows you what it is going to do before it starts.  Most answers are already filled in from what it found, so a first import is mostly reading each page and pressing the forward button.

## Where to start it

- From the + on Games and on Tables, where it is listed as **Import a Library**.
- From the Tables step of Setup, under **In another frontend**.
- From **Import a Library** on **Settings > Library > Folders**, beside **Add a Folder**.

Importing is done by this extension, which comes with VPinFE.  If the button is missing, open **System > Extensions**: the extension has to be on, and so does the Library feature.

## Before you start

- Point the import at the program's own folder.  For PinballX or PinballY that is the folder holding `Databases`.  For Popper it is the folder holding `PUPDatabase.db`.
- Your tables are not changed when you import from PinballX, PinballY or Popper, because the import copies them unless you choose to move them.  A plain folder of tables gets a folder made for each loose table, where it lies.

## The pages

Each page opens with the answer the import worked out already chosen.  A page with nothing to ask is skipped, so you may see fewer than nine.

### 1. Import a Library

Under **Importing From**, choose PinballX / PinballY, PinUP Popper or A Folder of Tables.  Each choice has a line under it saying what it brings in.

- For PinballX / PinballY and PinUP Popper, give the **Folder** the program is installed in.
- For A Folder of Tables there is no **Folder** here, because the next page asks where your tables are.

### 2. Reading it as your source

VPinFE shows where each kind of thing lives: **Tables**, **Media**, **ROMs**, **Sound and Color**, **Music**, **PUP Packs**, **Saved Scores** and **Play History**.  Most are worked out from the source and say so.  Anything you leave empty is not imported.

A frontend with more than one system adds a **Systems** list, so you can leave some out.

### 3. Tables

Every table found is listed.  **Filter by name** narrows the list.  The chips **New**, **In VPinFE** and one for tables hidden in the source narrow it by kind.  **Select All** and **Select None** act on the rows shown, and a count says how many are selected.

A game already in VPinFE is left alone unless you select it.  Then it is only given what it is missing.  Its row says how it was recognized ("Same folder", "Same VPS entry" or "Same table file") and what selecting it would add, such as "adds 2 tables, its ROM and its play history".

### 4. Match games to VPS

This page appears when some games could not be settled on their own.  VPS is the Virtual Pinball Spreadsheet, the community's database of tables.  A game that matches an entry gets its proper name, media and update notices.

- **Games to Match** lists the games VPinFE could not match on its own, each with the reason ("Two entries" or "IPDB says another entry") and the entry it would offer.
- **Change Match…** picks another entry.
- **Show All {count}** and **Hide Matched** show and hide the matched rows.

A game you leave is still imported, as **Not matched**, and you can match it afterward from Games.

### 5. Names and details

This page appears when the spreadsheet would name a matched game differently from your source.

- **Folder Names**: **From VPS** names each game folder for its entry, and the other choice keeps the names your source has.
- **Details**: **From VPS** takes title, maker, year and type from the spreadsheet.  Keeping your source's details saves them as your own edits, so they show over the spreadsheet's.  **Choose which** keeps yours for the fields you pick under **Keep Yours For**, each with how many differ.

### 6. Media

This page appears when the source has pictures.  It lists the kinds of picture your games come with and how many of each.  Every one is imported.

- **What Are Your PinballX Wheel Pictures?**: PinballX, PinballY and Popper do not tell wheels from logos, so this asks, naming your source.  The choices are **Wheels**, small badges that stand for each game in a list, and **Logos**, each game's title as a picture.  VPinFE marks the one it thinks it sees and shows a few of your images to help.
- Some folders hold files VPinFE has no place for, such as extra folders PinUP Popper keeps.  Each gets a line under **{folder} Folder** with how many files it holds and which games they are for.  **Keep as extra files** keeps them with their games, and it is the choice unless you change it.  A choice that starts with Use as puts them in a kind VPinFE has, and **Don't import** leaves them behind.  The summary lists what was left under **Files Not Imported**.
- If you choose **Logos**, VPinFE sets **Wheel Set** so themes keep showing them.
- **Download Missing Media** fills gaps afterward from VPinMediaDB.  It only fills empty slots, and only for games matched to the spreadsheet.
- **Manufacturer Logos** adds a logo for each maker your folder does not have one for.  It appears when the import finds some.

### 7. ROMs and more

A switch for each thing found, with the number of games it comes with: **ROMs**, **High Scores and Game Settings**, **Sound and Color Sets**, **Music** and **PUP Packs**.  A thing the source does not have is not listed.  The page also says how many tables need a ROM that is not there.

### 8. A folder for each table

This page appears when there are table files to carry.

**Copy or Move** is the choice here.

- **Copy** leaves your folder as it is.  It is already chosen, and it is the safe one, because your old frontend keeps working until you are sure.
- **Move** leaves no second copy.  Anything else that opens those tables will not find them any more.  For a frontend, the page says that source won't find them anymore.
- **Library Folder** is where VPinFE keeps your games, with a folder for each table.  Copy and move both ask for it.  It starts with a suggested folder, says "VPinFE creates it" when the folder is new, and shows the space needed and what is free.  A moved table is not forced into your source's folder.

A folder of loose tables you point at needs no copy.  Each table gets a folder where it lies.

### 9. This is what will happen

The summary, with what will be imported and what will not.  The next section goes through it.

A step that takes longer than a second, such as reading a large source or matching games, shows a bar and a line about what it is doing above the buttons.  The forward button waits until the step is done.  **Back** and **Cancel** stay available.

## The summary

The last page is the whole import in rows, so read it before you press the button.

- **Importing From** and **Source Folder**: what the import took your source to be, and where.
- A row for each kind of thing, with the folder it reads from or "not being imported", and **Missing ROMs** where tables need one that is not there.
- **VPS Matching**: how the matching went.  If some games did not match, **Not Matched to VPS** says how many were not found, how many could be two entries, and how many have an entry IPDB disagrees with.
- **Already Here**: how many existing games are given what they are missing, and how many are left alone.  **Skipped** counts the new ones you did not select.
- **How** and **Going Into**: copied, moved or put in a folder where they lie, and where to.  **Space Needed** shows the room.  The import will not start without enough: "Needs {size}, but only {free} is free on {where}".
- **What Is Imported**: **Games**, **Tables**, **Media Files**, **Backglasses and Settings**, **Games with Play History** and **Matched to VPS**.
- **Files Not Imported**: the media folders your source has that VPinFE has no slot for, each with how many files.  Pages after the first, and videos in a folder that takes pictures only, are counted here too.

Under the rows are notes on what the import found while reading, such as a file it could not parse or an encoding it had to guess.  They do not stop the import.

The button says what it will do: **Copy N tables**, **Move N tables**, **Put N tables in folders**, **Use this folder** or **Import N games**.  When there is nothing left to import, it says "Nothing left to import" and cannot be pressed.

## After you press the button

The import runs as a job, and you can leave the page.  The foot of the left menu names the game it is on, and Jobs shows the same.  **Stop** ends it after the game it is on.  What it has made so far stays.

When it ends, a notice says "Import finished", "Import finished - not imported: {count}" or "Import stopped", with **View report**.

A Games or Tables list you have open shows the new games at that point, without a reload.

## The report

The report opens from that notice, from **View Report** on the job in Jobs, and from the line beside **Import a Library** on the Folders page.  That line reads "{program}, {count} to review" until everything is settled and "{program}, imported {when}" after.  **Open in Its Own Tab** keeps the report beside the Manager while you work through it.

A strip of figures runs across the top: **Games Imported**, **Need Review**, **Already in VPinFE** and **Files Not Imported**.  Click one to jump to its section.  Each section is a card of rows in three columns: the game, a note, and what you can do about it.

It is a to-do list, in the order you would work down it.

- **Needs Review**:
  - **Not Imported** lists games that failed, with the reason, **See the Log**, and **Try These Again**, which starts a second import with just those games selected.
  - **Need a ROM** lists tables whose ROM is not there, with **Add the ROM**.
  - **Not Matched to VPS** has **Match**, and **Nothing for the Wheel** has **Add a Wheel**.
  - Each link opens that game at the right place.  When you fix one, its row keeps a mark (**Added** or **Matched**) and moves down, so the list shortens without losing your place.
- **Good to Know**:
  - **Already in VPinFE, Left Alone** has **Open** and **Add What These Are Missing**.
  - **DMD Positioned on Its Own** lists games whose DMD is in a place of its own, with **Displays**.
- **Files Not Imported** lists hardware setup files the import found beside your library and did not import, such as `ScreenRes.txt`, `DmdDevice.ini`, `B2SServer` and `DirectOutput`.  The ones that have a place in VPinFE link to **Displays**.
- **Imported** shows tiles for what was imported, and **Show All {count} in Tables** lists every game it made.

A group longer than a few rows names the first few and ends with "{count} more", which opens the rest in Tables.  The VPinFE wiki's Filling Media page covers anything still missing.

## Running it again

You can run an import again.  Games already in VPinFE are left alone unless you select them, so a second run adds the new ones and fills gaps in the old without changing what you have set.

## When something looks wrong

- **Import a Library** is missing.  The Library Importer extension is off, or the Library feature is.  Check **System > Extensions**.
- "Nothing this build can read is in that folder".  The folder is not one a supported frontend uses.  Pick the one holding `Databases` or `PUPDatabase.db`.
- Tables came in with no media.  The media folder on the second page is empty or wrong.  Point it at the right folder.
- Every game is **Not matched**.  The Virtual Pinball Spreadsheet may not be available, or matching may be off.  The summary says "Switched off, so no game is matched" or "VPS is not available, so no game is matched".
- "Needs {size}, but only {free} is free on {where}".  Choose a **Library Folder** with room.
- A table came in without its ROM.  The report lists it under **Need a ROM**, and **Add the ROM** opens where to put it.
- To import only a few tables, press **Select None** on the Tables page and select the ones you want.

## Less common cases

- The old device's paths are read as the ones on your share when the library is on another device you reach across a network share, and the summary says so with a line that starts "Reading".
- Matching games to the Virtual Pinball Spreadsheet needs the spreadsheet.  Without it the import still runs and every game comes in unmatched, which Games shows how to fix.
- A folder that does not look like the source you chose gets "That does not look like {source}", and you cannot go on.  A folder that cannot be reached says "That folder is not reachable from here".
- When a device has no folders yet, **Import a Library** is in the notice that says so.
- A Games or Tables list with something open in the panel, a row selected or text in the search box keeps what you are doing when the import ends, and **Reload from Disk** shows the new games.
