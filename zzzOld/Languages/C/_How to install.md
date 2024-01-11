## Windows Setup for C/C++ Development in VSCode:

1. **Download Visual Studio Code:**
   - Download and install Visual Studio Code (VSCode) from the official website: [VSCode Download](https://code.visualstudio.com/download).

2. **Install the C/C++ Extension:**
   - Open VSCode.
   - Go to the Extensions view by clicking on the square icon in the sidebar or using `Ctrl+Shift+X`.
   - Search for "C/C++" and click "Install" on the "C/C++" extension.

3. **Install the Code Runner Extension:**
   - In the Extensions view, search for "Code Runner" and install it.
   - To run code, use the shortcut `Ctrl+Alt+N`.
   - To stop running code, use the shortcut `Ctrl+Alt+M`.

4. **Download and Install GCC:**
   - Follow the installation instructions for GCC on Windows from the MSYS2 website: [MSYS2 Installation](https://www.msys2.org/).

5. **Install the Mingw-w64 Toolchain:**
   - Open a terminal within the MSYS2 environment.
   - Run the following command to install the Mingw-w64 toolchain, including the base development tools:
     ```bash
     pacman -S --needed base-devel mingw-w64-x86_64-toolchain
     ```

6. **Add GCC to PATH:**
   - Search for "path" in your Windows settings.
   - Click "Edit the system environment variables."
   - In the System Properties window, click the "Environment Variables" button.
   - Under "System variables," find the "Path" variable and click "Edit."
   - Click "New" and add the path to GCC: `C:\msys64\mingw64\bin`.
   - Click "OK" to save the changes.

7. **Verify GCC Installation:**
   - Open a Command Prompt (cmd) and run the following commands to check if GCC and related tools are installed correctly:
     ```bash
     gcc --version
     g++ --version
     gdb --version
     ```

8. **Configure VSCode for Integrated Terminal:**
   - In VSCode, go to File > Preferences > Settings.
   - Search for "Run Code Configuration" and select "Edit in settings.json."
   - Find the setting "Run In Terminal" and make sure it's set to run code in the integrated terminal.

9. **Create and Test a C File:**
   - Create a new C file in VSCode, e.g., `testing.c`.
   - Write a simple C program to test your setup, like the provided example:
     ```c
     #include <stdio.h>
     
     int main() {
         printf("Meow!");
         return 0;
     }
     ```
   - Save the file.

10. **Run C Code in VSCode:**
    - Open the `testing.c` file.
    - Use the "Run Code" feature by clicking the play button in the top-right corner of the editor or by using the shortcut `Ctrl+Alt+N`.
    - The output of your C program should appear in the integrated terminal.

