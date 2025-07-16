
# GNU Make & Custom Makefile for C/C++ Projects

This project contains a customizable and reusable **Makefile** designed to simplify the process of compiling and linking **C/C++** projects using `make`.

## 🧩 Features

- ✅ Supports both C and C++ source files
- 🎯 Defines multiple build targets (e.g., `all`, `clean`, `run`)
- 📦 Handles object file generation and cleanup
- ⚙️ Customizable compiler flags and arguments
- 🛠️ Includes `.PHONY` targets for proper dependency management

## 📂 Project Structure

```
Makefile/
├── Makefile          # Main Makefile for building C/C++ projects
├── main.c            # Example C source file
├── main.cpp          # Example C++ source file (optional)
```

## 🛠️ Usage

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

## 📘 Learning Resource

This Makefile was crafted for learning and teaching how to automate builds in C/C++ development using GNU Make.

📂 GitHub Repository: [ahmedmdtuhin/Makefile](https://github.com/ahmedmdtuhin/Makefile)

---

> 🚀 Use this Makefile to bootstrap C/C++ projects and understand the build process with Make.
