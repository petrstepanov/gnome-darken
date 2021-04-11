# GNOME Darken

<figure>
  <img src="https://raw.githubusercontent.com/petrstepanov/gnome-darken/main/resources/gnome-darken.png" alt="Gnome Darken Icon" />
</figure>

Shell script that enables dark window decorations for specific application in GNOME desktop environment. Script does work with majority of applications: Chromium browser, Visual Studio Code, etc. However, some apps require more sophisticated approach that is not yet implemented.

## How to Use the Script

Clone the repository and source the `install.sh` script:
```
cd ~/Downloads
git clone https://github.com/petrstepanov/gnome-darken && cd gnome-darken
chmod +x ./*.sh
source ./install.sh
```

In the file picker dialog select the application launcher that you want to apply the dark decorations to. Wait a few seconds before GNOME refreshes the list of launchers. Done.

If the dark theme was not successfully installed for your application please source the `uninstall.sh` script. Specify the same launcher that you used in the install script.

Contributions are welcome.
