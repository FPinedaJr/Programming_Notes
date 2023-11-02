
1. **Install the .NET Framework:**
   - Visit the official .NET website (https://dotnet.microsoft.com/download) and download the .NET SDK.
   - Follow the installation instructions for your platform (Windows, macOS, or Linux).

2. **Install the C# Extension in VSCode:**
   - Open VSCode.
   - Go to the Extensions view by clicking on the square icon in the sidebar or using the shortcut `Ctrl+Shift+X`.
   - Search for "C#" in the Extensions marketplace.
   - Click "Install" on the "C# for Visual Studio Code" extension.

3. **Install the C# Dev Kit Extension:**
   - While still in the Extensions view in VSCode, search for "C# Dev Kit."
   - Click "Install" on the "C# Dev Kit" extension.

4. **Create a New Console Project:**
   - Open a terminal in VSCode (Terminal > New Terminal) or use the integrated terminal.
   - Navigate to the directory where you want to create your C# project.
   - Type the following command to create a new console project:
     ```
     dotnet new console
     ```
   - This will create template files for a C# project in your current directory. To use the old template files, add `--use-program-main` to the command.

5. **Run the C# Code:**
   - To compile and run the C# code, type the following command in the terminal:
     ```
     dotnet run
     ```

6. **Generate Assets for Build and Debug:**
   - To make it easier to build and debug your C# project, you can use the ".NET: Generate Assets for Build and Debug" command.
   - Open the command palette by pressing `Ctrl+Shift+P`.
   - Search for and select ".NET: Generate Assets for Build and Debug."

7. **Configure Launch Settings:**
   - Navigate to your project's `.vscode` folder and open the `launch.json` file.
   - Find the `"console"` setting and change it from `"internalConsole"` to `"externalTerminal"`. It should look like this:
     ```json
     "console": "externalTerminal"
     ```

8. **Run C# Code with F5:**
   - Save the `launch.json` file.
   - Now, you can run your C# code by pressing `F5` in VSCode, which will open an external terminal with your program's output.
