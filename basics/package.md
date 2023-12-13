Packages and modules:
Use codes and other functions

Any service can be a module.
Packages are a set of codes that serve a specific purpose and create modules.

In fact, each module is created from a number of packages, which can be divided into three categories:
Packages that we write ourselves (directory)
Third party packages
Standard library packages

Convert project to module:
in terminal, go mod init + projects name

creating our directories :
for example tools folder, it contains these files greeting.go , count.go , fizzbbuzz.go , is_divisible.go
all of these files have a same header, package tools

use it ... tools.count

importing third party packages ----> go get + address , go mod tidy
