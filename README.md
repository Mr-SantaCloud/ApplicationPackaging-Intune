For details and step-by-step guide watch the youtube video: https://www.youtube.com/watch?v=phKeUzU-8qY&t=10s
This is a modified PSADT to get you started with an interactive application installation. By default it prompts end-user to close Microsoft Excel and Word before the installation can continue, if they are open.
To use it, download the repository, replace your setup file with the "setup.exe" in the "Files" folder.
Edit the "AppDeployToolkitConfig.xml" in the "AppDeployToolkit" folder for logging of the app installation.
The line you need to edit is in the XML file is:
<Toolkit_LogPath>$envProgramData\DemoLog\Win32</Toolkit_LogPath>
<!-- Log path used for Toolkit logging. Change the above ^ path to your desired Win32 app installation log  -->

Use the "Microsoft Win32 Content Prep Tool" https://github.com/microsoft/Microsoft-Win32-Content-Prep-Tool to convert your script to .intunewin file.
Upload the .intunewin file to Intune and you are ready to installation the application on the endpoints.
