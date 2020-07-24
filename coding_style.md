# Panda Coding Style

panda coding style follows the [Qt coding style](https://wiki.qt.io/Qt_Coding_Style), if you submit Pull requests to us, please follow these guidelines.

## Indentation

* 4 spaces are used for indentation
* Spaces, not tabs!

## Declaring variables

* Declare each variable on a separate line
* Avoid short or meaningless names (e.g. "a", "rbarr", "nughdeget")
* Single character variable names are only okay for counters and temporaries, where the purpose of the variable is obvious
* Wait when declaring a variable until it is needed

```c++
 // Wrong
 int a, b;
 char *c, *d;

 // Correct
 int height;
 int width;
 char *nameOfThis;
 char *nameOfThat;
```

## Whitespace

```c++
 // Wrong
 if(foo){
 }

 // Correct
 if (foo) {
 }
 ```
 
 * For pointers or references, always use a single space between the type and '*' or '&', but no space between the '*' or '&' and the variable name:
 
 ```c++
 char *x;
 const QString &myString;
 const char * const y = "hello";
 ```
 
* Surround binary operators with spaces
* Leave a space after each comma
* No space after a cast
* Avoid C-style casts when possible

```c++
// Wrong
char* blockOfMemory = (char* ) malloc(data.size());

// Correct
char *blockOfMemory = reinterpret_cast<char *>(malloc(data.size()));
```

* Do not put multiple statements on one line
* By extension, use a new line for the body of a control flow statement:

```c++
 // Wrong
 if (foo) bar();

 // Correct
 if (foo)
     bar();
```

## Braces

```c++
 // Wrong
 if (codec)
 {
 }
 else
 {
 }

 // Correct
 if (codec) {
 } else {
 }
```
