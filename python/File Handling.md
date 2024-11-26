# File Handling in Python

## 1. **File Modes Quick Reference**
| **Mode** | **Action**                       | **File Pointer**  | **File Existence** |
|----------|----------------------------------|-------------------|---------------------|
| `"r"`    | Read only                        | Beginning         | Must exist          |
| `"w"`    | Write only (overwrite)           | Beginning         | Creates if absent   |
| `"a"`    | Append only                      | End               | Creates if absent   |
| `"r+"`   | Read and write                   | Beginning         | Must exist          |
| `"w+"`   | Write and read (overwrite)       | Beginning         | Creates if absent   |
| `"a+"`   | Append and read                  | End               | Creates if absent   |
| `"x"`    | Create and write (fails if exists)| Beginning         | Must not exist      |

---

## 2. **Key File Operations**
- **Check File Existence**:
  ```python
  import os
  print(os.path.exists("file.txt"))  # Returns True or False
  ```

- **Create an Empty File**:
  ```python
  with open("newfile.txt", "x") as file:
      pass
  ```

---

## 3. **Reading Techniques**
| **Method**        | **Description**                   | **Code Example**            |
|--------------------|-----------------------------------|-----------------------------|
| `read()`           | Reads entire file content        | `content = file.read()`     |
| `readline()`       | Reads the next line              | `line = file.readline()`    |
| `readlines()`      | Reads all lines as a list        | `lines = file.readlines()`  |

### Example: Reading Line by Line
```python
with open("example.txt", "r") as file:
    for line in file:
        print(line.strip())  # Removes newline characters
```

---

## 4. **Writing Techniques**
- **Write Multiple Lines**:
  ```python
  with open("example.txt", "w") as file:
      file.writelines(["Line 1\n", "Line 2\n", "Line 3\n"])
  ```

- **Append Content**:
  ```python
  with open("example.txt", "a") as file:
      file.write("New line appended.\n")
  ```

---

## 5. **File Handling Utilities**
- **Renaming a File**:
  ```python
  os.rename("oldname.txt", "newname.txt")
  ```

- **Delete a File Safely**:
  ```python
  if os.path.exists("example.txt"):
      os.remove("example.txt")
  ```

- **Delete Empty Folder**:
  ```python
  os.rmdir("empty_folder")
  ```

---

## 6. **Context Manager**
- **Auto-close files**:
  ```python
  with open("example.txt", "r") as file:
      content = file.read()
      print(content)
  # No need for file.close()
  ```

---

## 7. **Common Exceptions**
| **Error**         | **Cause**                  | **Fix**                              |
|--------------------|---------------------------|--------------------------------------|
| `FileNotFoundError`| File doesn't exist        | Check with `os.path.exists()`       |
| `PermissionError`  | Insufficient permissions  | Check file permissions              |
| `IsADirectoryError`| Path is a directory       | Ensure correct file path            |

---

### Sample Code to Practice:
```python
import os

# Write to file
with open("sample.txt", "w") as file:
    file.write("This is a test file.\n")

# Read file content
with open("sample.txt", "r") as file:
    print(file.read())

# Append to file
with open("sample.txt", "a") as file:
    file.write("Appended text.\n")

# Check file existence
if os.path.exists("sample.txt"):
    print("File exists!")
```

---
## 📚 Resources for File Handling  

### 🎥 **Video Tutorial**  
1. **[File Handling in Python](https://youtu.be/Uh2ebFW8OYM?si=3zHWQLyyfZ9t5MFp)**  
2. **[W3Schools: File Handling](https://www.w3schools.com/python/python_file_handling.asp)**   
3. **[Python Documentation: File Objects](https://docs.python.org/3/)**  
