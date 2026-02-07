---
title: "OpenZT 0.1.0 Released!"
description: "Announcement post for the first OpenZT release 0.1.0"
date: 2025-02-06
draft: false
author: "Finn"
---

We are pleased to announce the very first release of OpenZT 0.1.0. If you just want to jump straight in you can download OpenZT [here](https://github.com/openzt1/openzt/releases/download/v0.1.0/res-openzt.dll), to install simply drop it in your Zoo Tycoon install folder, most likely at `C:\Program Files (x86)\Microsoft Games\Zoo Tycoon`, however please be mindful of the following: 
Expect bugs! This is a first release and is yet to be widely tested. We recommend a new clean install of Zoo Tycoon and for all mods to be put in a 'mods' subfolder rather than 'dlupdate', 'dupdate etc. We also recommend **not** editing the `path` field in `zoo.ini` and instead let OpenZT handle mod loading. Finally because OpenZT modifies the UI slightly the 'Allow Purchasing Young Hack' hack does not _currently_ work.

## Changes for users

### Configuring OpenZT

When you first run OpenZT it will create a new config file `openzt.toml` with some defaults, many of the features to follow are configured by editing this file.

### User customizable menu filters

You can now create custom filters for the purchase menu in Zoo Tycoon. Under the `[expansions]` section in `openzt.toml` you can add an entry like this:
`"Filter Name" = ["elephant", "zebra", "my mod.ztd"]`
This will add a new filter called "Filter Name" that will only display the elephant, zebra and any animals, scenery or buildings in the 'my mod.ztd' file.

### Configurable mod ordering and disabling

When you start Zoo Tycoon with mods installed in the `mods` subdirectory, each mod will be added to the `order` list under the `[mod_loading]` section in `openzt.toml`. These can then be reordered as needed. You can also add any of these mods to the `disabled` list and they will not get loaded.

### Bugfixes
 - Fixed a crash when a maintenance worker repairs a fence one tile away from the edge of the map
 - Fixed a crash when deleting a zoowall one tile away from the edge of the map
 - Fixed an issue where special characters like ä in the filename of .ztds would prevent the mod from being loaded if the Windows language was set to English


## Changes for modders

 - A new `meta.toml` file for adding metadata such as a mod_id, author name and dependencies [docs](https://docs.zooberry.org/zt1/openzt/getting-started/)
 - Custom Habitats and Locations are now easier to make [docs](https://docs.zooberry.org/zt1/openzt/habitats_and_locations/)
 - You can now patch individual values or sections in other zoo tycoon resources [docs](https://docs.zooberry.org/zt1/openzt/patch_mods/)
 - New 'Roof' tag can be applied to scenery items, allowing them to be hidden with a `Ctrl-R` shortcut [docs](https://docs.zooberry.org/zt1/openzt/extensions/#complete-example-roof-extension-mod)


## Acknowledgement

This is by no means an exhaustive list but I would like to thank the following people for their assistance with the OpenZT project
 - wowjinxy for an immense amount of reverse engineering
 - Goosifer for reverse engineering, coding and this website!
 - Gymnasiast for help reverse engineering the save game format
 - Jay and Fern for sharing their ridiculous levels of knowledge about zoo tycoon modding and various file formats
 - Vondell for the logo
 - Many modders from the zoo tycoon community for their knowledge, ideas and enthusiasm
