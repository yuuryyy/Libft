# 📚 Libft

Your very first custom C library. This project is the first milestone in the 1337 (42 Network) curriculum, challenging you to recreate standard C library functions from scratch to deeply understand memory management, pointers, and data structures.

---

## 📖 About The Project

In C programming, the standard library is a powerful tool, but at 42, we build our own. `Libft` is a static library (`libft.a`) containing custom implementations of essential `<string.h>`, `<stdlib.h>`, and `<ctype.h>` functions. This library will serve as the core foundation for almost every C project you write moving forward in the curriculum.

### 🎯 Objectives
* Understand the underlying mechanics of standard C functions.
* Master manual memory allocation and deallocation (`malloc`, `free`).
* Implement and manipulate basic data structures (Linked Lists).
* Strictly adhere to the 42 Norm coding standard.

---

## ✨ Features & Functionality

The library is categorized into three main parts:

### 1. 🧰 Part 1: Libc Functions
Direct rewrites of standard C library functions.

* **Character Classification:** `ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint`
* **Character Manipulation:** `ft_toupper`, `ft_tolower`
* **String Examination:** `ft_strlen`, `ft_strchr`, `ft_strrchr`, `ft_strncmp`, `ft_strnstr`
* **String Manipulation:** `ft_strlcpy`, `ft_strlcat`, `ft_strdup`
* **Memory Manipulation:** `ft_memset`, `ft_bzero`, `ft_memcpy`, `ft_memmove`, `ft_memchr`, `ft_memcmp`
* **Dynamic Memory & Conversion:** `ft_calloc`, `ft_atoi`

### 2. 🛠️ Part 2: Additional Functions
Utility functions useful for string manipulation and output that are not in standard Libc.

* **String Creation/Editing:** `ft_substr`, `ft_strjoin`, `ft_strtrim`, `ft_split`, `ft_itoa`
* **Function Application:** `ft_strmapi`, `ft_striteri`
* **File Descriptor Output:** `ft_putchar_fd`, `ft_putstr_fd`, `ft_putendl_fd`, `ft_putnbr_fd`

### 3. 🔗 Bonus Part: Linked Lists
Functions to create and manage the `t_list` structure.

* `ft_lstnew`: Creates a new list node.
* `ft_lstadd_front`: Adds a node to the beginning.
* `ft_lstsize`: Counts nodes in a list.
* `ft_lstlast`: Returns the last node.
* `ft_lstadd_back`: Adds a node to the end.
* `ft_lstdelone`: Deletes a single node's content.
* `ft_lstclear`: Deletes and frees a list.
* `ft_lstiter`: Applies a function to each node.
* `ft_lstmap`: Applies a function and returns a new list.

---

## 🛠️ Getting Started

### Prerequisites
* A standard C compiler (`cc`, `gcc`, or `clang`)
* `make` utility

### Installation & Compilation

1. Clone the repository:
   ```bash
   git clone [https://github.com/yuuryyy/Libft.git](https://github.com/yuuryyy/Libft.git)
   cd Libft
   ```

2. Compile the mandatory core library:
   ```bash
   make
   ```

3. Compile the library including the bonus linked-list functions:
   ```bash
   make bonus
   ```

This will generate the required static library file: `libft.a`.

### Makefile Rules

* `make` / `make all`: Compiles mandatory functions.
* `make bonus`: Compiles mandatory + bonus functions.
* `make clean`: Removes the compiled `.o` object files.
* `make fclean`: Removes the object files and the `libft.a` binary.
* `make re`: Runs `fclean` followed by `all`.

---

## 💻 Usage

To use `Libft` in your own C projects, include the header file and link the compiled library.

**1. Include the header in your C file (`main.c`):**
```c
#include "libft.h"

int main(void)
{
    char *str = ft_strdup("Hello 1337!");
    
    ft_putendl_fd(str, 1);
    free(str);
    
    return (0);
}
```

**2. Compile your program with the library:**
```bash
cc main.c -L. -lft -o my_program
```
*(Ensure `libft.a` is in the same directory, or adjust the `-L` path accordingly)*

---
*Developed by Youssra Chagri at 1337 (UM6P).*
