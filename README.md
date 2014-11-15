cordova-plugin-battery-status
=============================

[Cordova][cordova] plugin to get battery level on demand for iOS.

## Overview
1. [Supported Platforms](#supported-platforms)
2. [Installation](#installation)
3. [ChangeLog](#changelog)
4. [Using the plugin](#using-the-plugin)

## Supported Platforms
- __iOS__ *(including iOS8)*

## Installation
The plugin can be installed from git repository.

### Local development environment
From master:
```bash
# ~~ from master branch ~~
cordova plugin add https://github.com/solo999/cordova-plugin-battery-status.git
```

## ChangeLog
- See [CHANGELOG.md][changelog] to get the full changelog for the plugin.


## Using the plugin
The plugin creates the object `cordova.plugins.battery.status` with the following method:

[battery.status.get][get]

### Plugin initialization
The plugin and its methods are not available before the *deviceready* event has been fired.

```javascript
document.addEventListener('deviceready', function () {
// cordova.plugins.battery.status is now available
}, false);
```

### Get the battery status
The battery status can be accessed through the `battery.status.get` interface.<br>
The method takes a callback function as its argument which will be called with the battery level. Optional the scope of the callback function ca be defined through a second argument.

```javascript
cordova.plugins.battery.status.get(function (battLevel) {
// console.log('battery level: ' + battLevel);
}, scope);
```

## License

This software is released under the [Apache 2.0 License][apache2_license].

© 2013-2014 Polaris Telematics Ltd (HK). All rights reserved


[cordova]: https://cordova.apache.org
[CLI]: http://cordova.apache.org/docs/en/edge/guide_cli_index.md.html#The%20Command-line%20Interface
[PGB]: http://docs.build.phonegap.com/en_US/index.html
[PGB_plugin]: https://build.phonegap.com/plugins/1195
[changelog]: CHANGELOG.md
[get]: #get-the-battery-status
[apache2_license]: http://opensource.org/licenses/Apache-2.0

