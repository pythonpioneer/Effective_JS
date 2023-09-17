## Strict Mode in JavaScript

In your own projects, you could stick to a “strict-mode only” or “non- strict-mode only” policy, but if you want to write robust code that can be combined with a wide variety of code, you have a few alternatives.

Never concatenate strict files and nonstrict files. This is probably the easiest solution, but it of course restricts the amount of control you have over the file structure of your application or library. At best, you have to deploy two separate files, one containing all the strict files and one containing the nonstrict files.

Concatenate files by wrapping their bodies in immediately invoked function expressions. Item 13 provides an in-depth explanation of immediately invoked function expressions (IIFEs), but in short, by wrapping each file’s contents in a function, they can be independently interpreted in different modes.

### Important Note

- Decide which versions of JavaScript your application supports.
- Be sure that any JavaScript features you use are supported by all environments where your application runs.
- Always test strict code in environments that perform the strict- mode checks.
- Beware of concatenating scripts that differ in their expectations about strict mode.