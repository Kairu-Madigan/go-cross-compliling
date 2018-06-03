# go-cross-compliling
Go Cross-Compile Script.

GoLang cross-compile snippet for Go 1.6+ based loosely on Dave Chaney's cross-compile script:
http://dave.cheney.net/2012/09/08/an-introduction-to-cross-compilation-with-go

To use:

  $ cd ~/path-to/my-awesome-project
  $ go-build-all

Features:

  * Cross-compiles to multiple machine types and architectures.
  * Uses the current directory name as the output name...
    * ...unless you supply an source file: $ go-build-all main.go
  * Windows binaries are named .exe.
  * ARM v5, v6, v7 and v8 (arm64) support

ARM Support:

You must read https://github.com/golang/go/wiki/GoArm for the specifics of running
Linux/BSD-style kernels and what kernel modules are needed for the target platform.
While not needed for cross-compilation of this script, you're users will need to ensure
the correct modules are included.

Requirements:

  * GoLang 1.6+ (for mips and ppc), 1.5 for non-mips/ppc.
  * CD to directory of the binary you are compiling. $PWD is used here.

For 1.4 and earlier, see http://dave.cheney.net/2012/09/08/an-introduction-to-cross-compilation-with-go

