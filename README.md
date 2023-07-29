a small utility library that simplifies the usage of C++ Filesystem. It provides a convenient way to work with the C++ Filesystem library without directly including &lt;filesystem&gt; or &lt;experimental/filesystem&gt; headers in your code.

Usage:

Add cpp_find_fs as a subdirectory in your CMake project.

Link your project against the fs_bindings interface library provided by cpp_find_fs.

In your C++ code, include the fs.hpp header instead of directly including &lt;filesystem&gt; or &lt;experimental/filesystem&gt;. The fs.hpp header includes the necessary Filesystem functionality and ensures compatibility with both the standardized &lt;filesystem&gt; header (C++17 and later) and the experimental &lt;experimental/filesystem&gt; header.
