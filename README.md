# Introduction to programming in Yul Assembly

## References
- [Video tutorial](https://www.youtube.com/playlist?list=PL5hld-skrdFrxGUmmEbG1LBvYVyTE9M62)

## Bytes Cheatsheet
``` 
0xff means 1 byte (8 bits)
0xff == 1111 1111
``` 

## Memory Layout
Solidity reserves four 32-byte slots, with specific byte ranges (inclusive of endpoints) being used as follows:
- 0x00 - 0x3f (64 bytes) [0x00 - 0x20][0x20 - 0x40]: scratch space for hashing methods
- 0x40 - 0x5f (32 bytes) [0x40 - 0x60]: currently allocated memory size (aka. free memory pointer)
- 0x60 - 0x7f (32 bytes) [0x60 - 0x80]: zero slot
- The action begins in slot 0x80

For memory storage of abi.encode
- First the length of the array is stored
- And then the elements are stored
  
# Other Resources
- [Solidity docs on Yul](https://docs.soliditylang.org/en/latest/yul.html)


