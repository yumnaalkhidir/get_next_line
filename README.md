# get_next_line

A function that reads a text file descriptor one line at a time, without re-reading the whole file on each call. Includes a bonus version that correctly handles multiple file descriptors simultaneously.

## Concepts covered
- Static variables for preserving state between function calls
- Manual buffered reading from a file descriptor
- Bonus: multiplexing reads across several file descriptors at once using a static array

## Build & run
No Makefile — compile directly with a buffer size, along with your own test `main.c`:
```sh
cc -D BUFFER_SIZE=42 get_next_line.c get_next_line_utils.c main.c -o gnl
# bonus (multi-fd) version:
cc -D BUFFER_SIZE=42 get_next_line_bonus.c get_next_line_utils_bonus.c main.c -o gnl_bonus
```

---
Part of the 42 School curriculum.
