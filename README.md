# sm-autokit

SourceMod plugin for TF2 that auto-spawns persistent health and ammo kits, saved per-map in a MySQL/MariaDB database.

## Features

- Spawn small, medium, or full health/ammo kits at your position via admin menu (`sm_akmenu`)
- Kit locations are saved to the database and restored every round start
- Kits respawn automatically after being picked up
- Medkits are suppressed during sudden death

## Requirements

- MySQL / MariaDB database
- A `autokits` database entry in `addons/sourcemod/configs/databases.cfg`

## Installation

1. Copy `plugins/auto_kit.smx` to `addons/sourcemod/plugins/`
2. Add a `autokits` section to `databases.cfg`:

```
"autokits"
{
    "driver"    "mysql"
    "host"      "localhost"
    "database"  "your_database"
    "user"      "your_user"
    "pass"      "your_password"
}
```

3. Restart the server — the table `TF2_AutoKits` is created automatically.

## Credits

- **ClassicGuzzi** — original plugin author ([AlliedModders thread](https://forums.alliedmods.net/showthread.php?p=2231510))
- **DarthNinja** — Auto Pumpkins plugin, which this is based on
