## README 
https://packagecontrol.io/docs/syncing#git

Syncs the `Packages/User/` folder in the Sublime Text Application folder. Add alias to make it easy to navigate to config `alias sp="cd ~/Library/Application\ Support/Sublime\ Text/Packages/User/"`.

- `Package Control.sublime-settings` lists all the installed packages.
- Use `Default.sublime-mousemap` to bind mouse maps (not included initially in ST)

Certain files and folders in the Packages/User/ folder change regularly, so you may want to add them to a `.gitignore` file. There is really no harm in syncing these, however some of them change on an hourly basis, which may result in having to run more Git commands. Examples include:

```
Package Control.last-run
Package Control.ca-list
Package Control.ca-bundle
Package Control.system-ca-bundle
Package Control.cache/
Package Control.ca-certs/
```