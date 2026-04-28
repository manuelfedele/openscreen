<p align="center">
  <img src="public/openscreen.png" alt="OpenScreen Logo" width="64" />
</p>

# <p align="center">OpenScreen</p>

<p align="center"><strong>A free, open-source screen recording and editing app.</strong></p>

Record your screen, add zoom and motion effects, trim and annotate, and export polished video or GIF clips. OpenScreen is an Electron desktop app built with React, TypeScript, and PixiJS.

<p align="center">
	<img src="public/preview3.png" alt="OpenScreen App Preview 3" style="height: 0.2467; margin-right: 12px;" />
	<img src="public/preview4.png" alt="OpenScreen App Preview 4" style="height: 0.1678; margin-right: 12px;" />
</p>

## Core Features

- Record specific windows or your whole screen.
- Add automatic or manual zooms (adjustable depth levels) with customizable duration and position.
- Record microphone and system audio.
- Crop video recordings to hide parts.
- Choose between wallpapers, solid colors, gradients, or a custom background.
- Motion blur for smoother pan and zoom effects.
- Add annotations (text, arrows, images).
- Trim sections of the clip.
- Customize the speed of different segments.
- Export in different aspect ratios and resolutions.

## Running Locally

```bash
nvm use           # picks up .nvmrc (Node 22.22.1)
npm install
npm run dev       # launches Vite + Electron with hot reload
```

## Building

```bash
npm run build:mac     # macOS
npm run build:win     # Windows
npm run build:linux   # Linux AppImage + deb
```

## Platform Notes

System audio capture relies on Electron's [desktopCapturer](https://www.electronjs.org/docs/latest/api/desktop-capturer) and has platform-specific quirks:

- **macOS:** Requires macOS 13+. On macOS 14.2+ you'll be prompted to grant audio capture permission. macOS 12 and below does not support system audio (mic still works).
- **Windows:** Works out of the box.
- **Linux:** Needs PipeWire (default on Ubuntu 22.04+, Fedora 34+). Older PulseAudio-only setups may not support system audio (mic should still work).

If the Linux build fails to launch with a "sandbox" error, run it with `--no-sandbox`.

## Built With

- Electron
- React
- TypeScript
- Vite
- PixiJS
- dnd-timeline

## License

MIT. See [LICENSE](./LICENSE).
