# Creating UML diagrams in VSCode using PlantUML

## Installing PlantUML

## VSCode setup
1. Navigate to the extensions (Ctrl+Shift+X) and search for "PlantUML". Alternatively, launch VS Code Quick Open (Ctrl+P), paste the following command: `ext install plantuml`, and press enter.
2. Install the PlantUML extension by jebbs.

## Getting started
1. Create a new file with the *.wsd, *.pu, *.puml, *.plantuml, or *.iuml format.

## Troubleshooting
1. Press the Windows key and search for "environment variables"
2. Open "Edit the system environment variables" or "Edit the .
3. In the window that pops up, click on "Enviroment Variables..."\
![image](https://github.com/SjoerdDevelops/vscode-setup-for-unity-development/assets/146742966/c93b2aee-d3c4-4094-81dd-7d00156bce23)
4. Under "User variables for <username>" select PATH
5. Check if the Graphiz binaries are added to the PATH. If not, add it. The binaries are usually installed at `C:\Program Files\Graphviz\bin`
