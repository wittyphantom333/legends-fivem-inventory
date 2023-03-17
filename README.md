<div align='center'><img src='https://avatars.githubusercontent.com/u/127198147?s=200&v=4'/></div>
<div align='center'><h3><a href='https://legendssystems.github.io/docs/legendsInventory/'>legendsInventory Documentation</a></h3></div>

# Framework

The inventory was designed with the intention to move towards a more generic / standalone structure so it can be integrated into any framework without too much hassle. I will be writing a guide for manually setting up support _sometime soon™_. In the mean-time, it will work without any alterations if using the latest updates to **[ESX Legacy](https://github.com/esx-framework/esx-legacy)**.

Experimental support for [qb-core](https://github.com/qbcore-framework/qb-core) has been added, but requires a recent installation. Do not expect 100% compatibility or support.

# Config

Refer to the [documentation](https://overextended.github.io/docs/ox_inventory/) setting your config.
When set, you can add the following to your 'server.cfg'

```
exec @ox_inventory/config.cfg
ensure ox_inventory
```

# Logging

The included logging module utilises datadog to store logging data, which can be expanded for improved analytics and metrics. Register an account at [datadoghq](https://www.datadoghq.com/).
The _free plan_ is enough for most user's purposes and provides far more utility than the typical weird discord logs utilised in other resources.

Once you have registered, generate an API key and add `set datadog:key 'apikey'` to your server config.

# Features

### Shops

- Creates different shops for 24/7, Ammunation, Liquor Stores, Vending Machines, etc.
- Job restricted shops, such as a Police Armoury.
- Items can be restricted to specific job grades and licenses.
- Define the price for each item, and even allow different currency (black money, poker chips, etc).

### Items

- Generic item data shared between objects.
- Specific data stored per-slot, with metadata to hold custom information.
- Weapons, attachments, and durability.
- Flexible item use allows for progress bars, server callbacks, and cancellation with simple functions and exports.
- Support for items registered with ESX.

### Stashes

- Server-side security prevents arbitrary access to any stash.
- Support personal stashes, able to be opened with different identifiers.
- Job-restricted stashes as well as a police evidence locker.
- Server exports allow for registration of stashes from any resource (see [here](https://github.com/overextended/ox_inventory_examples/blob/main/server.lua)).
- Access small stashes via containers, such as paperbags, from using an item.
- Vehicle gloveboxes and trunks, for both owned and unowned.

### Temporary stashes

- Dumpsters, drops, and non-player vehicles.
- Loot tables allow users to find random items in dumpsters and unowned vehicles.

</td></tr></table>
