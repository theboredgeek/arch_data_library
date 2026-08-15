# [[Arch]] [[Linux]] - [[yay]] Cheat Sheet

General commands and purposes. Also similar to [[pacman]].

### 🔄 Sync and Update
* `yay` — Runs a full system upgrade for both official [[pacman]] repos and the [[AUR]].
* `yay -Syu` — Explicitly syncs repositories and upgrades all regular and AUR packages.
* `yay -Sua` — Upgrades only the [[AUR]] packages.

### 📥 Installing Packages
* `yay -S [package]` — Installs a new package from official repos or the [[AUR]].
* `yay -R [package]` — Removes a specified package from the system.
* `yay -Rns [package]` — Removes a package along with its unneeded dependencies and configuration files.
* 
### 🔍 Querying and Searching
* `yay [term]` — Interactively searches for a package by name across official repos and the [[AUR]].
* `yay -Ss [term]` — Non-interactively searches for a keyword in package names and descriptions.
* `yay -Si [term]` — Shows detailed information and metadata about a specific package.

### 🧹 Maintenance and Cleanup
* `yay -Yc` — Cleans up unneeded and orphaned dependencies left behind on the system.
* `yay -Sc` — Cleans old package caches from both [[pacman]] and [[yay]] storage.
* `yay -Ps` — Prints general system statistics, version data, and package counts.
* `yay -G [package]` — Downloads the raw [[PKGBUILD]] script for an [[AUR]] package without building it.
