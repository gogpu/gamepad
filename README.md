# gamepad

[![Go Reference](https://pkg.go.dev/badge/github.com/gogpu/gamepad.svg)](https://pkg.go.dev/github.com/gogpu/gamepad)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Pure Go gamepad and joystick input library. Zero CGO.

Part of the [GoGPU](https://github.com/gogpu) ecosystem.

## Status

🚧 **Early development** — not yet functional. Tracking issue: [gogpu#476](https://github.com/gogpu/gogpu/issues/476).

## Planned Features

- **Standard gamepad layout** — positional buttons (South/East/West/North), 6 axes, D-pad
- **Controller mapping database** — SDL community `gamecontrollerdb.txt` (800+ controllers)
- **Hot-plug detection** — connect/disconnect events
- **Rumble/haptics** — basic force feedback
- **Zero CGO** — pure Go on all platforms

## Platform Support

| Platform | API | Status |
|----------|-----|--------|
| Windows | XInput | Planned |
| Linux | evdev + inotify | Planned |
| macOS | IOKit HID | Planned |
| Browser | W3C Gamepad API | Planned |
| Android | InputDevice | Future |

## Architecture

Two-layer design following [SDL3](https://wiki.libsdl.org/SDL3/CategoryGamepad):

1. **Raw joystick layer** — OS-specific device enumeration, raw axes/buttons/hats
2. **Gamepad mapping layer** — standard layout normalization via controller database

Enterprise references: SDL3 (architecture), [Ebiten](https://github.com/hajimehoshi/ebiten) (zero-CGO Go proof).

## Installation

```bash
go get github.com/gogpu/gamepad
```

> **Note:** The package is not yet functional. This import path is reserved.

## License

MIT — see [LICENSE](LICENSE).
