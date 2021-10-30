# onScript: about...
This repository stores bash scripts that
I felt were helpful especially when dealing
in robotics and other opensource software.
It is especially handy in recording longer bash commands.
The goal of this repository is to take complex commands,
and put them in scripts preventing the need for google searches.

# Notes on using script
* Scripts are kind of lame at the moment.
    - They have to be coppied into home directory
    - most likely you'll have to edit some based on its documentaition
    - And all bash scripts must be called as follows: `bash script` where `script` is a stand in for the script you wish to call.

* installing a script into your system is as easy as: `cp {cloned_repository_name}/{script_name} ~`


# Pull policy
* Also if I bother to look in the bash file and see no comments/documentaitions I'm rejecting the request.

# convert2Mp4
* This script requires you have ffmpeg installed.
* It takes the path to a video file and returns an .mp4 version.

## These functions have to do with sourceing your ROS workspaces
**WARNING**
* Some of these scripts are dangerous if you don't follow precautions and follow instructions.
* Could result in loosing your .bashrc file.
* This warning remains in effect until I can improve the scripts.
* These scripts edit your .bashrc.  In order to look at your .bashrce use this command: `cat .bashrc`

# sourceWS
* This script sources a workspace that you specify.  
* It follows this form: `bash sourceWS {$name_of_workspace}`

# wsSourceRemove
* This script is suppose to remove the line that sources your workspace after finishing a project.
* *NOTE* 
    - All it does is remove the last line of the bashrc and does not target specific files.
    - It does not target added source lines.
    - This means you should run this script before starting a new project.
    - Also it creates a backup of the .bashrc incase you mess up, but it does this every time the script is run. This means you can eventually reduce your .bashrc down to nothing.


# buBashrc
* This script creates a backup of .bashrc file.
* This script is executed in `wsSourceRemove` and can be run on its own.

# rBashrc
* This script copies your backup .bashrc onto your .bashrc