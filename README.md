# QSV_AV1BatchEncodes
Hello, I don't know how to code. ChatGPT wrote everything.


PowerShell Video Encoding Script with HandBrake
This PowerShell script automates the process of encoding video files using HandBrake. It encodes all common video types in a source directory and outputs them in a destination directory.

Features
Encodes videos using QSV_AV1 codec, quality set to 24, variable frame rate, and the encoder preset set to quality
Retains the original resolution
Processes videos in alphabetical order
Logs encoded video names to prevent re-encoding
Checks for at least 100 GB free disk space before encoding each video
Sends an email and outputs a message in the terminal if there is insufficient disk space
Appends "_AV1" to the output file names
Prerequisites
Install HandBrake and note the path to HandBrakeCLI.exe.

Set up an email account and SMTP server to send email notifications when encoding stops due to insufficient disk space.

Usage
Open the script in a text editor and update the following configuration values:

$sourceFolder: The directory containing the video files to be encoded
$destinationFolder: The directory where encoded video files will be saved
$logFile: The log file to store encoded video names
$handBrakeCliPath: The path to HandBrakeCLI.exe on your system
$emailFrom: The email address to send notifications from
$emailTo: The email address to send notifications to
$emailSmtpServer: The SMTP server used to send email notifications
$emailSmtpPort: The SMTP server port used to send email notifications
$emailUsername: The username for the email account used to send notifications
$emailPassword: The password for the email account used to send notifications
Save your changes to the script.

Run the script by either:

Right-clicking on the script file and selecting "Run with PowerShell"
Opening PowerShell, navigating to the script's directory, and executing the script: .\script_name.ps1
The script will process the videos in the source directory and save the encoded output files to the destination directory. If there is insufficient disk space, the script will send an email notification and output a message in the terminal.

Notes
This script has been tested with HandBrake version 1.5.1 and PowerShell 5.1. Make sure to use compatible versions of HandBrake and PowerShell for proper execution.
Ensure you have sufficient disk space in the destination directory, as the script checks for at least 100 GB of free space before encoding each video.
