# Creating UML diagrams in VSCode using PlantUML

## Installing PlantUML
1. Open a Command Prompt as Admin.
2. Use the following command to intall Chocolatey. If Chocolatey is already installed, the command will fail: 
```
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
```
3. Use the following command to intall PlantUML:
```
choco install plantuml
```

## VSCode setup
1. Navigate to the extensions (Ctrl+Shift+X) and search for "PlantUML". Alternatively, launch VS Code Quick Open (Ctrl+P), paste the following command, and press enter:
```ext install plantuml```
3. Install the PlantUML extension by jebbs.

## Getting started
1. Create a new file with the *.wsd, *.pu, *.puml, *.plantuml, or *.iuml format.
2. Start creating your UML diagram. For reference, check [PlantUML Language Reference Guide](https://plantuml.com/guide).
3. Press Alt+D to start the PlantUML Preview Diagram to see the resulting diagram. 

Some useful features of the Diagram Preview:
- It auto updates whenever the contents of the file change.
- You can pan and zoom using common mouse, keyboard, and touchpad inputs.

## Troubleshooting
### Error: Path to the Graphviz Install Exe not found
A common error that occurs when installing PlantUML using Chocolatey is depicted in the image below:\
![Screenshot 2023-11-16 102020 cropped](https://github.com/SjoerdDevelops/vscode-setup-for-unity-development/assets/146742966/6ab74ef8-145d-42ed-852e-c593774eb9bc)
This error may indicate that the downloaded files for Graphviz are removed by security software. \
To resolve the issues, manually install the required Graphviz dependecy:
1. Navigate to `https://graphviz.org/download/`
2. Download the EXE Installer for the required Graphviz version, e.g. `graphviz-9.0.0 (64-bit) EXE installer [sha256]`
3. Install Graphviz through the downloaded EXE Installer.

### Unstested
1. Press the Windows key and search for "environment variables"
2. Open "Edit the system environment variables" or "Edit the .
3. In the window that pops up, click on "Enviroment Variables..."\
![image](https://github.com/SjoerdDevelops/vscode-setup-for-unity-development/assets/146742966/c93b2aee-d3c4-4094-81dd-7d00156bce23)
4. Under "System Variables" click "New...".
5. In the "Variable name" field, type "GRAPHVIZ_DOT"
6. In the "Variable value" field, insert the path to the Graphviz dot.exe. This is usually `C:\Program Files\Graphviz\bin\dot.exe`.
