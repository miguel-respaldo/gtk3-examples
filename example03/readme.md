You can compile the program with GCC using:

```bash
gcc `pkg-config --cflags gtk+-3.0` -o example-3 example-3.c `pkg-config --libs gtk+-3.0`
```

You need to keep builder.ui in the same directory where the binary is.
      
