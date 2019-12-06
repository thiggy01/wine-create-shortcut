# wine-create-shortcut

This is a script which creates shortcuts for Windows programs installed with Wine on Gnome applications menu.It extracts 
the icon from the submited .exe file and convert it to .png files of different qualities. Then, it select the best image
and create a .deskop launcher file with with some inputs from the user and link it to a shortcut file in applications
menu folder.

## Installing

Download and change its execution permission with the following commands:

    curl -L -O github.com/thiggy01/wine-create-shortcut/raw/master/wine-create-shortcut
    chmod +x wine-create-shortcut
    
## Dependencies

You need to have wrestool, convert and zenity packages installed to be able to create the Windows application shortcut.
So, check if they are install in your system with `dpkg -l icoutils imagemagick zenity | tail -n 3`. If some of them
don't show up, you have to install them with `sudo apt install <package-name1> <pagacke-name2> ...` for debian based
distributions.

## Usage

Run the scrip with this command: `./wine-create-shortcut path/to/app.exe`. It will display a lot of messages showing what
it is doing until it is done. After that, you should see the shortcut appearing on the applications menu of Gnome
when you search for it.
