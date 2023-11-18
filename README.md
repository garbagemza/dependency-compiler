[![cdcompiler](https://github.com/garbagemza/dependency-compiler/actions/workflows/go.yml/badge.svg)](https://github.com/garbagemza/dependency-compiler/actions/workflows/go.yml)

# cdcompiler
This tool attempts to compile C/C++ dependencies. Use it in combination of dependency-checker and dependency-linker.

## dependencies

This tool depends on `gcc` to perform compilation of source code.

## build

`go build -v ./...`

`cdcompiler` is created for you.

## run

This tool is intended for use with command line on global scope

Put this binary on your bin/ directory and use.

## usage

1. Use dependency-checker `cdcheck` first, as it will download your required dependency. The file output and directory structure is used by `cdcompiler`.
2. Run `cdcompiler`. That's it.

- After the compilation is done. You will find new files created for you.
Your new objects will be located here:
`build` > `intermediates` > `<library name>` > `intermediates`

3. Use this tool in combination of `cdlinker` to create libraries from the output of `cdcompiler`.
