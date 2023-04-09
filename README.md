![Octocat](https://user-images.githubusercontent.com/66946245/230781621-7fa88d7d-020a-4fe8-9eaa-afb0c4befdc2.png "Github logo")
![Octocat](https://user-images.githubusercontent.com/66946245/230781504-af5ff2a1-db16-42a0-9dac-9401c7a857e5.png "Github logo") 
# Fix Ubuntu Server Cockpit
## How to: Fix Ubuntu Server “Cockpit Cannot refresh cache whilst offline” and “Cannot refresh cache whilst offline” Errors

### The Error

When cockpit is installed on Ubuntu Server  we might get following errors

Cockpit Cannot refresh cache whilst offline

Cannot refresh cache whilst offline

The Fix

By disabling the network-manager, we can resolve those errors (Yes, It’s more of workaround rather than fix)

Warning: Do not run these commands on production server, unless you know what you are doing.

## Disable network-manager service and stop it immediately, then restart the system

```
sudo systemctl disable network-manager.service
```
```
sudo systemctl stop network-manager.service
```
```
sudo reboot
```
Done
