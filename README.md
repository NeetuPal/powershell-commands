# powershell-commands

### List files & folders by last modified date (descending)
```ps
Get-ChildItem | Sort-Object LastWriteTime -Descending
```
### Top 5 most recently modified
```ps
Get-ChildItem | Sort-Object LastWriteTime -Descending | Select-Object -First 5
```
### Include subfolders (recursive)
```ps
Get-ChildItem -Recurse | Sort-Object LastWriteTime -Descending | Select-Object FullName, LastWriteTime -First 10
```
### ii = Invoke-Item, like double-clicking in Explorer
```ps
ii "C:\Program Files\GitHub CLI\"
```
### To check if gh.exe exists in that folder
```ps
dir "C:\Program Files\GitHub CLI\"
```
### That lists only the immediate folders in Downloads
```ps
Get-ChildItem -Path 'C:\Users\Naresh Pal\Downloads\' -Directory
```
### To run gh.exe directly
```ps
& "C:\Program Files\GitHub CLI\gh.exe" --version
```
### Find where gh is installed
```ps
where.exe gh
```
### Install (or update) AWS CLI v2 on Windows using the MSI installer directly from the URL.
```ps
msiexec.exe /i https://awscli.amazonaws.com/AWSCLIV2.msi
```
### Simple view (all drives) 
```ps
Get-PSDrive -PSProvider FileSystem
```
### Delete zip file without confirmation
```ps
Remove-Item .\terraform-project.zip -Force
```
### Extract a .zip file
```ps
Expand-Archive -Path .\terraform-project.zip -DestinationPath .\terraform-project -Force
```
### Move the file into the inner folder
```ps
Get-ChildItem .\terraform-project
```
