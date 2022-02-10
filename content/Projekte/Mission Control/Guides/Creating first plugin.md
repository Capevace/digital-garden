\#mission-control #docs

# Creating your first plugin

Functionality is added to mission-control through plugins and its Plugin API.

Plugins expose a single function that gets called dynamically by mission-control.
Passed during initialization is a `PluginAPI` that exposes mission-controls features to the plugin.

## Plugin API

`PluginAPI` exposes access to:

* [Service API](Service%20API.md)
* [HTTP API](HTTP%20API.md)
* Permissions API
* Dashboard API

## Creating a TODO plugin

Start by creating a new file 
