# powershell_cheatSheet

### List files & folders by last modified date (descending)
```ps
Get-ChildItem | Sort-Object LastWriteTime -Descending
```
