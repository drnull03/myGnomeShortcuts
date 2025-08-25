# myGnomeShortcuts

A personal collection of custom keyboard shortcuts for the GNOME desktop environment, designed to enhance productivity.

## Getting Started

These instructions will help you apply my custom shortcuts to your GNOME setup using `dconf`.

###  Important: Back Up Your Existing Shortcuts

Before applying these new shortcuts, it is **highly recommended** to back up your current configuration. This allows you to easily restore your original settings if you decide to revert the changes.

Open a terminal and run the following command to create a backup file named `gnome-shortcuts-backup.dconf` in your home directory:

```bash
dconf dump /org/gnome/settings-daemon/plugins/media-keys/ > ~/gnome-shortcuts-backup.dconf
```

### Applying the Shortcuts

First, clone this repository to your local machine. Once cloned, navigate into the `myGnomeShortcuts` directory in your terminal.

From inside the repository's directory, run the following command to load the keybindings from the `my-gnome-shortcuts.dconf` file:

```bash
dconf load /org/gnome/settings-daemon/plugins/media-keys/ < my-gnome-shortcuts.dconf
```

Your new shortcuts should now be active.

## Available Keybindings

Here is a summary of the shortcuts included in this configuration:

| Shortcut              | Action                | Command                    |
| --------------------- | --------------------- | -------------------------- |
| `Super + E`           | Browse Files          | `nautilus`                 |
| `Ctrl + Alt + ]`      | Suspend System        | `systemctl suspend`        |
| `Ctrl + Alt + \`      | Power Off System      | `poweroff`                 |
| `Ctrl + Alt + [`      | Reset Display Manager | `systemctl restart gdm3`   |
| `Ctrl + Alt + '`	| Reset Network Service | `systemctl restart NetworkManager` |

Going to add way more shortcuts in the future stay tuned !

## Future Keybindings and Suggestions

Feel free to contribute your own favorite shortcuts! You can suggest new keybindings or improvements in two ways:

1.  **Open an Issue:** Propose a new shortcut or a change by opening an issue in the repository. This is a great way to start a discussion.
2.  **Submit a Pull Request:** Fork the repository, add your custom keybindings to the `my-gnome-shortcuts.dconf` file, and submit a pull request with your changes.


## Restoring Your Backup

If you want to revert to your old settings, you can load the backup file you created earlier with this command:

```bash
dconf load /org/gnome/settings-daemon/plugins/media-keys/ < ~/gnome-shortcuts-backup.dconf
```


