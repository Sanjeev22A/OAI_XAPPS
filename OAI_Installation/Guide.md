## Installation Guide for OAI
***Note:This will be the first version of installation, the guide might vary as hurdles are faced***

- First step is to get the necessary code to build.
  - Run the below code in a directory initialized with git
  ```bash
  git pull https://gitlab.eurecom.fr/oai/openairinterface5g.git
  ```
- Next step is to build the project. To build it go to the directory cmake_targets inside the pulled project
  - Run the below given command to go to the particular directory
    ```bash
      cd cmake_targets
    ```
    Be careful to run this command only from the correct directory. Otherwise you will face an error.
- Locate a file named build_oai in the current directory. This script is developed to build the oai binaries for different hardware platforms and usecases. The main OAI binaries currently available are:
  - LTE UE: lte-uesoftmodem
  - 5G UE: nr-uesoftmodem
  - LTE eNodB: lte-softmodem
  - New radio gnb: nr-softmodem
  - New radio cu-up : nr-cuup
  - LTE physical simulators: dlsim and ulsim
  - The 5G PHY simulators: nr_dlschsim, nr_dlsim, nr_pbchsim, nr_pucchsim, nr_ulschsim, nr_ulsim, polartest, smallblocktest, nr _ulsim, ldpctest.

- Refer to the file [Build_Options.md](build_options) file for the build details
- 
    



