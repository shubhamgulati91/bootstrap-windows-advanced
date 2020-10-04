# [Setup](README.md) customization

## All the softwares you need with Chocolately

All the freeware software can be installed using [Chocolately](https://chocolatey.org/). The list of softwares to install is located to [configs/chocopkg.txt](https://github.com/shubhamgulati91/windows-final-setup/blob/master/configs/chocopkg.txt) and it is installed using a priority index that ranges from 1 to 3. You can freerly add and remove any package you want.

You can add your favourite softwares using [Chocolately search](https://chocolatey.org/search) and adding them into `chocopkg`, or you can update all your softwares launching a `choco upgrade all -y`.

## Enable and disable Windows features

In the [main set-up script](https://github.com/shubhamgulati91/windows-final-setup/blob/master/setup.psm1) there is a comprehensive list of the actions performed to disable and enable specific Windows features that you might or might not need.

To get a list of all your currently enabled Windows features, call `Get-WindowsOptionalFeature -Online` from PowerShell.

## UI, taskbar and multi-monitor enhancements

In the [main set-up script](https://github.com/shubhamgulati91/windows-final-setup/blob/master/setup.psm1) there is a comprehensive list of the actions performed to tweak the UI, like hiding People and Cortana buttons, enabling Dark Mode, reducing the size of the taskbar, disable the Administrator security prompt, disabling Aero Shaking and many more.

## Uninstall pre-installed Windows Apps

Because we do not need Candy Crush Saga.

## Install Ubuntu

Install the latest LTS version of Ubuntu using WSL 2.0, automatically.

## Disable telemetry

The script will call a script from [another repository](https://github.com/W4RH4WK/Debloat-Windows-10/) (which I admit, it is potentially unsafe) to disable Telemetry. The source code of the script is located to [Debloat Windows 10 repository](https://github.com/W4RH4WK/Debloat-Windows-10/blob/master/scripts/block-telemetry.ps1).

## Start layout

It is possible to restore a previously back-up start layout. The [start layout configuration](https://github.com/shubhamgulati91/windows-final-setup/blob/master/configs/start-layout.xml) it is just an XML file that will be read, from the current User folder, the very first time that the specified user logs in, when the start layout database does not exists or is corrupted. Once that the start layout is installed, the user has to log-out and log-in.

## Visual Studio Code extensions list

All the extensions specified into [configs/vscode-extensions.txt](https://github.com/shubhamgulati91/windows-final-setup/blob/master/configs/vscode-extensions.txt) will be automatically installed to Visual Studio Code.

To retrieve the ID of the extension, just go to [Visual Studio Marketplace](https://marketplace.visualstudio.com) and retrieve, from the url, the value of `itemName`.

eg. for Python plugin, `https://marketplace.visualstudio.com/items?itemName=ms-python.python`, the extension ID is `ms-python.python`.

To export the current start layout, open PowerShell and enter `Export-StartLayout start-layout.xml`.

## PowerShell and Command Prompt color scheme

By default, [Dracula color theme](https://github.com/shubhamgulati91/windows-final-setup/blob/master/configs/Dracula-ColorTool.itermcolors) is installed by the [set-up](https://github.com/shubhamgulati91/windows-final-setup/blob/master/setup.psm1) script. The choice is because it is the most similar color scheme to the original, while keeping the text readable on LCD/LED screens. Infact, the old color scheme is fully readable only on CRT screens!

More color schemes can be found on [Microsoft's ColorTool GitHub page](https://github.com/microsoft/terminal/tree/master/src/tools/ColorTool/schemes).
