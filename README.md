#as2dts

A command-line tool that converts ActionScript 3 classes and interfaces to TypeScript definitions. This tool can be used along with FlexJS to provide TypeScript definitions to your ActionScript libraries that have been cross-compiled to JavaScript.

#Steps:

* Install npm
* Run `npm install -g as2dts` to install globally or `npm install --save as2dts` to install locally as a dependency in your project
* Run `as2dts --defs-only --out-name foo /path/to/as3/src /path/to/foo/`
* Copy the resulting file `/path/to/foo/foo.d.ts` into your TypeScript project

---------------------------------
#Old readme below


##Installation

Install this module with npm: 

```
npm install -g as2dts
```

##Usage

```
as2dts [--defs-only] <sourceDir> <outputDir>
```

##Note

This tool will not magically transform your as3 codebase into perfect typescript, the goal is to transform the sources into *syntactically* correct typescript, and even this goal is not perfectly respected. It also won't try to provide javascript implementation for flash libraries.

However unlike most attempts that I have seen this tool is based on a true actionscript parser, and so should be able to handle most of as3 constructs and greatly ease the pain of porting a large code base written in as3 to typescript.

##Command-line help

Compile:
```
npm run-script compile
```

Install on command-line:
```
npm install -g
```

Install debugger:
```
npm install -g node-inspector
```

Start debugging service:
```
node-inspector -p 8081 &
```

Debug:
```
node-debug bin/as2dts [--defs-only] [--out-name <name>] <sourceDir> <outputDir>
```
