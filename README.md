# 🦴 SFML skeleton

![Release](https://img.shields.io/badge/Release-v1.0-blueviolet)
![Language](https://img.shields.io/badge/Language-C%2B%2B-0052cf)
![Size](https://img.shields.io/badge/Size-16Ko-f12222)
![Open Source](https://badges.frapsoft.com/os/v2/open-source.svg?v=103)

<br>

This repository is a **skeleton C++ project**.

<br>

<p align="center">
	<img src="https://upload.wikimedia.org/wikipedia/commons/1/18/ISO_C%2B%2B_Logo.svg" width="200">
</p>

<br>

# 📋 Summary

* **[📋 Summary](#-summary)**
* **[🛠️ Install](#%EF%B8%8F-install)**
	* [🪟 Windows](#-windows)
	* [🐧 Unix](#-unix)
	* [💎 Using VS Code](#-using-vs-code-recommended) *(recommended)*
* **[🙏 Credits](#-credits)**

<br>

# 🛠️ Install

I recommend using **[VS Code](#-using-vs-code-recommended)**.

<br>

## 🪟 Windows

### What you need

* **[CMake](https://cmake.org/)**

* A compiler :

	* **[Visual Studio](https://visualstudio.microsoft.com/)** (the software or the compiler only) *(recommended)*

	* **[MinGW](https://www.mingw-w64.org/)** *(not recommended)*

### How to compile it?

* **Visual Studio** *(recommended)* :

	* Run the **[vs32_run.bat](https://github.com/angeluriot/Skeleton/blob/master/vs32_run.bat)** *(for 32 bits)* or the **[vs64_run.bat](https://github.com/angeluriot/Skeleton/blob/master/vs64_run.bat)** *(for 64 bits)* to create the project

	* Then run the file in **.sln** in the build folder

*(Run the .bat file again each time you add or remove a file)*

* **MinGW** *(not recommended)* :

	* Open a terminal in the project root and type : `.\mingw_run.bat` to create and compile the project

	* Then type : `.\build\App.exe` to run the program *(or something else if you changed the name)*

*(Type the first command when you want to compile and the second when you want to run the program)*

<br>

## 🐧 Unix

### What you need

* **[CMake](https://cmake.org/)**

* **A compiler :**

	* **[GCC](https://gcc.gnu.org/)** for **Linux**

	* **[Clang](https://clang.llvm.org/)** for **MacOS**

The easiest way is to open a terminal and type : `sudo apt update` and `sudo apt upgrade`, then type :

* For **Linux** : `sudo apt install gcc g++ make cmake gdb`

* For **MacOS** : `sudo apt install clang clang++ make cmake lldb`

### How to compile it?

* Open a terminal in the project root and type : `bash unix_run.sh` to create and compile the project

* Then type : `./build/App` to run the program *(or something else if you changed the name)*

*(Type the first command when you want to compile and the second when you want to run the program)*

<br>

## 💎 Using VS Code *(recommended)*

### What you need

* The **"What you need"** part of your OS *(above)*

* The **[C/C++ Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools-extension-pack)**

### How to compile it?

* `Ctrl` + `Shift` + `P` and type *"scan for kits"*, then choose you compiler *(I recommend the Visual Studio compiler for Windows)*

* Choose *"debug"* or *"release"* at the bottom

* Go to *"Preferences"*, then *"Settings"* and type *"cmake debug"*, then clic on *"Edit in settings.json"* that will open the **settings.json** file

* Add this at this end *(don't forget the comma on the previous element)* :
	```json
	"cmake.debugConfig": {
		"cwd": "${workspaceFolder}"
	}
	```

* If there is a **build** folder, delete it and reload VS Code

* Wait until the **CMakeLists.txt** runs or choose again *"debug"* or *"release"* at the bottom

*(Choose "debug" or "release" again each time you add or remove a file and clic on the play button at the bottom to compile and run the program)*

<br>

# 🙏 Credits

* **[Angel Uriot](https://github.com/angeluriot) :** Creator of the skeleton project.
