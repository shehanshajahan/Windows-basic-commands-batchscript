# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file
Save each script in a file with a .bat extension.
Ensure you have the necessary permissions to perform the operations.
Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 

# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "MyLab" on the desktop.


## COMMAND AND OUTPUT

```
mkdir %userprofile%\Desktop\MyLab
```

![ex8_1](https://github.com/user-attachments/assets/2a74a29c-349c-47e2-9ebc-a844290977f2)


Change to the "MyLab" directory and create an empty text file named "MyFile.txt" inside it.


## COMMAND AND OUTPUT

```
cd %userprofile%\Desktop\MyLab
```
![ex8_2](https://github.com/user-attachments/assets/7ffcaa76-350c-4f41-8e6f-5ca348e720c0)


```
type nul > MyFile.txt
```

![ex8_3](https://github.com/user-attachments/assets/6b96d213-fd30-41ab-a20b-f21d3b4f60f7)


List the contents of the "MyLab" directory.


## COMMAND AND OUTPUT

```
dir %userprofile%\Desktop\MyLab
```

![ex8_4](https://github.com/user-attachments/assets/3d46b18d-ff34-4150-8f2f-129750e157ec)


Copy "MyFile.txt" to a new folder named "Backup" on the desktop.

## COMMAND AND OUTPUT

```
mkdir %userprofile%\Desktop\Backup
```

![ex8_5](https://github.com/user-attachments/assets/edaf0b58-97d1-4360-a59f-618d341c2f4a)


```
copy MyFile.txt %userprofile%\Desktop\Backup
```

![ex8_6](https://github.com/user-attachments/assets/e48ec061-4490-46a2-a025-3d4ef660ccd8)


Move the "MyLab" directory to the "Documents" folder.

## COMMAND AND OUTPUT

```
mkdir %userprofile%\Desktop\Documents
```
```
move MyLab Documents
```

![ex8_7](https://github.com/user-attachments/assets/65a049fa-474f-4ace-b241-14dd73d36696)


## Exercise 2: Advanced Batch Scripting
Create a batch script named "BackupScript.bat" that creates a backup of files with the ".docx" extension from the "Documents" folder to a new folder named "DocBackup" on the desktop.

## COMMAND

```
@echo off
mkdir %userprofile%\Desktop\DocBackup
copy %userprofile%\Documents\*.docx %userprofile%\Desktop\DocBackup
echo Backup completed successfully!
```

## OUTPUT

![ex8_8](https://github.com/user-attachments/assets/2d4f05ac-265c-4d53-bd73-81bad6905d34)


## COMMAND
```
  @echo off
  mkdir %userprofile%\Desktop\DocBackup
  copy %userprofile%\Documents\*.docx %userprofile%\Desktop\DocBackup
  del %userprofile%\Documents\*.docx
  echo Backup and deletion completed successfully!
```
## OUTPUT

![image](https://github.com/user-attachments/assets/bf63b7f0-86ba-40ca-adc3-3711f05eb336)


# RESULT:
The commands/batch files are executed successfully.

