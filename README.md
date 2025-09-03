# powershell_cheatSheet

### List files & folders by last modified date (descending)
```ps
Get-ChildItem | Sort-Object LastWriteTime -Descending
```
### Top 5 most recently modified
```ps
Get-ChildItem | Sort-Object LastWriteTime -Descending | Select-Object -First 5
```
