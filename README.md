# Cryptage-and-hide

------- à coller dans le doc texte -------


cls
@ECHO OFF
title Folder security
if EXIST -Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}- goto UNLOCK
if NOT EXIST security goto MDLOCKER
:CONFIRM
echo Are you sure you want to lock the folder(Y-N)
set-p -cho=--
if %cho%==Y goto LOCK
if %cho%==y goto LOCK
if %cho%==n goto END
if %cho%==N goto END
echo Invalid choice.
goto CONFIRM
:LOCK
ren security -Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}-
attrib +h +s -Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}-
echo Folder locked
goto End
:UNLOCK
echo Enter password to unlock folder
set-p -pass=--
if NOT %pass%== tonmotdepasse goto FAIL
attrib -h -s -Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}-
ren -Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}- security
echo Folder Unlocked successfully
goto End
:FAIL
echo Invalid password
goto end
:MDLOCKER
md security
echo security created successfully
goto End
:End

 all that you could change the extension to.Bat extension 
 follow this video :
https://www.youtube.com/watch?v=2xf1EQuv6SU
