# Creating UML diagrams in VSCode using PlantUML
---
## Setting up PlantUML in VS Code
### Installing the PlantUML extention
1. Navigate to the extensions (Ctrl+Shift+X) and search for "PlantUML". Alternatively, launch VS Code Quick Open (Ctrl+P), paste the following command, and press enter:
```ext install plantuml```
2. Install the PlantUML extension by jebbs.

### Installing dependencies
The plugin for VS code has an integrated copy of plantuml.jar and Graphviz, so you are normally good to go. However, it also requires Java to run PlantUML. 
If you don't have Java installed, perform the following steps:
1. Navigate to the [Java Download page](https://www.java.com/en/download/manual.jsp).
2. Download the version corresponding with your operating system (e.g. "Windows Online").
3. Install Java using the downloaded installer.
4. if after you've installed Java it still prompts "java not installed", please add java bin path to the PATH environment variable.

Alternatively, you can download the latest plantuml.jar or install it using choco as shown below:
1. Open a Command Prompt as Admin.
2. Use the following command to intall Chocolatey. If Chocolatey is already installed, the command will fail: 
```
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
```
3. Use the following command to intall PlantUML:
```
choco install plantuml
```
#### Troubleshooting
When installing PlantUML using choco, sometimes an error occurs that states that the path to the Graphviz EXE Installer cannot be found (see image), possibly because it was removed by antivirus.  
![Screenshot 2023-11-16 102020 cropped](https://github.com/SjoerdDevelops/vscode-setup-for-unity-development/assets/146742966/6ab74ef8-145d-42ed-852e-c593774eb9bc)
To resolve the issues, manually install the required Graphviz dependecy:
1. Navigate to `https://graphviz.org/download/`
2. Download the EXE Installer for the required Graphviz version, e.g. `graphviz-9.0.0 (64-bit) EXE installer [sha256]`
3. Install Graphviz through the downloaded EXE Installer.

---
## Using the PlantUML extention
1. Create a new file with the *.wsd, *.pu, *.puml, *.plantuml, or *.iuml format.
2. Start creating your UML diagram. For reference, check [PlantUML Language Reference Guide](https://plantuml.com/guide).
3. Press Alt+D to start the PlantUML Preview Diagram to see the resulting diagram. 

Some useful features of the Diagram Preview:
- It auto updates whenever the contents of the file change.
- You can pan and zoom using common mouse, keyboard, and touchpad inputs.

