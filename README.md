![Rocket Nuimo](https://github.com/pryomoax/rocket-nuimo-node/raw/master/assets/rocket-nuimo.png)

[![Release](https://img.shields.io/github/release-pre/pryomoax/rocket-nuimo-node.svg?style=for-the-badge)](https://github.com/pryomoax/rocket-nuimo-node/releases)
[![License](https://img.shields.io/github/license/pryomoax/rocket-nuimo-node.svg?style=for-the-badge)](./LICENSE)
![Node](https://img.shields.io/npm/v/rocket-nuimo.svg?style=for-the-badge&label=version)
[![Maintained](https://img.shields.io/badge/Maintained%3F-yes-green.svg?style=for-the-badge)](https://github.com/pryomoax/rocket-nuimo-node/graphs/commit-activity)

🚀 Rocket Nuimo, a Node.js client package for Senic's [Numio Control](https://www.senic.com/nuimo-control) BLE device.

----

# Installation
To install `rocket-nuimo` for use within your project use [yarn](https://yarnpkg.com) or [npm](https://npmjs.com)

```bash
$ yarn add rocket-nuimo
```

## macOS Mojave Installation
`rocket-numio` uses [noble](https://github.com/noble/noble) under the hood for communicating with to BLE devices. `nobel` running on Mojavé has issues currently and must be worked around.

Whether you are uses `rocket-numio` as a depedency, or running one of the [example](./examples) you will need to make overrides or adjustments when running on macOS.

### Overridding Depedencies

In *your* project's `package.json` insert the following:

```json
  "depedendencie": {
   "rocket-nuimo": "^0.4"
  },
  "resolutions": {
    "noble": "https://github.com/Timeular/noble-mac"
  }
```

Then run from the terminal

```bash
$ yarn install
```

Now when you run your respect `yarn install` or `npm install` it will the package suitable to running on macOS.

----

# Getting Started

API documentation coming shortly. Check out [examples](./examples) for now.

Clone `rocket-nuimo-node` and run the examples to try things out. [package.json](./package.json) contains many example scripts. Alternatively, for [Visual Sudio Code](https://code.visualstudio.com/) users you have access to the pre-configured launch configurations to run the examples.

```bash
$ git clone https://github.com/pryomoax/rocket-nuimo-node.git
$ cd rocket-nuimo-node
$ yarn install
```

Run one of the following scripts

```bash
# Device discovery
$ yarn device-discovery

# Simple display of custom glyphs
$ yarn display

# Example of simple animation
$ yarn animation

# Selection events
$ yarn select-events

# Touch/Long Touch events
$ yarn touch-events

# Swipe (on device) and through the "fly" touchless gesture
$ yarn swipe-events

# Hover proximity events, through "fly" touchless gestures
$ yarn hover-events

# Dial rotate events
$ yarn rotate-events
```

# Toubleshooting

There can be troubles connecting to a Nuimo when playing around with the device. To give you some leads in trouble shooting, try the following:

- Click the center screen button to wake up Nuimo Control
- Power cycle Nuimo Control
- [Reset bluetooth](https://macpaw.com/how-to/fix-bluetooth-not-available-problem) on your Mac
- Check if there are any current issue with [noble](https://github.com/noble/noble) related to the OS/Node.js version you are using.
