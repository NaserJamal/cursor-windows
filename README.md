# Cursor Context Menu Integration

This repository contains a registry script that adds Cursor to your Windows context menu, allowing you to open files and folders directly with Cursor.
![context](https://github.com/user-attachments/assets/bcc062b1-2e83-42b4-ade4-df009c06b6ed)

## Prerequisites

- Cursor must be installed on your system.
- The default installation path for Cursor is assumed to be `%LOCALAPPDATA%\Programs\cursor\Cursor.exe`.

## Installation

1. Download the `add_cursor_to_context_menu.reg` file from this repository.
2. Double-click the downloaded `.reg` file.
3. Windows will show a security warning. Click "Run" to continue.
4. A User Account Control dialog may appear. Click "Yes" to allow the changes.
5. Windows will ask if you're sure you want to add the information to the registry. Click "Yes" to confirm.
6. You should see a message confirming that the keys and values have been successfully added to the registry.

## What This Does

After running the script:

- A new "Open with Cursor" option will appear in your context menu when you right-click on:
  - Any file
  - The background of any folder

- Clicking this option will open the selected file or folder in Cursor.

## Customization

If Cursor is installed in a different location on your system, you'll need to modify the paths in the `.reg` file before running it. Replace `%LOCALAPPDATA%\\Programs\\cursor\\Cursor.exe` with the correct path to your Cursor executable.

## Uninstalling

To remove Cursor from your context menu:

1. Open the Registry Editor (regedit.exe)
2. Navigate to and delete the following keys:
   - `HKEY_CLASSES_ROOT\*\shell\Open with Cursor`
   - `HKEY_CLASSES_ROOT\Directory\Background\shell\Open with Cursor`

Alternatively, you can create an uninstall script by copying the content of the install script and replacing `HKEY_CLASSES_ROOT` with `HKEY_CLASSES_ROOT\-`.

## Note

Modifying the Windows registry can affect your system's behavior. While this script is designed to be safe, it's always a good practice to back up your registry before making changes.

## License

This project is open source and available under the [MIT License](LICENSE).
