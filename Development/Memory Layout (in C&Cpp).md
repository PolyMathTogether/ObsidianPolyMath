A source code writen in C/C++ is stored in **storage**. When we compile it, the system creates an **executable file**, which is also stored in **storage**. When we run the program, it is loaded into **memory** and then executed. *So, what kind of structure does a program have once it is loaded into memory?*

The memory layout of a C/C++ program is structured into text segment, initialized data segment, uninitialized data segment, heap and stack.

![[memory_layout.jpg]]
# Text Segment
---
At the lowest memory addresses, the **program’s code** is stored.

# Initialized Data Segment (DS)
---
This is where global and static variables are stored, provided that they are **initialized with a non-zero value** by the programmer.

# Unintialized Data Segment (BSS)
---
This is where global and static variables that are either **uninitialized** or **initialized to zero** are stored.

# Heap and Stack
---
The **stack** is a region of memory that is **automatically allocated** and follows a LIFO (Last In, First Out) structure. On the other hand, **heap** is **manually allocated** by programmer.
