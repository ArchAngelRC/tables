
Cheat Engine tables for NSFW Games

Feel free to share, edit or modify these tables.


## Naming Scheme

For most files, where applicable, I'm doing the following scheme:

`Game Name and Version (DLsiteid)(last 10 characters of game binary MD5).CT`

Ex: `Game v1.23 (RE123456)(1234567890).CT`

**Note**: I'm using the MD5 part mostly for myself to verify I have the right file at a glance. Truncated for file name size. Not concerned about collisions.

### Generate truncated MD5 via PowerShell (copy+paste into prompt):
```powershell
$ans = read-host "Paste full game .exe path"
$ans = $ans -replace '"', ""
$file = ls $ans
$($(Get-FileHash $file.FullName -Algorithm MD5).Hash).substring(22,10)
 
```
