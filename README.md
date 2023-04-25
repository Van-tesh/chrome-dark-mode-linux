# chrome-dark-mode-linux
This is a workaround fix to an issue where chrome does'nt enable dark mode on linux even when systemwide dark mode is enabled.
<br></br>Works on any linux distro.

## Steps
Run the shell script below in terminal
```
sudo sed -i 's/^Exec=\/usr\/bin\/google-chrome-stable$/& --enable-features=WebUIDarkMode --force-dark-mode/' /usr/share/applications/google-chrome.desktop
```
```
sudo sed -i 's/%U/--enable-features=WebUIDarkMode --force-dark-mode &/' /usr/share/applications/google-chrome.desktop
```
Restart Chrome.

## Note 
You have to run the shell script again after every chrome update.
Only works on chrome stable version.
