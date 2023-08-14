a small utility library that simplifies the usage of C++ Filesystem. It provides a convenient way to work with the C++ Filesystem library without directly including &lt;filesystem&gt; or &lt;experimental/filesystem&gt; headers in your code. And handles cases where linking to fs (i.e. -lstdc++fs) is needed

Usage:
```
// CMakeLists.txt
add_subdirectory(dep/fs)
target_link_libraries(target_name fs_bindings)
```
```
// main.cpp
#include <iostream>
#include "fs.hpp"

int main()
{
     std::cout << fs::current_path() << '\n'
}
```
