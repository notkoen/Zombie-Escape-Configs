
# CS2 Config Formatting

## CS2Fixes Entwatch

```json
[
    {
        "name": "Item Name",                // Name of item that appears in chat
        "shortname": "Short Name",          // Name of item that appears on the HUD
        "hammerid": "",                     // Hammerid of the weapon entity
        "message": true,                    // Whether to show pickup/drop messages in chat
        "ui": true,                         // Whether to show this item on the HUD
        "transfer": true,                   // Whether to allow this item to be transferred
        "color": "",                        // Color of the item for chat messages (see list of colors)
        "triggers": [""],                   // Array of hammerids of any triggers that this item is associated with
        "handlers": [
            {
                "type": "button",           // "button" or "game_ui"
                "hammerid": "",             // hammerid of the entity
                "event": "OnPressed",       // Name of the output
                "mode": 2,                  // Mode of the handler
                                            //  0/1 = None
                                            //  2 = Cooldown,               3 = MaxUses
                                            //  4 = MaxUsesWithCooldown,    5 = CooldownAfterUses
                                            //  6 = CounterDown,            7 = CounterUp
                "cooldown": 60,             // Cooldown duration if mode = 2,4,5
                "maxuses": 0,               // Maxuses if mode = 3,4,5
                "message": true,            // Whether to show when this is used in chat
                "ui": true                  // Whether to track this handler on the HUD
            }
        ]
    }
]
```

### Clean Template

```json
[
    {
        "name": "",
        "shortname": "",
        "hammerid": "",
        "message": true,
        "ui": true,
        "transfer": true,
        "color": "",
        "triggers": [""],
        "handlers": [
            {
                "type": "button",
                "hammerid": "",
                "event": "OnPressed",
                "mode": 0,
                "cooldown": 0,
                "maxuses": 0,
                "message": true,
                "ui": true
            }
        ]
    },
]
```

### Available Colors

- white, default
- darkred
- team
- green
- lightgreen
- olive
- red
- gray, grey
- yellow
- silver
- blue
- darkblue
- purple, pink
- red2
- orange, gold