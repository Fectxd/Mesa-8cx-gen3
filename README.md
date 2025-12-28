# Mesa Zink for Windows on ARM (8cx Gen 3)

This repository provides automated builds of Mesa with Zink driver for Windows on ARM devices, specifically optimized for Snapdragon 8cx Gen 3.

## What is this?

- **Mesa**: Open-source graphics library implementation
- **Zink**: OpenGL implementation on top of Vulkan
- **Target**: Windows on ARM64 (aarch64) devices

## Features

- OpenGL support via Zink (using Vulkan backend)
- Software rasterizer (swrast) as fallback
- OpenGL ES 1.x and 2.x support
- OSMesa (off-screen rendering)

## Download

Compiled binaries are available in the [GitHub Actions artifacts](../../actions) after each successful build.

For tagged releases, check the [Releases](../../releases) page.

## Installation

1. Download `mesa-zink-windows-arm64.zip` from the latest build
2. Extract the archive
3. Copy the DLL files to your application directory or system directory
4. Ensure you have up-to-date Vulkan drivers installed

## Building

This project uses GitHub Actions for automated builds. The workflow:
- Uses MSVC ARM64 cross-compiler
- Builds Mesa with Meson build system
- Enables Zink and software rasterizer drivers
- Packages the output as artifacts

To trigger a build, simply push to the repository or manually trigger the workflow.

## Requirements

- Windows on ARM64 device
- Vulkan-capable GPU driver (for Zink)
- Or software rendering fallback (swrast)

## License

Mesa is licensed under the MIT License and other open-source licenses. See the [Mesa project](https://gitlab.freedesktop.org/mesa/mesa) for details.

## Credits

- [Mesa3D](https://www.mesa3d.org/) - The Mesa 3D Graphics Library
- Built for Snapdragon 8cx Gen 3 Windows on ARM devices
