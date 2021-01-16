# Flashbang Bytecode
Flashbang Bytecode consists of a 4 byte instruction, split into a few parts, formatted like so XXYYZZAA:
XX: Instruction Number, currently only 01 (debug print), 02 (set address) and 03 (set address value) are valid
YY: Either the beginning of an address pointer (FY is reserved for this purpose) or an argument.
ZZ: Either the end of an address pointer or another argument/continuation of argument 1.
AA: Either 00 (in the case of a pointer) or another argument/continuation of argument 2.
## `01` debug print
To use a debug print, your byte code would be the following:
`01486921`
Which would print `Hi!`
## `02` set address
Use this to set an address for use later.
E.x., `02F12345` would set the current address to `F12345`.
NOTE: The F at the beginning is required. It's an F in the chat for Adobe Flash ;)
## `03` set address value
Sets the value of the current address.
E.x., `03486921` sets the current address (see above) to Hi!
Note: Putting consecutive addresses (incrementing by 1) will make some functions print all of them out. 
E.x., `02F12345030348656C02F12346036C6F21` will make `01F12345` print Hello!
## Playing Flashbang Bytecode
Currently **there is no official player for Flashbang Bytecode files**
