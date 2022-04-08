# filesystem
A Complet Cross Os Virtual FileSystem Layer that just works.

In NodeJS Apps as also Windows Linux and any Other Application it is often needed to use the filesystem as interface so this code parts are needed

- there are many other possible combinations but this 2 are the most generic at present. 
- for NodeJS Electron App use it would be enough to use something like node-module-system to hijack the module resolution in CJS Context
  - Example usecase VSCODE Electron Build using Typescript to modify the FS Module that the loaded Typescript


## Goal 

### Example 1
Use VSCODE + Typescript as Extension and modify the filesystem via a injected node-module-system instance

### Example 2 (Most Promissing Integration Method at present) [Only modifys user Project behavior]
Use VSCODE + the remote attach features to connect to a container that offers a fuse filesystem that we control https://www.docker.com/blog/deep-dive-into-new-docker-desktop-filesharing-implementation/
maybe we could start the linux electron from a modifyed container even under windows https://dev.to/darksmile92/run-gui-app-in-linux-docker-container-on-windows-host-4kde

## Problems
- chocolaty and other dependencies are not install able without admin rights so easy
- docker desktop needed but maybe acceptable.
- lockdown a windows user profile to only execute the needed parts to run stealifyOs - Windows Edition based on Docker and 

### Example 3
- https://docs.microsoft.com/en-us/windows/win32/projfs/projected-file-system
- fuse

### Example 4
use nodejs commandline switches to replace the core modules or hook into the module resolve mechanics

### Example 5
Force the Ecosystem to use the pass System Modules pattern

```js
// ... code that uses fs

const myCode = (fs) => {
  fs.readFileSync()
}

// Other code that uses the above code needs to explicit pass the fs implementation into the module that uses it.
```
