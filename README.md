# ha-config
I use snapshots for comprehensive configuration versioning. Home Assistant has a blend of UI and text based configuration, which snapshots are best suited for. This repo is the source of text editable configuration. It is used for:
* version control: HA pulls the latest master branch.
* documentation: Github provides a great UI for file browsing, quick edits, and issue tracking.
* sharing: I've learned from browsing others' repos, hopefully I can give back.

**Key Capabilities**
* Allow Lutron Pico remotes to control Hue, or anything else
* Dashboard for Home Resource: NAS Health, Printer supply levels, etc
* Integrate unsupported hardware into HomeKit

**Roadmap**

Enhance robustness:
* Modernize: Update Lutron custom integration, migrate to HACS version
* Backups: Automate creation and pruning of snapshots
* Reduce risk of SD card failure; SSD, network disk, VM, etc

Unifi Protect Cameras integrated in Homekit:
* Home assistant integration https://github.com/briis/unifiprotect
* HomeKit bridge - installed, but inactive

Data Insights & Dashboard:
* Home event dashboard
* Natural light level metrics
* Influx and Grafana for visualization
  * https://www.home-assistant.io/blog/2015/12/07/influxdb-and-grafana/

AV integration to support replacement of aging URC solution:
* Bring Pioneer AVR into HK (volume resets / remote control)
  * Power/wake, volume, input selection
  * Older https://www.home-assistant.io/integrations/pioneer/
  * Newer https://www.home-assistant.io/integrations/onkyo
* Investigate Blu-ray support

Integrations for logging activity:
* Integrate Homekit only sensors (direct or through homekit?)
* Integrate RainMachine - good for logging. Investigate: flow sensor passthrough, weather parsing?
  * https://www.home-assistant.io/integrations/rainmachine/
* Integrate Unifi Network

Home Event Notifications
* Duration based notifications (door open too long)
* Text To Speech notifications

Home Resource Dashboard
* Reduce / centralize source of emails & reminders
  * Backup health monitoring
  * Version availability
* Add monitoring capabilites
  * NVR disk space
  * Key Network HW outage alerts

Daily Task Dashboard
* Dog care
* Chores / homework

Enhance presence using Unifi Network
