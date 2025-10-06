#python
glob is a library which helps find all the pathnames matching a specified pattern.

Example Usage:
```python
import glob

# Find all .txt files in the current directory
txt_files = glob.glob("*.txt")
print(f"Text files: {txt_files}")
# You can also mention the directory like 'directory/*.txt'

# Find all files recursively in subdirectories
all_files_recursive = glob.glob("**/*", recursive=True)
print(f"All files recursively: {all_files_recursive}")
```

Reference:
[glob docs](https://docs.python.org/3/library/glob.html)