---
tags:
  - Cpp
---

Get line from stream to string.
## Explanation
This function extracts characters into a [[string]] from input stream until the delimitation character or [[delimiter]] `delim` is found (by default this is newline character `\n`)

## Signature
`istream& getline(istream& is, string& str, char delim)`
`istream& getline (istream& is, string& str);`
## Example Usage
```cpp
#include <iostream>
#include <string>

int main() {
	std::string name;
	std::getline(std::cin, name);
	std::cout << "Hello, " << name << "!\n";
}
```
