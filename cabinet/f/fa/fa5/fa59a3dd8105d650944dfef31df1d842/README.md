# Using Bash in Flatpak VSCode

Because Flatpak VSCode on Linux is sand-boxed it isn’t possible to
access many of the native system commands, including running Bash in the
integrated terminal. To work around this the following code can be
appended to the settings.json file:

    "terminal.integrated.defaultProfile.linux": "bash",
    "terminal.integrated.profiles.linux": {
      "bash": {
        "path": "/usr/bin/env",
        "args": ["--", "flatpak-spawn", "--host", "--env=TERM=xterm-256color", "bash"]
      }
    }
