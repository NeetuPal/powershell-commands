# powershell_cheatSheet

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
### To run gh.exe directly
```ps
& "C:\Program Files\GitHub CLI\gh.exe" --version
```
