## Example output
```
# dur /snap
Showing Size of each dir

16K	snap/snap-store
16K	snap/snapd-desktop-integration
16K	snap/remmina
16K	snap/firmware-updater
16K	snap/aws-cli
12K	snap/mesa-2404

=====================
======================
PATH : snap/snap-store
======================
4.0K	snap/snap-store/common
4.0K	snap/snap-store/1367
4.0K	snap/snap-store/1338
0	snap/snap-store/current
======================
PATH : snap/snapd-desktop-integration
======================
4.0K	snap/snapd-desktop-integration/common
4.0K	snap/snapd-desktop-integration/361
4.0K	snap/snapd-desktop-integration/357
0	snap/snapd-desktop-integration/current
======================
PATH : snap/remmina
======================
4.0K	snap/remmina/common
4.0K	snap/remmina/7392
4.0K	snap/remmina/7085
0	snap/remmina/current
======================
PATH : snap/firmware-updater
======================
4.0K	snap/firmware-updater/common
4.0K	snap/firmware-updater/226
4.0K	snap/firmware-updater/224
0	snap/firmware-updater/current
======================
PATH : snap/aws-cli
======================
4.0K	snap/aws-cli/common
4.0K	snap/aws-cli/2193
4.0K	snap/aws-cli/2188
0	snap/aws-cli/current
```
## Example Output with -e (exclude path)
```
root@a024:~# dur -e snap/snap-store snap
Showing Size of each dir

16K	snap/snap-store
16K	snap/snapd-desktop-integration
16K	snap/remmina
16K	snap/firmware-updater
16K	snap/aws-cli
12K	snap/mesa-2404

=====================
======================
PATH : snap/snapd-desktop-integration
======================
4.0K	snap/snapd-desktop-integration/common
4.0K	snap/snapd-desktop-integration/361
4.0K	snap/snapd-desktop-integration/357
0	snap/snapd-desktop-integration/current
======================
PATH : snap/remmina
======================
4.0K	snap/remmina/common
4.0K	snap/remmina/7392
4.0K	snap/remmina/7085
0	snap/remmina/current
======================
PATH : snap/firmware-updater
======================
4.0K	snap/firmware-updater/common
4.0K	snap/firmware-updater/226
4.0K	snap/firmware-updater/224
0	snap/firmware-updater/current
======================
PATH : snap/aws-cli
======================
4.0K	snap/aws-cli/common
4.0K	snap/aws-cli/2193
4.0K	snap/aws-cli/2188
0	snap/aws-cli/current
```

- **Can be used on /var**
- **Huge output warning when use on such paths /usr , /var/lib**
- **Use -e to exclude nosiy path from output Example : `dur -e /path/e1 /path/e2 /path/e3 /path`**
