# OS Module in Python  

## 1. **Overview**  
The `os` module provides a way to interact with the operating system for file and directory management, process handling, and more.

---

## 2. **Key Methods and Usage**  

### 📂 **Directory Management**  
| **Method**                | **Description**                      | **Code Example**                |
|---------------------------|--------------------------------------|----------------------------------|
| `os.getcwd()`             | Gets the current working directory   | `print(os.getcwd())`            |
| `os.chdir(path)`          | Changes the working directory        | `os.chdir("new_path")`          |
| `os.listdir(path)`        | Lists files and directories in path  | `print(os.listdir("."))`        |
| `os.mkdir(path)`          | Creates a single directory           | `os.mkdir("folder_name")`       |
| `os.makedirs(path)`       | Creates nested directories           | `os.makedirs("dir1/dir2")`      |
| `os.rmdir(path)`          | Removes an empty directory           | `os.rmdir("folder_name")`       |
| `os.removedirs(path)`     | Removes nested empty directories     | `os.removedirs("dir1/dir2")`    |

---

### 📜 **File Management**  
| **Method**                | **Description**                      | **Code Example**                |
|---------------------------|--------------------------------------|----------------------------------|
| `os.rename(src, dst)`     | Renames a file or directory          | `os.rename("old.txt", "new.txt")`|
| `os.remove(path)`         | Deletes a file                      | `os.remove("file.txt")`         |
| `os.path.exists(path)`    | Checks if a file/directory exists    | `print(os.path.exists("file"))` |
| `os.path.isfile(path)`    | Checks if the path is a file         | `os.path.isfile("file.txt")`    |
| `os.path.isdir(path)`     | Checks if the path is a directory    | `os.path.isdir("folder")`       |

---

### 🔎 **Path Manipulation**  
| **Method**                   | **Description**                       | **Code Example**                   |
|------------------------------|---------------------------------------|-------------------------------------|
| `os.path.join(path, name)`   | Joins paths in a platform-safe way    | `os.path.join("dir", "file.txt")`  |
| `os.path.basename(path)`     | Gets the file name from a path        | `os.path.basename("/dir/file.txt")`|
| `os.path.dirname(path)`      | Gets the directory name from a path   | `os.path.dirname("/dir/file.txt")` |
| `os.path.split(path)`        | Splits path into dir and file         | `os.path.split("/dir/file.txt")`   |
| `os.path.abspath(path)`      | Converts relative path to absolute    | `os.path.abspath("file.txt")`      |

---

### 🖥️ **Environment Variables**  
| **Method**                | **Description**                          | **Code Example**                  |
|---------------------------|------------------------------------------|------------------------------------|
| `os.getenv(var)`          | Gets the value of an environment variable| `print(os.getenv("HOME"))`        |
| `os.putenv(var, value)`   | Sets an environment variable (deprecated)| `os.putenv("MY_VAR", "value")`    |
| `os.environ`              | Access environment variables as a dict   | `print(os.environ["HOME"])`       |

---

### 🛠️ **System Operations**  
| **Method**                | **Description**                          | **Code Example**                  |
|---------------------------|------------------------------------------|------------------------------------|
| `os.system(command)`      | Executes a system command                | `os.system("ls")`                 |
| `os.name`                 | Returns the name of the operating system | `print(os.name)`                  |
| `os.getlogin()`           | Returns the logged-in user               | `print(os.getlogin())`            |

---

### 📑 **Practical Examples**  

#### 1. **Check and Create a Directory**  
```python
import os

if not os.path.exists("new_folder"):
    os.mkdir("new_folder")
    print("Directory created.")
else:
    print("Directory already exists.")
```

#### 2. **List Files with Full Path**  
```python
import os

for file in os.listdir("."):
    print(os.path.join(os.getcwd(), file))
```

#### 3. **Delete Files with a Specific Extension**  
```python
import os

for file in os.listdir("."):
    if file.endswith(".txt"):
        os.remove(file)
        print(f"{file} deleted.")
```

#### 4. **Combine Environment Variables with Paths**  
```python
import os

home_dir = os.getenv("HOME")
file_path = os.path.join(home_dir, "myfile.txt")
print(f"File path: {file_path}")
```
---

## 📚 Resources for OS Module   
1. **[W3Schools: Python OS Module](https://www.w3schools.com/python)**  
2. **[Python Documentation: OS Module](https://docs.python.org/3/library/os.html)**  
3. **[OS Module Explained](https://youtu.be/tJxcKyFMTGo?si=4DtRhF-ICCuLGKVm)**
