## Floating point Numbers

Most programming languages have several types of numeric data, but JavaScript gets away with just one.

examples: (Number)

    typeof 17; // Number
    typeof 17.17;  // Number
    typeof 17.117171717171; // Number

**Note:** In fact, all numbers in JavaScript are double-precision floating-point numbers, that is, the 64-bit encoding of numbers specified by the IEEE 754 standard—commonly known as “doubles". and also keep in mind that doubles can represent integers perfectly with up to 53 bits of precision. Ranges from (2^-53) to (2^53).


### Bitwise operators with Numbers

The bitwise arithmetic operators, however, are special. Rather than operating on their arguments directly as floating-point numbers, they implicitly convert them to 32-bit integers.

let's perform an XOR operation two swap two numbers

    (3 ^ 2);  // integers

    // in binary (treated as 32 bits integers)
    (00000000000000000000000000000011) ^ (00000000000000000000000000000010); 
    1;  // result


### Accuracy and Performance Issues with Floating Point Number

- Adding two floating point number
  
      0.1 + 0.2 = 0.30000000000000004
      0.1 + (0.1 + 0.2) = 0.4
      // quite unpredictable behaviour

- To resove this (try to perform operations with whole numbers)
    
      1 + 2 = 3
      3/10 = 0.3


### Important Note

- JavaScript numbers are double-precision floating-point numbers.
- Integers in JavaScript are just a subset of doubles rather than a
separate datatype.
- Bitwise operators treat numbers as if they were 32-bit signed integers.
- Be aware of limitations of precisions in floating-point arithmetic.

