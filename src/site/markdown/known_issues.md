# Known Issues

## Problem opening the file in text editor on Linux systems

You may come across an issue on a Linux system where you have clicked Tools -> Open file in text editor and an exception has occurred (and the file not opened)

`java.lang.UnsupportedOperationException: The EDIT action is not supported on the current platform!`

The problem here is that we are using java.awt.Desktop utility class on Linux systems and I have found that that just does not work sometimes. At the moment I can't tell if if it's a GTK versioning issue or something else on the Linux system itself. In the meantime you will not be able to open the file automatically from the UI in your text editor, you will have to do that manually...sorry
