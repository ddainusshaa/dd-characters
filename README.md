# DD Characters

Multicharacter system for [Qbox](https://github.com/Qbox-project/qbx_core).

**Author:** ddainusshaa

## Requirements

- [ox_lib](https://github.com/overextended/ox_lib)
- [qbx_core](https://github.com/Qbox-project/qbx_core)
- [illenium-appearance](https://github.com/iLLeniumStudios/illenium-appearance)
- [qbx_apartments](https://github.com/Qbox-project/qbx_apartments) (new characters)
- [bob74_ipl](https://github.com/Bob74/bob74_ipl) (preview interiors)

## Installation

1. Add the resource as `dd-characters`.
2. In `qbx_core/config/client.lua`:

   ```lua
   characters = {
       useExternalCharacters = true,
   }
   ```

3. `ensure dd-characters` after dependencies.

## Character slot limits

Configure **only** in `data/server.lua`:

```lua
characters = {
    defaultNumberOfCharacters = 3,
    playersNumberOfCharacters = {
        ['license2:xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx'] = 10,
    },
},
```

dd-characters owns character listing, slot limits, and creation. It does not use `qbx_core` multichar callbacks or `qbx_core/config/server.lua` character limits.

## Configuration

| File | What to edit |
|------|----------------|
| `data/shared.lua` | Brand, apartments, codex/pulse toggles, exit action, default spawn |
| `data/client.lua` | Preview scenes, model loading timeout |
| `data/server.lua` | Character slot limits, registration validation |
| `data/starters.lua` | Starter items for new characters |
| `data/codex.lua` | Codex content (enable in shared.lua) |
| `data/pulse.lua` | Pulse feed content (enable in shared.lua) |

## Development

```bash
cd web
bun install
bun run build
```
