# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
`
Create a directory named "my-folder"
`
<img width="817" height="157" alt="image" src="https://github.com/user-attachments/assets/bce2aa8f-e27e-4afd-b34d-ec7bee4707c4" />

## COMMAND AND OUTPUT

Remove the directory "my-folder"

<img width="565" height="76" alt="image" src="https://github.com/user-attachments/assets/ea5ecb66-852d-4d66-bc70-feba93ed1a99" />

## COMMAND AND OUTPUT
``
Create the file Rose.txt
``
<img width="1041" height="222" alt="image" src="https://github.com/user-attachments/assets/39bac3d0-720c-4ed8-b368-db7214bab3c7" />

## COMMAND AND OUTPUT
``
Create the file hello.txt using echo and redirection
``
<img width="1020" height="172" alt="image" src="https://github.com/user-attachments/assets/8ea0f7c9-5353-4399-b84c-212b1e7ae5de" />

## COMMAND AND OUTPUT
``
Copy the file hello.txt into the file hello1.txt
``
<img width="897" height="105" alt="image" src="https://github.com/user-attachments/assets/e72641dc-1142-4bf8-a41e-bb88e1767eeb" />

## COMMAND AND OUTPUT

Remove the file hello1.txt

<img width="680" height="71" alt="image" src="https://github.com/user-attachments/assets/2e253acb-4c97-4cb2-b860-efc39862d236" />

## COMMAND AND OUTPUT
``
List out the file hello1.txt in the current directory
``
<img width="956" height="258" alt="image" src="https://github.com/user-attachments/assets/155af7ad-a7e3-4795-9695-7445b47761df" />

## COMMAND AND OUTPUT
``
List out all the associated file extensions 
``
<img width="750" height="791" alt="image" src="https://github.com/user-attachments/assets/ef58ca39-736d-49d8-a9a9-3a58b10e276f" />

## COMMAND AND OUTPUT
``
Compare the file hello.txt and rose.txt
``
<img width="960" height="293" alt="image" src="https://github.com/user-attachments/assets/081e60bd-e79d-43e9-afd9-71de18625d13" />

## COMMAND AND OUTPUT

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
```
@echo off
set name=John
echo Hello, %name%!
pause
```

## OUTPUT

<img width="523" height="168" alt="image" src="https://github.com/user-attachments/assets/4a714ba3-e029-4e9b-9e35-679c4546e440" />


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
```
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)

:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause
```
## OUTPUT
<img width="825" height="310" alt="image" src="https://github.com/user-attachments/assets/76bdc233-42c5-4bbf-929b-aa97ea6425a3" />



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```

## OUTPUT
<img width="543" height="260" alt="image" src="https://github.com/user-attachments/assets/2f75b93b-12be-4928-9b54-92a07aa2cc63" />




Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```
## OUTPUT
<img width="733" height="311" alt="image" src="https://github.com/user-attachments/assets/e4b64fdf-78bb-460a-8d0e-3fe6dce035bb" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
```
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pause
```

## OUTPUT
<img width="772" height="532" alt="image" src="https://github.com/user-attachments/assets/4e9a0e23-08dd-49f3-8606-7826edd239d3" />



# RESULT:
The commands/batch files are executed successfully.

