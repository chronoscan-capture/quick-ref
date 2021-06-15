
## Desktop / Debugging VBScripts / Start debugging

Once you have the environment ready (see: [Getting the environment ready for debugging](./desktop/debugging-vbscripts/getting-ready.md)) ChronoScan VBScripts can be debugged by clicking
on the button **Debug Script**.

<img src="./_images_/debugging/run_script_1.png" width="620" height="auto">

The Just-In-Time Debugger prompt will appear. Choose **New instance of Visual Studio 2017** and click **OK**.

<img src="./_images_/debugging/vs_prompt.jpg" width="620" height="auto">

Visual Studio will take a moment to start and we will be able to debug ChronoScan code and Objects as done in Visual Studio:

> If we want to add breakpoints, we use the VBS reserved word __Stop__ at the desired line. If no Stop statement is added, ChronoScan will append one at the beggining of the Script

Some Visual Studio commands for debugging.

* F10 - Step Over
* F11 - Step Into
* F5  - Resume
* Add watchers, etc.

<img src="./_images_/debugging/inside_vs.jpg" width="620" height="auto">

> After using Visual Studio for debugging click on the Stop Script button on ChronoScan VBScript editor

<img src="./_images_/debugging/stopdeb.jpg" width="620" height="auto">

> Close the Visual Studio instance used for debugging
