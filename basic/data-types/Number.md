## Floating point Numbers

Most programming languages have several types of numeric data, but JavaScript gets away with just one.

examples: (Number)

    typeof 17; // Number
    typeof 17.17;  // Number
    typeof 17.117171717171; // Number

**Note:** In fact, all numbers in JavaScript are double-precision floating-point numbers, that is, the 64-bit encoding of numbers specified by the IEEE 754 standard—commonly known as “doubles". and also keep in mind that doubles can represent integers perfectly with up to 53 bits of precision. All of the integers from –9,007,199,254,740,992 (–253) to 9,007,199,254,740,992 (253) are valid doubles.


### Bitwise operators with Numbers

The bitwise arithmetic operators, however, are special. Rather than operating on their arguments directly as floating-point numbers, they implicitly convert them to 32-bit integers.

let's perform an xor operation two swap two numbers

    (3 ^ 2);  // integers

    // in binary (treated as 32 bits integers)
    (00000000000000000000000000000011) ^ (00000000000000000000000000000010); 
    
    1;  // result

