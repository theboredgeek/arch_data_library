# [[Arch]] [[Linux]] - [[pacman]] Cheat Sheet

General commands and purposes. Also similar to [[yay]].

### 🔄 Sync and Update
* `pacman -Syu` — Update the entire system by syncing repositories and upgrading packages.
* `pacman -Sy` — Refresh the local package databases without upgrading packages (use with caution).
* `pacman -Syy` — Force-refresh all local package databases even if they look up-to-date.

### 📥 Installing Packages
* `pacman -S <pkg>` — Install a specific package from the repositories.
* `pacman -Sv <pkg>` — Verbose installation to view detailed download and dependency information.
* `pacman -U /path/to/pkg` — Install a local file or a package via an external URL.

### ❌ Removing Packages
* `pacman -R <pkg>` — Remove a package but leave its configurations and dependencies intact.
* `pacman -Rs <pkg>` — Remove a package and any of its dependencies not used by other programs.
* `pacman -Rns <pkg>` — Purge a package, its unused dependencies, and all its global configuration files.

### 🔍 Querying and Searching
* `pacman -Ss <keyword>` — Search the remote repositories for a specific keyword or package name.
* `pacman -Qs <keyword>` — Search your locally installed packages for a keyword.
* `pacman -Si <pkg>` — Display detailed information about a package in the remote repositories.
* `pacman -Qi <pkg>` — Display detailed information about a package already installed on your system.
* `pacman -Ql <pkg>` — List every single file installed by a specific package.
* `pacman -Qo /path/to/file` — Find out which package owns a specific file on your system.

### 🧹 Maintenance and Cleanup
* `pacman -Qdtq` — List all orphaned packages (installed as dependencies but no longer needed).
* `pacman -Rns $(pacman -Qdtq)` — Recursively remove all orphaned packages from your system.
* `pacman -Sc` — Clean the package cache by removing old, uninstalled package files.
* `pacman -Scc` — Completely empty the package cache directory to free up maximum disk space.
