# Using the `build_oai` Script

Calling the `build_oai` script with the `-h` option gives a list of all available options. Below are some important ones:

- `-I`  
  Install pre-requisites. You only need to run this the first time you build the softmodem or when some OAI dependencies have changed.

- `-w`  
  Select the radio head support you want to include in your build. Radio head support is provided via a shared library called the **"oai device"**.  
  The build script creates a soft link from `liboai_device.so` to the actual device used at run-time (e.g., for USRP: `liboai_usrpdevif.so`).  
  The RF simulator is implemented as a specific device replacing RF hardware. It can be specifically built using the `-w SIMU` option but is also built during any softmodem build.

- `--eNB`  
  Build the `lte-softmodem` executable and all required shared libraries.

- `--gNB`  
  Build the `nr-softmodem` and `nr-cuup` executables and all required shared libraries.

- `--UE`  
  Build the `lte-uesoftmodem` executable and all required shared libraries.

- `--nrUE`  
  Build the `nr-uesoftmodem` executable and all required shared libraries.

- `--ninja`  
  Use the Ninja build tool, which speeds up compilation.

- `-c`  
  Clean the workspace and force a complete rebuild.

---

`build_oai` also provides various options to enable runtime error checkers (i.e., sanitizers) to find various types of bugs in the codebase and enhance the stability of the OAI softmodems. Refer to `sanitizers.md` for more details.
