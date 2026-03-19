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
Create a directory named "my-folder"

## COMMAND AND OUTPUT
mkdir my-folder

<img width="666" height="394" alt="image" src="https://github.com/user-attachments/assets/12939aae-1015-40c1-88c9-41cfb85721f2" />


Remove the directory "my-folder"

## COMMAND AND OUTPUT
rmdir my-folder

<img width="438" height="292" alt="image" src="https://github.com/user-attachments/assets/a821e1cf-7c6c-4e21-9b2d-14b8a88f9db2" />

Create the file Rose.txt

## COMMAND AND OUTPUT
type nul > rose.txt

echo Rose flower is beautiful >> rose.txt

<img width="699" height="102" alt="image" src="https://github.com/user-attachments/assets/f39a5a61-9339-4f11-a613-c3cd72062892" />



Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
echo Hello > hello.txt

type hello.txt

<img width="497" height="193" alt="image" src="https://github.com/user-attachments/assets/d8b792dd-3423-42fd-b5bf-a31a39af6cb8" />

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
copy hello.txt hello1.txt

type hello1.txt

<img width="501" height="212" alt="image" src="https://github.com/user-attachments/assets/37fec9ae-6ec5-4000-b9a8-8009e661c326" />

Remove the file hello1.txt

## COMMAND AND OUTPUT
del hello1.txt

<img width="508" height="313" alt="image" src="https://github.com/user-attachments/assets/22629fbb-d9b1-4d90-8a79-cf95153ff72b" />


List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
dir hello1.txt


<img width="438" height="196" alt="image" src="https://github.com/user-attachments/assets/dbd87ffb-6f59-4125-9ab6-2ad6045e3d47" />

List out all the associated file extensions 

## COMMAND AND OUTPUT
assoc


<img width="452" height="337" alt="image" src="https://github.com/user-attachments/assets/f7a2435d-cf51-42c2-9b66-c5b2f63d625e" />


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
fc hello.txt rose.txt

<img width="482" height="262" alt="image" src="https://github.com/user-attachments/assets/40acedbe-ef4a-435d-bae3-c7db0586e833" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
```
@echo off
set name=Saveetha
echo Hello, %name%!
pause
```





## OUTPUT
<img width="405" height="88" alt="image" src="https://github.com/user-attachments/assets/1b58a902-987a-4979-bc94-b335a54b6185" />



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

<img width="662" height="206" alt="image" src="https://github.com/user-attachments/assets/2b3a5c3a-df57-4cf9-a049-47bbf4e73d10" />




Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause

```



## OUTPUT

<img width="424" height="185" alt="image" src="https://github.com/user-attachments/assets/fe810554-dde3-4989-846f-90382797ee5e" />



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

<img width="394" height="149" alt="image" src="https://github.com/user-attachments/assets/11999a2f-177a-454a-8ec7-66e995550905" />


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
<img width="540" height="421" alt="image" src="https://github.com/user-attachments/assets/4344f1bf-4f77-44b0-aeec-8276490844f7" />



# RESULT:
The commands/batch files are executed successfully.

