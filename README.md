# GSoC_24-Final-Submission-Report

This repository contains the final report for my Google Summer of Code (GSoC) 2024 project with Chips Alliance. The project involved implementing a GDS reader/writer in OpenROAD using OpenDB. The report details the work completed, what’s left to do, and acknowledgments.

The project repository can be found at [Ali-975/OpenROAD](https://github.com/Ali-975/OpenROAD).    
The project report can be found at [Final Report GSoC 24](https://github.com/Ali-975/GSoC_24-Final-Submission-Report/blob/main/Final_Report.md)

## Instructions

To build and test the GDS reader/writer implementation, follow these steps:

1. **Clone the Repository:**
   ```bash
   git clone --recursive git@github.com:Ali-975/OpenROAD.git
   ```
   This command clones the OpenROAD repository along with all its submodules. The `--recursive` flag ensures that all nested repositories and dependencies are also cloned.

2. **Navigate to the Repository Directory:**
   ```bash
   cd OpenROAD
   ```
   This command changes your current directory to the `OpenROAD` directory where the project files are located.

3. **Install Dependencies:**
   You may follow our helper script to install dependencies as follows:
   ```bash
   sudo ./etc/DependencyInstaller.sh
   ```
   This command executes the `DependencyInstaller.sh` script to install the necessary dependencies for the project.

4. **Create a Build Directory and Navigate into It:**
   ```bash
   mkdir build && cd build
   ```
   This command creates a new directory named `build` and moves into it. This is a standard practice to keep build files separate from the source code.

5. **Generate Build Files with CMake:**
   ```bash
   cmake ..
   ```
   This command configures the project using CMake, generating the necessary build files based on the `CMakeLists.txt` file located in the parent directory (`..`).

6. **Build the Test Executable:**
   ```bash
   make TestGDSIn
   ```
   This command compiles the `TestGDSIn` executable, which is used to test the GDS reader functionality.

7. **Run the Test:**
   ```bash
   cd src/odb/test/cpp/
   ./TestGDSIn <input.gds> <output.gds>
   ```
   This command executes the `TestGDSIn` program. Replace `<input.gds>` with the path to the GDS file you want to test and `<output.gds>` with the desired name for the output file. Make sure that the `input.gds` file is located at the root of the repository or specify its relative path from the `cpp` directory.
