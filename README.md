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

The columns in the CSV file are as follows:

- what the row is about e.g. "N" for a node , or "#" for a comment
- Name of the OS, this has to be the name of the first release if the OS was renamed later
- Color; here please follow the current scheme (Dark Purple: Apple, Cyan: Microsoft, Red: Unix-like, Green: RSX/VMS-like, Dark Blue: DOS-like, Orange: AmigaOS-like, Brown: mainframe systems, Yellow: L4 microkernel family, Bright Purple: OSEK-compliant), note that for Unix there are two colours depending on whether the OS is still alive or not
- Parent: for forks of another OS, this has to EXACTLY match the name of the parent OS
- Start: first release date. Dates always have to be in the format YYYY.MM.DD (days and months are optional)
- Stop: end of support date for discontinued OS, leave blank otherwise. One issue here is that you cannot have a fork starting after the parent OS is already dead.
- Icon: ignore
- Description: ignore
- Namechange: if the OS was renamed, enter the new name here
- When: date of the name change
- Description: ignore
- then a couple more columns (Namechange, When, Description) for additional name changes

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
