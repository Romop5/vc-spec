This document describes textdb.dat file (DAT/textdbg.dat)

File format
===========
Textdb.dat contains a dictionary of key and their values. Multiple values per key are allowed.

Header
------
* strings are terminated with \0 (zero-terminated)

Total size: 16

| Offset | Name      | Type     |
|--------|-----------|----------|
| 0      | Signature | CHAR[4]  |

1. Unkwown DWORD (4 bytes), probably signature. Contains 0x1

After header, there are 

Pair
-------

This block contains a key and its set of values. The block always terminated with 0xFFFFFFFF 0xFFFFFFFF 

| Offset | Name      | Type  |
|--------|-----------|-------|
| 0      | Length of key name| uint\_32|
| 1      | Key name | c-string|
| 2      | Number of values | uint\_32|
| 3      | Length of first value | uint\_32|
| 4      | Name of the first value | c-string|
| -     | - | - |
| end   | Terminated sequence of 0xFF | uint\_32\*2| 


### Example
TODO


