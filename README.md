# Unclosed File Resource in Python Function
This repository demonstrates a common error in Python: failing to close a file after opening it.  Unclosed files can lead to resource exhaustion and unexpected behavior in your applications.

The `bug.py` file contains the erroneous code, while `bugSolution.py` provides the corrected version using a `with` statement for proper file handling.

**Issue:**
The original code opens a file using `open()`, but lacks a `f.close()` call to explicitly close the file. If an exception occurs within the function before reaching the end, the file remains open, potentially leading to a resource leak.

**Solution:**
The solution employs a `with open(...) as f:` statement. This ensures the file is automatically closed when the block of code within the `with` statement is executed, regardless of exceptions.