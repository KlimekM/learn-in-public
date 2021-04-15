# Hexes and Other Magical Numbers

Original article: [Hexes and Other Magical Numbers](https://medium.com/basecs/hexs-and-other-magical-numbers-9785bc26b7ee)

## Notes

8 digits in binary is a byte. Bytes can be strung together to form kilobytes, megabytes, gigabytes, etc.

One byte can only represent a single character. For instance my name Michal would be 6 bytes, or 48 bits.

In order to convert letters into binary we need to encode the characters using some sort of encoding rule set.

ASCII encoding is a common rule set that allows us to translate certain characters into decimal numbers. ASCII has 128 possible characters that includes all the lowercase and uppercase letters as well as numbers, and special characters such as spaces, exclamation points, plus signs, ampersands, etc.

<br />

![ASCII Table](https://www.asciitable.com/index/asciifull.gif)

To convert a word to binary we want to look at an encoding table like the one above and convert a character to its decimal equivalent and then convert the decimal into binary.

Initially ASCII had only 128 possibilities and the first character in each byte was a 0 so only 7 bits were being used. 7 bits is 2<sup>7</sup> or 128, 8 bits is 2<sup>8</sup>, or 256. The unused 8 bit led to the ASCII scheme being extended. ASCII is a single encoding and there are several different encoding rule sets.

### Hexadecimals

In addition to base 10 and base 2 there is a base 16 number system that has 16 possible digits per place.

The 16 possible digits are:

0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F

Representing the number 205 in binary or base 2 we would need 8 digits, but only need 2 digits in base 16: **CD**

The general rule of thumb is that the higher the base the fewer place values you need in order to represent a number.

### Hexadecimals in Action

We often use hex codes when styling a web page with CSS. Computers however always specify colors using rgb (red, green, blue).

Hex codes get converted to rgb via hexadecimals.

i.e.
#EC152E gets broken down as EC → 236, 15 → 21, 2E → 46.

Hex codes can be broken down into 3 segments that represent the red, green, and blue value to make a given color.

The rgb color model only allows for values between 0 and 255 because one byte or 8 bits results in 256 possible combinations which is why those are the only accepted values in the rgb color model.

One other take away from all of this as someone who has worked with base 64 encoding in the past is that base 64 is just another abstraction similar to base 10, and base 16 in that there are 64 possible characters per place. This allows us to more efficiently encode/transmit large sets of data such as an image or a video.
