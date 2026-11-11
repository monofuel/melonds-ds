# monoMelon development

The `monomelon` branch starts at melonDS DS 1.4.0 commit
`f394adbacb5722ee97c1b37c8064da9a25818310`. It preserves the libretro API and
runtime identity. Its build fixes allow optional Git discovery and populated
FetchContent source directories, including offline package-manager builds.

The default engine dependency is a full commit pin from
https://github.com/monofuel/melonDS/tree/monomelon. That branch contains the
existing ARM64 tile and sprite optimizations and their reference test. Future
engine changes belong there; libretro integration changes belong here.

Build and validation instructions, the pinned dependency inventory and
open-demo PGO training are maintained in
https://github.com/monofuel/mono-overlay/blob/master/docs/monomelon.md.
The overlay supplies checksummed archives and keeps its engine pin aligned with
`cmake/FetchDependencies.cmake`. Update both pins when promoting engine changes.
Preserve all upstream source and dependency licenses when distributing binaries.
