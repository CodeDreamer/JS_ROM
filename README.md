# JS_ROM
Disassembly of the Sinclair QL's operating system, version "JS".

The Sinclair QL came with an operating system in ROM called QDOS. Version "JS" is the last version that was available in the UK.

This is a commented disassembly of the ROM that has been available online and was created by Wolfgang Goeller. Additional comments by Richard Zidlicky.

## History
1. Disassembly and comments by Wolfgang Goeller (downloaded from the *Maya* FTP archive in the early days of the Internet).
2. Additional comments by Richard Zidlicky (also available on Dilwyn's web site).

## Building with the GST assembler
From a comment in system_asm, it's possible to assemble the ROM code with the GST Macro Assembler. It needs a 256 KB memory expansion and using the -NOLIST option to avoid running out of space.