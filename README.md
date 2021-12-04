# My Configuration Stuff
This that I use to hold my vscode, powershell and other stuff configuration files

## Powershell Customization
- Download Caskaydia Cove Nerd Font Complete from [Nerd Fonts]
- Install [Oh-My-Posh]
- Install [Terminal-Icons]
- Install [PSReadLine]

```powershell
Invoke-WebRequest -Uri https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/CascadiaCode.zip -OutFile CascadiaCode.zip
Expand-Archive .\CascadiaCode.zip -DestinationPath CascadiaCode
Remove-Item CascadiaCode.zip
```
Drag and drop the CascadiaCode/*.ttf files to C:\Windows\Fonts
Under setting>powershell>apearence, select "CaskaydiaCove NF"

Install Modules
```powershell
winget install JanDeDobbeleer.OhMyPosh
Install-Module -Name Terminal-Icons -Repository PSGallery
Install-Module PSReadLine -AllowPrerelease -Force
```

Download config Files and use them
```powershell
Invoke-WebRequest -Uri https://raw.githubusercontent.com/nicolasCavalcante/config-stuff/master/my_oh_my_posh.json -OutFile ~/my_oh_my_posh.json
New-Item $PROFILE -Force
Invoke-WebRequest -Uri https://raw.githubusercontent.com/nicolasCavalcante/config-stuff/master/profile.prof -OutFile $PROFILE
. $PROFILE
```


[Nerd Fonts]: https://www.nerdfonts.com/

[Oh-My-Posh]: https://ohmyposh.dev/

[Terminal-Icons]: https://github.com/devblackops/Terminal-Icons

[PSReadLine]: https://docs.microsoft.com/en-us/powershell/module/psreadline/about/about_psreadline?view=powershell-7.2

Inpired by (copied from) [Scott-Hanselman-Ultimate-Powershell](https://www.hanselman.com/blog/my-ultimate-powershell-prompt-with-oh-my-posh-and-the-windows-terminal)

