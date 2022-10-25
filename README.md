# filesystem
A Complet Cross Platform Virtual FileSystem Layer that just works. This is not a Real filesystem this is a Linking Layer implemented as composition out of ECMAScript Modules to link bind into existing filesystem implementations while @stealify/fs implements our own core filesystem implementation and holds Components to compose filesystems and Databases.

## Why?
This modules and Components do exist to migrate port incrementaly legacy software via the most generic method filesystem replacement that allows us to virtual modify existing software to get desired results this targets mostly Software that we do not want to modify on build. So to generate fast Prototypes and evaluate consequences and work needed to generate final CodeMod Components.

In Developer terms this is a Universal MockAPI to fast implement filesystem abstractions and use them as ECMAScript Module in your favorit project via replacing a single file. 


## Content Old Readme needs porting
In NodeJS Apps as also Windows Linux and any Other Application it is often needed to use the filesystem as interface so this code parts are needed

- there are many other possible combinations but this 2 are the most generic at present. 
- for NodeJS Electron App use it would be enough to use something like node-module-system to hijack the module resolution in CJS Context
  - Example usecase VSCODE Electron Build using Typescript to modify the FS Module that the loaded Typescript



