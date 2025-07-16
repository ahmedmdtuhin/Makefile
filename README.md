
# GNU Make & Custom Makefile for C/C++ Projects

This project contains a customizable and reusable **Makefile** designed to simplify the process of compiling and linking **C/C++** projects using `make`.

## 🧩 Features

- ✅ Supports both C and C++ source files
- 🎯 Defines multiple build targets (e.g., `all`, `clean`, `run`)
- 📦 Handles object file generation and cleanup
- ⚙️ Customizable compiler flags and arguments
- 🛠️ Includes `.PHONY` targets for proper dependency management

## 📂 Project Structure
The repository is structured into folders, each representing a level of complexity. From a minimal Makefile that compiles a single C file. Great for beginners to a full-featured Makefile with pattern rules, variables, .PHONY targets, and compiler flag customization.


## 🛠️ Usage
```bash


cd desired_folder/
make            # Build the project
make run        # Run the binary (if defined)
make clean      # Remove generated files
```
### 🔨 Build the Project

```bash
make
```

### ▶️ Run the Executable

```bash
make run
```

### 🧹 Clean Build Files

```bash
make clean
```

## 🔧 Customize

You can adjust the following variables directly in the Makefile:

```makefile
CC = gcc           # Compiler (gcc/g++)
CFLAGS = -Wall     # Compiler flags
SRC = main.c       # Source file(s)
TARGET = main      # Output executable
```

> 🚀 Use this Makefile to bootstrap C/C++ projects and understand the build process with Make.
## 📘 Learning Resource

[Make and Makefile for C/C++ Projects (Udemy)](https://www.udemy.com/course/make-and-makefile-for-cc-projects-2022-edition/?couponCode=KEEPLEARNING)




