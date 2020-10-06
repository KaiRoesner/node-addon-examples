[![Version 0.0.2](https://img.shields.io/badge/version-0.0.2-blue)](https://github.com/KaiRoesner/node-addon-examples/tree/master/external_lib_demo#n-api-external-lib-demo)

# N-API External Lib Demo

This is an example project that demonstrates how to wrap an external C++ library (i.e. one that we do not own ourselves) in a Node module.

## Folder Structure
The example assumes the following folder structure:

```bash
root  # project root folder
  +- src  # the sources of the external lib
  |    +- external_lib.cpp  # the api of the external lib
  |    +- external_lib.h
  |    +- ...  # other source files of the external lib
  +- node  # the node wrapper addon
  |    +- wrapper.cc  # C++ N-API wrapper of the external lib
  |    +- wrapper.h
  |    +- ...  # other files required for Node binding
  +- ...   # wrappers for other languages
```

## Usage
To build and run this program on your system, clone it to your computer and run these commands inside the `node` folder of your clone:

```bash
$ npm install
$ npm run test
```

> You need to have Node 10.5.0 or later installed. 

To re-build the program after changing the C++ code do

```bash
$ npm run rebuild
```

## Changelog

### **0.0.1** (2010-10-05)
- Initial version

### **0.0.2** (2010-10-06)
- Less invasive version (C++ wrappers inside `node` folder)