# Fix-Ubuntu-Server-Cockpit-
# How to: Fix Ubuntu Server 19 “Cockpit Cannot refresh cache whilst offline” and “Cannot refresh cache whilst offline” Errors
The Error

When cockpit is installed on Ubuntu Server 19, we might get following errors

Cockpit Cannot refresh cache whilst offline

Cannot refresh cache whilst offline

The Fix

By disabling the network-manager, we can resolve those errors (Yes, It’s more of workaround rather than fix)

Warning: Do not run these commands on production server, unless you know what you are doing.

## 1 Disable network-manager service and stop it immediately, then restart the system

```
 sudo systemctl disable network-manager.service

 sudo systemctl stop network-manager.service

sudo reboot
```
2 Now, get back to cockpit, errors won’t be there anymore
