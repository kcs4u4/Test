andyinthecloud
==============

Dependencies

[![Version](https://img.shields.io/npm/v/andyinthecloud.svg)](https://npmjs.org/package/andyinthecloud)
[![CircleCI](https://circleci.com/gh/D:/andyinthecloud/tree/master.svg?style=shield)](https://circleci.com/gh/D:/andyinthecloud/tree/master)
[![Appveyor CI](https://ci.appveyor.com/api/projects/status/github/D:/andyinthecloud?branch=master&svg=true)](https://ci.appveyor.com/project/heroku/andyinthecloud/branch/master)
[![Codecov](https://codecov.io/gh/D:/andyinthecloud/branch/master/graph/badge.svg)](https://codecov.io/gh/D:/andyinthecloud)
[![Greenkeeper](https://badges.greenkeeper.io/D:/andyinthecloud.svg)](https://greenkeeper.io/)
[![Known Vulnerabilities](https://snyk.io/test/github/D:/andyinthecloud/badge.svg)](https://snyk.io/test/github/D:/andyinthecloud)
[![Downloads/week](https://img.shields.io/npm/dw/andyinthecloud.svg)](https://npmjs.org/package/andyinthecloud)
[![License](https://img.shields.io/npm/l/andyinthecloud.svg)](https://github.com/D:/andyinthecloud/blob/master/package.json)

<!-- toc -->
<!-- install -->
<!-- usage -->
<!-- commands -->
<!-- debugging-your-plugin -->
# Debugging your plugin
We recommend using the Visual Studio Code (VS Code) IDE for your plugin development. Included in the `.vscode` directory of this plugin is a `launch.json` config file, which allows you to attach a debugger to the node process when running your commands.

To debug the `hello:org` command: 
1. Start the inspector
  
If you linked your plugin to the sfdx cli, call your command with the `dev-suspend` switch: 
```sh-session
$ sfdx hello:org -u myOrg@example.com --dev-suspend
```
  
Alternatively, to call your command using the `bin/run` script, set the `NODE_OPTIONS` environment variable to `--inspect-brk` when starting the debugger:
```sh-session
$ NODE_OPTIONS=--inspect-brk bin/run hello:org -u myOrg@example.com
```

2. Set some breakpoints in your command code
3. Click on the Debug icon in the Activity Bar on the side of VS Code to open up the Debug view.
4. In the upper left hand corner of VS Code, verify that the "Attach to Remote" launch configuration has been chosen.
5. Hit the green play button to the left of the "Attach to Remote" launch configuration window. The debugger should now be suspended on the first line of the program. 
6. Hit the green play button at the top middle of VS Code (this play button will be to the right of the play button that you clicked in step #5).
<br><img src=".images/vscodeScreenshot.png" width="480" height="278"><br>
Congrats, you are debugging!
