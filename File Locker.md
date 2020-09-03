# Filelocker

There are many file locker applications available over the internet. 
We need to pay for some of the applications available.
 Here in this Video let us discuss on how to create a file locker without installing any software in your windows machine. You may seem this method bit difficult. But, secure than any other file locker software as this method is from Microsoft. 

There are lot of Text editing apps like Atom, Notepad++, WordPad, Vim, Brackets, Notepad etc.,

So, Open your Text editing app. 
Here I will be using Notepad

 
Step 1:

Copy the following code and paste it into notepad

cls
@ECHO OFF
title Folder Locker
if EXIST "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}" goto UNLOCK
if NOT EXIST Locker goto MDLOCKER
:CONFIRM
echo Are you sure u want to Lock the folder(Y/N)
set/p "cho=>"
if %cho%==Y goto LOCK
if %cho%==y goto LOCK
if %cho%==n goto END
if %cho%==N goto END
echo Invalid choice.
goto CONFIRM
:LOCK
ren Locker "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"
attrib +h +s "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"
echo Folder locked
goto End
:UNLOCK
echo Enter password to Unlock folder
set/p "pass=>"
if NOT %pass%==type your password here  goto FAIL
attrib -h -s "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"
ren "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}" Locker
echo Folder Unlocked successfully
goto End
:FAIL
echo Invalid password
goto end
:MDLOCKER
md Locker
echo Locker created successfully
goto End
:End


Step 2:
Make sure that you will replace "type your password here" with your own password in the code.

Now Save Notepad as FolderLock.bat in the desired location.


Step 3:
Now double click on FolderLock.bat file then a new folder named as Locker is created.



Step 4:
Save your files in Locker folder



Step 5:
Again, double-click on the FolderLock.bat, a Command prompt window pops up.



Step 6:
To lock the folder(Locker) press "y " in the prompt to lock and hide the folder.








If you want to unlock the folder to access that folder; please double click on FolderLock.bat. You will be asked to enter the password.




Please enter the password and press enter.
The Locker folder gets unlocked and you can access the files that you were in need of.



Conclusion:
Using the above steps, you can lock the folder and unlock it using Notepad.
