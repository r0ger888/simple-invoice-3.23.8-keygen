To keygen this app :
- get the length and buffer for the mail string
- concatenate the mail string with the specific string - 23m0odr32 - and initiate them with the variable that saves the MD5 hashing (you either need a useful assembly file for MD5 or just cryptohash.lib)
- calculate the length of the MD5 hashing and create a new variable which saves its length - hLen (or wutever u call it..) dd ?
- start initiating the MD5 hashing on both the MD5 variable and the length of the MD5 hash too
- with Hex2ch (or HexToChar) , convert the hexadecimal chars loaded from MD5 hashing to proper unicoded chars with maximum of 16 hexadecimal chars.
- the serial has four parts with 4 chars each, this time they're lowercase (on Vocal remover pro the md5 chars were UPPERCASE) . So as you can see in the source code,i've initiated custom variables for the each of the serial parts to save them. So as for the first part, you need to compute the MD5 hash on the first position . and then concatenate the first part saved with a dash,then save it on the serial variable.
- for the second part, the md5 hash compution should be on the 5th position.
- for the third part, the md5 hash compution should be on the 10th position.
- and for the last part, the md5 hash compution should be on the 15th position.
- then make a clean subroutine to clear all the memory used for md5-computing and serial-generation with RtlZeroMemory so it won't overwrite the serial generation ever again.

and that's how i wrote an MD5 keygen for it in assembly.
