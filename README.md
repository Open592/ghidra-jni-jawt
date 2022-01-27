# ghidra-jni-jawt
jni.h and jawt.h compiled for Ghidra

## Credits
Credit goes to https://github.com/extremecoders-re/ghidra-jni for initial `jni.h` and parse configuration profile options.

## Purpose
This repository contains an all-in-one header file to provide data types for both `jni.h` and `jawt.h` within Ghidra.

## Howto

Go to `File -> Parse C Source`

Create a new Parse Configuration Profile with the following Parse Options

```
-D_X86_
-D__STDC__
-D_GNU_SOURCE
-D__WORDSIZE=64
-Dva_list=void *
-D__DO_NOT_DEFINE_COMPILE
-D_Complex
-D_WCHAR_T
-D__NO_STRING_INLINES
-D__signed__
-D__extension__=""
-D_Bool="bool"
-D__GLIBC_HAVE_LONG_LONG=1
-D__need_sigset_t
-Daligned_u64=uint64_t
-Daligned_u64=uint64_t
```

Under source files to parse, add `jni-jawt.h` to the list. Remove any other existing file (if any).
