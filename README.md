# JS_ROM
Disassembly of the Sinclair QL's operating system, version "JS".

The Sinclair QL came with an operating system in ROM called QDOS. Version "JS" is the last version that was available in the UK.

QDOS was written at Sinclair Research, mostly by Tony Tebby (operating system) and Jan Jones (SuperBASIC interpreter).

This is a commented disassembly of the ROM that has been available online and was created by Wolfgang Goeller. Additional comments by Richard Zidlicky and Daniele Terdina.

## History
1. Disassembly and comments by Wolfgang Goeller (downloaded from the *Maya* FTP archive in the early days of the Internet).
2. Additional comments by Richard Zidlicky (also available on Dilwyn's web site).
3. Additional comments by Daniele Terdina (also available on Q-emuLator's web site).
4. Minor changes to cross-assemble with Asm68K_QL and generate accurate binary.

## Building with the GST assembler
According to a comment in system_asm, it's possible to assemble the ROM code with the GST Macro Assembler. It needs a 256 KB memory expansion and using the -NOLIST option to avoid running out of space.  
Use the [original sources](https://github.com/CodeDreamer/JS_ROM/releases/tag/original).

## Building with Asm68K
Using the Asm68K cross-assembler, assemble with:
```
Asm68K --noopt system_asm
```
The --noopt is not necessary, but makes the output closer to the original.

## Releases
Available GitHub releases (code snapshots):
- `original` is the original disassembly published in the 90s, plus some additional comments. It contains some modifications.
- `accurate` produces code identical to the JS ROM when assembled with Asm68K_QL, with one exception: some jumps in the original ROM use "absolute long" addressing (probably by mistake), while the assembler generates "absolute short" addressing. There is no functional difference, and the disassembly already included NOPs to keep the following code at the original address.

## main branch
The main branch contains the original ROM JS code plus a couple of additional changes:
- Workaround for ROM detection issue.