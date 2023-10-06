## Implicit Type Coercions

- Boolean Type
    
    - true: 1
    - false: 0

          2 + true;  // 3
          2 + false;  // 2

- String Type

String is treated as number, when we try to multiply them
  
  - Addition with Strings
    
        2 + 3;  // 5
        2 + "3";  // 23
        2 + "3" + 1;  // 231
        2 + 1 + "3";  // 33

  - Multiplication with Strings 

        "2" * 3;  // 6
        "2" * "3";  // 6
        "2" * "3a";  // NaN

  - Bitwise Operation with strings

        "2" | "4";  // 6

- NaN type

  - use NaN to check a Number

        isNaN(true);  // false
        isNaN(false);  // false
        isNaN(NaN);  // true
        isNaN("any str");  // true

  - Issues with NaN (Not A Number)
  
    ``` 
    var x = NaN;
    ```

        x === NaN;  // false
        x !== NaN;  // true

        // comparing with the self
        x === x;  // false

        // use this to compare NaN
        isNaN(x);  // true
    
      