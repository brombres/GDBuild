# GDBuild
Rogo-based Godot engine build management tool.

About     | Current Release
----------|-----------------------
Version   | 0.4 (in development)
Date      | October 20, 2023
Platforms | Windows, macOS, Linux
License   | [MIT License](LICENSE)

# Usage

    > rogo help

    USAGE
      rogo build [targets]           Builds the Godot editor and/or export templates for the specified platforms.
      rogo clean                     Deletes the 'bin', 'Build' and '.rogo' folders.
      rogo default
      rogo dist                      Shorthand for 'rogo build dist'
      rogo help [command]            Displays help for a specified command or else all build commands.
      rogo install
      rogo libs
      rogo package
      rogo run                       Runs the most recent editor build for the current platform.
      rogo update <name>
      rogo version [x.y.z [status]]  Displays or changes the Godot version number in all applicable files.

# Description
Supplements Godot's existing SCons-based build system with additional convenience functionality.

- Automatically downloads and builds the Godot engine source.
- Automatically downloads and builds MoltenVK dependency on macOS.
- Automatically downloads and builds the Spine animation module.
- Easily add additional modules (duplicate [BuildSpine.rogue](BuildSpine.rogue) as `BuildXYZ.rogue` and adjust).
- Simple, flexible build syntax. For example, `rogo build templates ios macos release` builds the export templates for iOS and macOS in release mode.
- `rogo` by default builds and runs the editor for the current OS.
- If a file `Local.rogo` exists and defines a project path `AUTLAUNCH = "path/to/godot/project"`, that project will be automatically loaded when `rogo` or `rogo run` is executed.

# Installation
1. Install [Rogo](https://github.com/brombres/Rogo).
2. Clone this repo.
3. Run `rogo`, `rogo help`, etc.
4. Run `rogo build` to build the editor for the current platform.
5. Edit `Config.json` to adjust repo URLs and branches.
