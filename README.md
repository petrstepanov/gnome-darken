# GNOME Darken

<figure>
  <img src="https://raw.githubusercontent.com/petrstepanov/gnome-darken/main/resources/gnome-darken.png" alt="Gnome Darken Icon" />
</figure>

Shell script that **enables dark theme** (window decorations) **for specific applications in GNOME** desktop environment. Script works with majority of applications: Chromium browser, Visual Studio Code, etc. However, some apps (like Krita, GIMP...) require more sophisticated approach that is not yet implemented.

## How to Use the Script

Clone the repository and source the `install.sh` script:
```
cd ~/Downloads
git clone https://github.com/petrstepanov/gnome-darken && cd gnome-darken
chmod +x ./*.sh
source ./gnome-set-dark-app.sh
```

In the file picker dialog select the application launcher that you want to apply the dark decorations to. Wait a few seconds before GNOME refreshes the list of launchers. Done.

<figure>
 <img src="https://raw.githubusercontent.com/petrstepanov/gnome-darken/main/resources/gnome-dark-decorations-for-visual-studio-code-vscode.png" alt="Dark window decorations applied to Visual Studio Code in GNOME desktop environment" />
</figure> 

Screenshot above demonstrates dark window decorations applied to Visual Studio Code application in GNOME desktop environment. At the same time Nautilus still has default light decorations.</figcaption>

If the dark theme was not successfully installed for your application please source the `gnome-set-dark-app.sh` script. Specify the same launcher that you used in the install script:
```
source ./gnome-unset-dark-app.sh
```

## Under the Hood

Script creates `./config-dark` folder in your home directory. It instructs application to be run with dark decorations in `./config-dark/gtk-3.0/settings.ini`.
```
[Settings]
gtk-application-prefer-dark-theme=true
```

Next, script overrides default application launcher located in `/usr/share/applications` by making a copy in your `/local/share/applications` folder. Modified launcher is diracted to use the `./config-dark` folder instead of the default `.config` by modifying the executable command `Exec=env XDG_CONFIG_HOME=/home/$USER/.config-dark <your-application>`.

Additionally the application alias is created in `.bashrc`. This ensures the application is launched with dark decorations even if use staqrted it from terminal.

Contributions are welcome.
