# Sainbury's Ubuntu Touch webapp

This webapp is based on ogra's alternate-webapp-container:

    bzr branch lp:~ogra/junk/alternate-webapp-container

This is a new approach using an alternate webapp container that
does not use a toolbar at the top but instead provides a bottom
menu with navigation objects. 

## TODO

  * Add URL handlers for supported sites.

## Changes

### 1.4-WIP

  * Added support for handmadebyyou.co.uk.
  * Added support for sainsburysenergy.com.
  * Added support for sainsburyshome.co.uk.
  * Added support for sainsburyslivingarchive.co.uk.
  * Added support for sainsburysgifts.co.uk.

### 1.3

  * Added radial navigation for Home and Groceries.
  * Update framework components.

### 1.2

  * Added a splash screen.

### 1.1

  * Removed unused assets.

### 1.0

  * Updated framework to 15.04.
  * Removed unused policy groups.

### 0.4

  * Added Ogra's alternate webapp template.

### 0.3

  * Initial release.

# Development

## Building

Edit the value of `applicationName` at the top of `qml/Main.qml` to match
your application name to work around <https://launchpad.net/bugs/1435778>

Edit `config.js` to add `webappName`, `webappUrl` and `webappUrlPattern`
similar to how you would use them as commandline options to webapp-container.

Optionally you can set the `webappUA` variable in `config.js` to override
the User Agent string.

Edit the `.desktop` and `manifest.json` to your liking.

Replace icon.png with your own icon that is 128x128.

Now run:

    click build .

This will create a `.click` package with you webapp.

## Installing

Push the click to your device via adb, then:

    adb shell pkcon install-local --allow-untrusted /path/to/click

You will see a bunch of progress bars ... once they are done,
pull down the app scope to refresh it and find your new app in there.

## Publishing

Publish the generated click package at https://myapps.developer.ubuntu.com/dev/click-apps/

# License

touch-app-sainsburys is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

touch-app-sainsburys is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with touch-app-lastpass. If not, see <http://www.gnu.org/licenses/>.
