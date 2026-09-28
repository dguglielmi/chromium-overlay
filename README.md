![pkgcheck](https://github.com/dguglielmi/chromium-overlay/actions/workflows/pkgcheck.yaml/badge.svg)

# chromium-overlay
A Gentoo Linux Chromium browser overlay.

## How to use this overlay ?
You can use this overlay with portage plug-in sync system (see: https://wiki.gentoo.org/wiki/Project:Portage/Sync)

### New portage plug-in sync system (>=sys-apps/portage-2.2.16)

- Add "chromium-overlay" configuration
```
# cat << EOF > /etc/portage/repos.conf/chromium-overlay.conf
[chromium-overlay]
location = /var/db/repos/chromium-overlay
sync-type = git
sync-uri = https://github.com/dguglielmi/chromium-overlay.git
auto-sync = yes
masters = gentoo
EOF
```

OR via eselect-repository

```
# emerge app-eselect/eselect-repository
# eselect repository add chromium-overlay git https://github.com/dguglielmi/chromium-overlay.git
```

- Retrieve chromium overlay

```
# emaint sync -r chromium-overlay
```
