# Que 13: Difference between apt update & apt upgrade.

| apt update | apt upgrade |
| ---------- | ----------- |
| `apt update` updates the list of available packages and their versions, but it does not install or upgrade any packages | `apt upgrade` actually installs newer versions of the packages you have. After updating the lists, the package manager knows about available updates for the software you have installed. This is why you first want to update. |
