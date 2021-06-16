
## Desktop / Debugging VBScripts / Getting the environment ready for debugging

### 1. Required Software

**Microsoft Visual Studio 2017** installed in the same machine is required in order to debug ChronoScan VBScripts.

Download link for free community edition:  

[https://visualstudio.microsoft.com/es/vs/older-downloads/](https://visualstudio.microsoft.com/es/vs/older-downloads/)

### 2. If using Visual Studio Community edition, make sure you have installed the component Just-In-Time debugger in the installer

Just-in-Time debbuger can be either installed on Visual Studio by adding the workload for C++ Desktop development or by adding it as an individual component as shown on the following images.

__Workload__:  
<img src="./_images_/debugging/vscomunnitygitcpp.jpg" width="620" height="auto">


__Individual component__:  
<img src="./_images_/debugging/vs2017jit.jpg" width="620" height="auto">

### 3. Enable Just-In-Time debugging for Scripts and Managed code on Visual Studio

Run Visual Studio as **administrator** and open Tools > Options... on the main toolbar.

<img src="./_images_/debugging/vs2017_tool_debug.png" width="620" height="auto">

Check Just-In-Time debugging for Scripts and Managed code.

<img src="./_images_/debugging/justin.jpg" width="620" height="auto">

### 3. Close Visual Studio
