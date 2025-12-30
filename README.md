![Tree](https://raw.githubusercontent.com/Carlos834777/hurd-family-tree/5b9a00235a050bfcda0f870f69c19d6646b46b49/HurdTimeline.svg)

### Installation
gnuclad can be installed via flatpak or snap.

Snap:
````
sudo snap install gnuclad
````

Flatpak:
````
flatpak install flathub net.launchpad.Gnuclad
````

You can also use the [official Debian binary](https://launchpad.net/gnuclad/+download).

### How to edit the .CSV file

The CSV file can be edited with LibreOffice Calc, for example. It is important here that all lines are formatted as text when opening the CSV file in order to prevent, for example, a date from being automatically adjusted. If you open in in Microsoft Excel, make sure to save it as "CSV (Comma delimited") (note there are multiple variants of the CSV format in Excel, you must use this one).

### How to create the .SVG file

Once the changes have been made to the CSV file, the SVG file can be generated with the following command:
````
gnuclad file.csv output.svg config.conf
````

or for the Flatpak:
````
flatpak run net.launchpad.Gnuclad file.csv output.svg config.conf
````

Examples:
````
gnuclad HurdTimeline.csv HurdTimeline.svg HurdTimeline.conf
````
````
flatpak run net.launchpad.Gnuclad HurdTimeline.csv HurdTimeline.svg HurdTimeline.conf
````
### Other

This was heavily inspired by Eylenburg's [os-family-tree](https://github.com/eylenburg/os-family-tree) and the [Linux Distribution Timeline](https://commons.wikimedia.org/wiki/File:Linux_Distribution_Timeline.svg)
