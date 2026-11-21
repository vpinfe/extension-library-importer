# Library Importer

An official extension for [VPinFE](https://github.com/vpinfe/vpinfe).  It moves your tables to VPinFE from PinballX, PinballY or PinUP Popper, or from a plain folder of tables, and makes a game folder for each one with the media, ROMs, saved scores and play history that go with it.

It comes with VPinFE and is on from the start.  Nothing is imported until you start an import, and the last page shows what it is going to do before it does anything.

## Start an import

Open **Import a Library** from any of these:

- The + on **Games** and on **Tables**.
- The Tables step of **Setup**, under **In another frontend**.
- **Settings > Library > Folders**, beside **Add a Folder**.

If you do not see it, open **System > Extensions** and check that Library Importer is **On**.  It also needs the Library feature, which **Settings > This Device** turns on or off.

## What you will be asked

Most answers are already filled in from what the import found, so a first import is mostly reading each page and pressing the forward button.

1. **Importing From**: PinballX / PinballY, PinUP Popper or A Folder of Tables.  For the first two, give the folder the program is installed in.  For PinballX and PinballY that is the folder with `Databases` in it.  For Popper it is the folder with `PUPDatabase.db`.
2. Where each kind of thing lives: tables, media, ROMs, sound and color, music, PUP Packs, saved scores and play history.  Clear one to leave it out.
3. Which tables to import.  Games already in VPinFE are left alone unless you select them, and then they are only given what they are missing.
4. Which VPS entry each game is, where the import could not tell.  VPS is the Virtual Pinball Spreadsheet, and a match gives a game its proper name, media and update notices.
5. Whether to take names and details from VPS or keep your source's.
6. What your wheel pictures are, wheels or logos, and what to do with media folders VPinFE has no slot for.
7. Which of ROMs, high scores and game settings, sound and color sets, music and PUP Packs to bring.
8. Copy or Move, and which library folder the games go in.  Copy is chosen for you and leaves your old frontend working.

A page with nothing to ask is skipped.  The page after that is a summary of everything above, and the button on it says what it will do, such as **Copy 40 tables**.

## When it is running

The import runs as a job, so you can leave the page.  The foot of the left menu names the game it is on, and **Stop** ends it after that game.  What it has made so far stays.

When it ends, **View report** lists what needs you: games that failed, tables whose ROM is missing and games not matched to VPS, each with a link to fix it.  You can run an import again.  Games already in VPinFE are left alone unless you select them.

## Common problems

- **Import a Library** is missing.  The extension is off, or the Library feature is.
- "Nothing this build can read is in that folder".  Pick the program's own folder, the one with `Databases` or `PUPDatabase.db`.
- Every game comes in as **Not matched**.  VPS may not be reachable, or matching may be off.  The summary says which.
- "Needs {size}, but only {free} is free".  Choose a library folder with room.
- A table came in without its ROM.  The report lists it under **Need a ROM**.

The [import walkthrough](docs/importing.md) goes through every page and the report.

## Settings and actions

Library Importer has no settings of its own.  Its one action is **Import a Library**.  It reads the folders you point it at, adds and changes games, and adds library folders.  VPinFE shows this under **What It Can Do** on the extension's page.

## Where to ask

Open an [issue](https://github.com/vpinfe/extension-library-importer/issues) here, or ask in the vpinfe channel of the Virtual Pinball Chat Discord.  Say which program you imported from and what the summary page said.  VPinFE's Getting Help window builds a zip of your logs to attach.

## For developers

To write your own extension, see the [extension docs](https://github.com/vpinfe/vpinfe/blob/vpinfe-3.0/docs/extensions/README.md).

The tests need a VPinFE checkout, because they drive the real thing.  Clone or link this repository into the checkout's `extensions/library_importer` folder, then from the checkout's root:

```bash
python -m tests tests/invariants extensions/library_importer/tests
```

See [Testing your extension](https://github.com/vpinfe/vpinfe/blob/vpinfe-3.0/docs/extensions/testing.md) for the rest.  `tests/` and `.github/` are left out when VPinFE installs the extension.
