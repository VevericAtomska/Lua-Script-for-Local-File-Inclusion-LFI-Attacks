--------------------------------------------------------------------------------------------------------------
Lua Script for Local File Inclusion (LFI) Attacks
This Lua script is designed for conducting Local File Inclusion (LFI) attacks against vulnerable web applications. It supports various functionalities such as choosing HTTP methods, using custom headers, and specifying the target URL and LFI paths.
--------------------------------------------------------------------------------------------------------------
Requirements
Lua interpreter (tested with Lua 5.3)
LuaSocket library (socket.http)
LuaSocket URL library (socket.url)
LuaSocket ltn12 library (ltn12)
Lua argparse library for command-line parsing (argparse)
Installation
Install Lua Interpreter:
--------------------------------------------------------------------------------------------------------------
Download and install Lua interpreter from Lua.org.
Install LuaSocket and argparse Libraries:
--------------------------------------------------------------------------------------------------------------
Use LuaRocks to install required libraries:
luarocks install luasocket
luarocks install argparse
--------------------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------------------
Usage
Command-line Options
The script supports the following command-line options:

--url-target <URL>: Specify the target URL with LFI vulnerability.
--file-path <PATH>: Specify the file path for LFI exploitation.
--http-method <METHOD>: (Optional) Choose HTTP method (GET or POST). Default is GET.
--use-headers: (Optional) Use custom headers in the HTTP request.
--headers-file <FILE>: (Required if --use-headers is set) Specify a file containing custom headers.
Example Usage
--------------------------------------------------------------------------------------------------------------
Basic Usage:
--------------------------------------------------------------------------------------------------------------
lua lfi_attack.lua --url-target "http://example.com/vulnerable_script.php" --file-path "../../../../etc/passwd"
--------------------------------------------------------------------------------------------------------------
Advanced Usage with Custom Headers:
--------------------------------------------------------------------------------------------------------------
lua lfi_attack.lua --url-target "http://example.com/vulnerable_script.php" --file-path "../../../../etc/passwd" --http-method "POST" --use-headers --headers-file "custom_headers.txt"
--------------------------------------------------------------------------------------------------------------
