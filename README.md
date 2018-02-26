# antlr-scripts
A collection of *nix scripts for invoking and working with ANTLR parser generator.

## Installation

These scripts expect to be placed in a directory that *itself* contains
a directory named `active` (or, better yet, a symlink named `active`
linking to a versioned directory, like `4.7.1`). The `active` directory
should contain all JARs needed to run ANTLR (perhaps just one, like
`antlr4-4.7.1-complete.jar`).

## Usage

### antlr
Run the ANTLR parser generator.

Usage:
```
antlr <options-passed-to-antlr...>
```

### grun
Run the test rig (test a compiled grammar).

Usage:
```
grun <options-passed-to-test-rig...>
```

### grund
Run the test rig directly on an uncompiled grammar (generate a parser,
compile it, and run the test rig).

Usage:
```
grund <grammar-file> <options-passed-to-test-rig...>
```

Example:
```
grund Java.g4 compilationUnit -gui SomeClass.java
```

### antlr-classpath
Source this script in the current shell to add ANTLR JARs to your
`CLASSPATH` variable.

Usage:
```
. antlr-classpath
```
