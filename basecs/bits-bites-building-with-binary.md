# Bits, Bytes, Building With Binary

Our modern counting system is known as base 10 or denary since there are 10 possible digits per place. We increment digits in one place until we can't any more then add a digit to the next place.

In the binary number system there are only 2 possible digits per place (0, 1) but we count in the same way by incrementing the digits in one place until we cant anymore then add a digit to the next place.

i.e. the number 2 in binary is 10, 3 is 11, 4 is 100, 5 is 101, 6 is 110, 7 is 111, 8 is 1000

Converting numbers from base 10 into binary we want to break the number down into powers of two. In base 10 we have places for units, tens, hundreds, thousands, and so on. In binary our places come from the powers of 2 so they are 2 to the power of 0, 2 to the power of 1, 2 to the power of 2, and so on… those power values equate to 1, 2, 4, 8. 16, 32, 64, 128, 256, etc. (think 2048 game numbers).

<br/>

**Powers of Two Chart:**

| Power of Two  | Denary Value |
| :------------ | -----------: |
| 2<sup>0<sup>  |            1 |
| 2<sup>1<sup>  |            2 |
| 2<sup>2<sup>  |            4 |
| 2<sup>3<sup>  |            8 |
| 2<sup>4<sup>  |           16 |
| 2<sup>5<sup>  |           32 |
| 2<sup>6<sup>  |           64 |
| 2<sup>7<sup>  |          128 |
| 2<sup>8<sup>  |          256 |
| 2<sup>9<sup>  |          512 |
| 2<sup>10<sup> |         1024 |
| 2<sup>11<sup> |         2048 |

<br />

### Converting a denary number to binary:

If we take a number to convert like 37, we would break it down by finding the highest power of two within it without going over, subtracting from the total, and repeating until we have 0 or 1 left over. Like so:

| Power of Two | Equals | Denary Value | Calculation |
| :----------- | :----: | -----------: | ----------: |
| 2<sup>5<sup> |   =    |           32 | 37 - 32 = 5 |
| 2<sup>2<sup> |   =    |            4 |   5 - 4 = 1 |
| 2<sup>0<sup> |   =    |            1 |   1 - 1 = 0 |

We can see that we have a value for each of the powers above so those places will get a value of 1 and any power of 2 that does not have a value will get a zero so 37 in binary would be: **100101**

<br />

Converting a bigger number of 168:

| Power of Two | Equals | Denary Value |    Calculation |
| :----------- | :----: | -----------: | -------------: |
| 2<sup>7<sup> |   =    |          128 | 168 - 128 = 40 |
| 2<sup>5<sup> |   =    |           32 |    40 - 32 = 8 |
| 2<sup>3<sup> |   =    |            0 |      8 - 8 = 0 |

Binary value: **1010100**

<br />

**Even numbers in base 10 will always end in 0 when converted into binary, odd numbers will always end in 1 when converted into binary.** Since 2 raised to the power of 0 is always equal to 1. Even numbers are divisible by two so we will have an extra remainder of 1 for odd numbers.

### Converting a binary number to denary:

Converting numbers from binary to base 10 we take the numbers in the given places for the power of 2 and multiply the power by 1 if there is a 1 in that place or a 0 otherwise and add them all up. So a number like 43 which is **101011** in binary we would convert back like so:

| Power of Two | Times | Binary Value | Equals | Denary Value |
| :----------- | :---: | -----------: | :----: | -----------: |
| 2<sup>5<sup> |  \*   |            1 |   =    |           32 |
| 2<sup>4<sup> |  \*   |            0 |   =    |            0 |
| 2<sup>3<sup> |  \*   |            1 |   =    |            8 |
| 2<sup>2<sup> |  \*   |            0 |   =    |            0 |
| 2<sup>1<sup> |  \*   |            1 |   =    |            2 |
| 2<sup>0<sup> |  \*   |            1 |   =    |            1 |

Denary Value: **43**

### Additional Tidbits

A single digit in binary is known as a binary digit or a bit. A bit can only ever be composed of a 0 or 1.

8 bits (or 8 digits) strung together is a byte. A single byte can represent 256 different combinations.

2 bytes or 16 bits can represent 65,536 different combinations.

Bits are important because different computers can process a different number of bits at a time. i.e. an 8-bit machine processes 8-bits at a time.

Most computers are 32 or 64 bit meaning that it processes binary strings that are 32 or 64 digits long (think Windows 32 or 64 bit).
