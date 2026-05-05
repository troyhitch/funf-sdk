# Funf SDK

Developer kit for **Funf**, a sub-$99 physical fantasy handheld with hard era-authentic constraints, physical cartridges, and BLE-based local trading.

You write games in Lua 5.4 against a thin API. The runtime enforces every era constraint at the metal: 64-color master palette, 16 colors per sprite/tile, 2 BG layers, 64 sprites onscreen, 16 sprites per scanline, 4-channel chiptune audio, 2 MB cartridge ROM, 8 KB FRAM save, 60 Hz hard real-time, BLE link only — no internet from games.

The constraints aren't suggestions. They're the platform's identity.

## What's in this repo (when populated)

```
api/         Lua API headers and reference implementation stubs you link
             against in the emulator.
docs/        SDK API reference, .cart binary format spec, asset pipeline
             docs, getting-started guide.
tools/       cart-builder, asset converters (PNG → tilemap, WAV → wavetable
             audio, Aseprite → sprite sheets), .cart inspector.
examples/    Pressure-test cartridges: Pong, Snake, tile RPG screen,
             trading demo. Read these to learn the API.
```

## Status

Bootstrap. Repo just created — code lands as the runtime stabilizes. The current API draft is in the workspace project (`projects/funf/SDK-API-REFERENCE.md`) and in the project's Obsidian vault.

## Runtime

The runtime that executes your `.cart` files is closed-source and ships as a binary inside the official desktop/web emulator. Source for the device firmware and runtime lives in the private platform repo (`troyhitch/funf`); only the SDK is open.

## License

MIT. Build whatever you want with this. Cartridges you ship are yours.
