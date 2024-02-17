**For details and step-by-step guide watch the youtube video: [Interactive Application Deployment for Intune with PSADT](https://www.youtube.com/watch?v=phKeUzU-8qY&t=10s)** <br><br>
This is a modified PSADT to get you started with an interactive application installation. By default it prompts end-user to close Microsoft Excel and Word if they are open before the installation can continue. <br>
To use it, download the repository, replace your setup file with the "setup.exe" in the "Files" folder. <br>
Edit the "AppDeployToolkitConfig.xml" in the "AppDeployToolkit" folder for logging of the app installation. <br>
The line you need to edit is in the XML file is: <br>
<br>
<Toolkit_LogPath>$envProgramData\DemoLog\Win32</Toolkit_LogPath> <br>
<-- Log path used for Toolkit logging. Change the above ^ path to your desired Win32 app installation log  --> <br><br>
Use the [Microsoft Win32 Content Prep Tool](https://github.com/microsoft/Microsoft-Win32-Content-Prep-Tool) to create .intunewin from the toolkit. <br>
Upload the .intunewin file to Intune and you are ready to installation the application on the endpoints. <br>
