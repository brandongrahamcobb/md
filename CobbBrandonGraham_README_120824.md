# Installing Python on Windows, Linux, and OSX

This guide explains how to install Python on Windows, Linux, and OSX using a script. Follow the steps below and refer to the provided images for visual assistance.

## Installation Instructions

### Windows

1. **Run the Installation Script**

   Open Command Prompt as an administrator. Run the following command to execute the script that will handle the Python installation:

   ```sh
   @powershell -Command "& {Start-Process PowerShell -ArgumentList '-NoProfile -ExecutionPolicy Bypass -File install_python_windows.ps1' -Verb RunAs}"
   ```

   ![Running Script on Windows](CobbBrandonGraham__030824.png)

2. **Verify Installation**

   After the script completes, verify the installation by running:

   ```sh
   python --version
   ```

   ![Verify Python Installation on Windows](CobbBrandonGraham__030824.png)

### Linux

1. **Run the Installation Script**

   Open a terminal and run the following command to execute the script that will handle the Python installation:

   ```sh
   bash <(curl -s https://example.com/install_python_linux.sh)
   ```

   ![Running Script on Linux](CobbBrandonGraham__030824.png)

2. **Verify Installation**

   After the script completes, verify the installation by running:

   ```sh
   python3 --version
   ```

   ![Verify Python Installation on Linux](CobbBrandonGraham__030824.png)

### OSX

1. **Run the Installation Script**

   Open Terminal and run the following command to execute the script that will handle the Python installation:

   ```sh
   bash <(curl -s https://example.com/install_python_osx.sh)
   ```

   ![Running Script on OSX](CobbBrandonGraham__030824.png)

2. **Verify Installation**

   After the script completes, verify the installation by running:

   ```sh
   python3 --version
   ```

   ![Verify Python Installation on OSX](CobbBrandonGraham__030824.png)

## Conclusion

By running the provided commands in your terminal or command prompt, the script will automatically handle the Python installation for Windows, Linux, and OSX. If you encounter any issues, refer to the troubleshooting section in the script documentation or seek help from the community.

