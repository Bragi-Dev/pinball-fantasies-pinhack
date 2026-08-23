# Pinball Fantasies Pinhack for DOSBox Staging

A modern DOSBox Staging port of the classic Pinball Fantasies no-scroll pinhack.

This patch allows the full pinball table to be shown on screen at once instead of scrolling vertically during play.

The Windows and Linux packages work with all games/tables included in the Pinball Fantasies Deluxe package.

---

## Download

Go to the **Releases** section and download the package for your operating system:

- `Pinball-Fantasies-Pinhack-Windows-x64.zip`
- `Pinball-Fantasies-Pinhack-Linux-x86_64.tar.gz`

You still need your own copy of **Pinball Fantasies Deluxe**.
The game itself is not included.

---

# Windows

## Installation

1. Download:
   `Pinball-Fantasies-Pinhack-Windows-x64.zip`

2. Open your existing Pinball Fantasies Deluxe installation folder.

   This is the folder containing files such as:

   ```text
   dosboxPFD.conf
   dosboxPFD_single.conf
   game.gog
   game.inst
   DOSBOX\
   ```

3. Extract the contents of the ZIP file directly into that folder.

   After extraction, the folder should also contain files such as:

   ```text
   dosbox.exe
   Pinball-Fantasies-Pinhack.bat
   pinhack.conf
   resources\
   docs\
   ```

4. Double-click:

   ```text
   Pinball-Fantasies-Pinhack.bat
   ```

That's it.

You do **not** need to install DOSBox Staging separately or edit the original GOG configuration files.

---

# Linux

## Installation

1. Download:

   `Pinball-Fantasies-Pinhack-Linux-x86_64.tar.gz`

2. Open your existing Pinball Fantasies Deluxe installation folder.

   This is the folder containing files such as:

   ```text
   dosboxPFD.conf
   dosboxPFD_single.conf
   game.gog
   game.inst
   DOSBOX/
   ```

3. Extract the contents of the archive **directly into that folder**.

   After extraction, the folder should also contain:

   ```text
   dosbox
   Pinball-Fantasies-Pinhack
   pinhack.conf
   ```

4. Run:

   ```text
   Pinball-Fantasies-Pinhack
   ```

If your file manager does not allow the launcher to run, make sure it is marked as executable.

From a terminal this can be done with:

```bash
chmod +x Pinball-Fantasies-Pinhack
```

The included DOSBox Staging build is a native Linux executable.  
Do **not** run it through Wine or Proton.

---

# What the pinhack does

Pinball Fantasies normally scrolls the playfield vertically as the ball moves around the table.

With this version of DOSBox Staging, the complete playfield is displayed at once.

The patch:

- works with all games/tables in the Pinball Fantasies Deluxe package
- shows the full playfield without vertical scrolling
- leaves menus and other video modes unaffected
- is enabled automatically by the included `pinhack.conf`

The original game files are not modified.

---

# Existing saves and high scores

The pinhack uses the same Pinball Fantasies Deluxe installation and game files as the normal version.

This means your existing high scores and other game data remain shared with the original installation.

You can keep using the original launcher as well as the pinhack launcher.

---

# Disabling the pinhack

Simply start the game using your normal Pinball Fantasies Deluxe launcher instead of the included pinhack launcher.

---

# Supported platforms

Prebuilt packages are currently provided for:

- Windows x64
- Linux x86_64

The Windows package contains a complete portable DOSBox Staging build, including the resources required by DOSBox Staging.

The Linux package uses a portable x86-64 DOSBox Staging build with most non-system dependencies bundled or statically linked.

---

# Tested with

- Pinball Fantasies Deluxe
- all games/tables included in the Pinball Fantasies Deluxe package
- GOG release
- Windows 11
- Linux Arch
- DOSBox Staging development version from August 2026

---

# Background

This project is based on the original `dosbox-pinhack` work by **DeXteRrBDN**:

https://github.com/DeXteRrBDN/dosbox-pinhack

The original patch targeted an older DOSBox codebase and no longer applies directly to current DOSBox Staging.

This project ports the relevant behaviour to modern DOSBox Staging and adds a simple configuration option:

```ini
pinhack = true
```

The ready-made packages use this option automatically through the included `pinhack.conf`.

---

# Building from source

If you prefer to build it yourself, apply:

```text
dosbox-staging-pinball-fantasies.patch
```

to a compatible DOSBox Staging source tree and build DOSBox Staging normally for your platform.

The patch adds the `pinhack = true` render option and the Pinball Fantasies no-scroll behaviour.

See the official DOSBox Staging build documentation for platform-specific dependencies and build instructions.

---

# Credits

Original DOSBox pinhack concept and implementation:

- DeXteRrBDN — `dosbox-pinhack`

Port to modern DOSBox Staging:

- Bragi-Dev
- Developed and tested with assistance from ChatGPT

DOSBox Staging is developed by the DOSBox Staging project and contributors.

---

# License

This project is derived from and distributed alongside DOSBox Staging.

See the included license files and the DOSBox Staging project for the applicable licensing terms.

Pinball Fantasies is not included with this project and must be obtained separately.
