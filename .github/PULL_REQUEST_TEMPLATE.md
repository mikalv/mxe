Please read http://mxe.cc/#creating-packages

In particular, make sure that your build rules:

  * install .pc file,
  * install bin/test-pkg.exe compiled with flags by pkg-config,
  * install .dll to bin/ and .a, .dll.a to lib/,
  * use $(TARGET)-cmake instead of cmake,
  * build in `$(BUILD_DIR)` instead of `$(SOURCE_DIR)`,
  * do not run target executables with Wine,
  * do not download anything while building,
  * do not install documentation,
  * do not install .exe files except test and build systems,

and .patch files are generated by tools/patch-tool-mxe.

If you add a package, you can use tool tools/skeleton.py.

Thanks!
