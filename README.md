https://packagecontrol.io/docs/syncing#git

Add alias to make it easy to navigate to config
alias sp="cd ~/Library/Application\ Support/Sublime\ Text/Packages/User/"


````
To properly sync your installed packages across different machines, you actually do not want to sync the whole Packages/ and Installed Packages/ folders. The reason for this is that some packages have different versions for different operating systems. By syncing the actual package contents across operating systems, you will possibly run into broken packages.

The proper solution is to install Package Control on all machines and then to sync only the Packages/User/ folder. This folder contains the Package Control.sublime-settings file, which includes a list of all installed packages. If this file is copied to another machine, the next time Sublime Text is started, Package Control will install the correct version of any missing packages.

Using Git
Many developers are familiar with Git, and it is a logical choice for keeping files in sync across machines if you don't mind a little manual work. There are a few things to keep in consideration when using Git:

If you use a service like GitHub and do not use a private repository, you may accidentally share license keys for any commercial packages you have purchased.
Certain files and folders in the Packages/User/ folder change regularly, so you may want to add them to a .gitignore file. There is really no harm in syncing these, however some of them change on an hourly basis, which may result in having to run more Git commands. Examples include:

Package Control.last-run
Package Control.ca-list
Package Control.ca-bundle
Package Control.system-ca-bundle
Package Control.cache/
Package Control.ca-certs/
```