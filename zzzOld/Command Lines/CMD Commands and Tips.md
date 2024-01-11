## Directories & Files

### Changing Directories
- `cd`: Change directory.
- `cd Desktop`: Change to the 'Desktop' directory.
- `cd..`: Move back one directory.
- `cd Desktop/videos`: Change to 'Desktop/videos'.
- `cd ../..`: Move back two directories.
- `cd "c:\Program Files\Meow"`: Change to an absolute path with spaces.

### Displaying Directories
- `dir`: List all files and directories.
- `dir Desktop`: List 'Desktop' contents.
- `dir /a`: Show hidden directories/files.
- `dir *.png*`: List files with the 'png' extension.
- `tree`: Display directories in a tree diagram.

### Opening Files
- `meow.png`: Open 'meow.png'.
- `path`: Search in directories listed in 'path'.

### Creating and Deleting Directories
- `mkdir nameHere`: Create a directory.
- `rmdir nameHere`: Remove a directory.
- `rmdir /s nameHere`: Delete directory and contents.

## Tips
1. Use `Tab` for autocompletion.
2. Use `cls` to clear the screen.
3. Use Up & Down keys to access previous commands.
4. Use `commandHere /?` for help.
5. Use Home & End keys to navigate lines.
6. Use `Ctrl + Left/Right` for word navigation.
7. Use `Ctrl + c` to stop running processes.
8. Focus on 'Program Files' and 'Users' directories.

## Drives
- `wmic logicaldisk get name`: List available drives.
- `E:`: Change to drive 'E:'.

## Colors
- `color /?`: Display color options.
- `color xy`: Change CMD colors (x=background, y=foreground).
- `color`: Reset to default.

## Files

### Attributes
- `attrib /?`: Show 'attrib' command options.
- `attrib`: Display file attributes.
- `attrib +h meow.txt`: Add 'hidden' attribute.
- `attrib +r -h meow.txt`: Add 'read-only' and remove 'hidden'.

### Deleting Files
- `del meow.txt`: Delete 'meow.txt'.

### Text Files
- `echo meow meow > meow.txt`: Create/overwrite file.
- `type meow.txt`: Display file content.
- `echo meooow >> meow.txt`: Append text.
- `dir > dir.txt`: Save command output.

### Rename, Copy, Move Files
- `rename cat meow`: Rename directory.
- `copy meow.txt meowFolder`: Copy file to directory.
- `copy meow.txt e:`: Copy file to drive root.
- `xcopy meowFolder catFolder`: Copy directory contents.
- `xcopy meowFolder catFolder /s`: Copy directory and subdirectories.

