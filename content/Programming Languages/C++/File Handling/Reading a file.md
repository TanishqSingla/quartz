---
tags:
  - Cpp
---

To read a file `ifstream` object is used, this object is present under `std` namespace inside `fstream` library

E.g
```c
#include <string>
#include <fstream>

int main() {
	ifstream in("file.txt"); // open for reading
	string s;

	while(getline(in, s)) {
		std::cout << s << "\n";
	}
}
```


### Footnotes
The [[getline(string)|getline]] function discards the newline character at the end, hence `\n` is added manually while printing