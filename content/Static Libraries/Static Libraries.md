Static libraries also called archives consists of nothing more than a collective of raw object files strung together along with a table of contents for fast symbol access.

Traditionally libraries were archives (`.a` files). There were created using 
```sh
ar cr libfoo.a foo.o bar.o spam.o
```

This aforementioned command will output a archive named `libfoo.a`. 