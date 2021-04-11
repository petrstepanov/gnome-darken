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
source ./install.sh
```

In the file picker dialog select the application launcher that you want to apply the dark decorations to. Wait a few seconds before GNOME refreshes the list of launchers. Done.

gnome-dark-decorations-for-visual-studio-code-vscode.png


<figure>
 <img src="https://raw.githubusercontent.com/petrstepanov/gnome-darken/main/resources/gnome-dark-decorations-for-visual-studio-code-vscode.png" alt="Dark window decorations applied to Visual Studio Code in GNOME desktop environment" />
 <figcaption>Dark window decorations applied to Visual Studio Code application in GNOME desktop environment.</figcaption>
</figure> 

If the dark theme was not successfully installed for your application please source the `uninstall.sh` script. Specify the same launcher that you used in the install script.

Contributions are welcome.
