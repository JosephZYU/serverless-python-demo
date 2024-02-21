Yes, you are correct in your understanding of the Makefile syntax:

1. **Target Name**: In the Makefile, the word before the colon `:` is the target name. In your example, `lint` is the target name. The word after the colon, such as `format` in your example, is a dependency. This means that before executing the `lint` target, Make will first ensure that the `format` target is executed.

2. **Indentations**: The indentation (spaces or tabs) in a Makefile is significant. It is used to define a command that is part of a particular target. Each command associated with a target is indented to visually separate it from the target definition and to indicate that it is a command to be executed when that target is invoked.

3. **Comments**: Yes, anything following a hash symbol `#` in a Makefile is considered a comment and is ignored by Make during execution. Comments are used to add explanations or notes in the Makefile, which can be helpful for anyone reading or maintaining the file.

So, in your example, `lint: format` means that the `lint` target depends on the `format` target. The commands under `lint` are indented and executed when the `lint` target is called. Comments with `#` provide explanations but are not executed.
