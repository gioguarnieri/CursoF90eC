[HelloWorld.c](HelloWorld.c.md)
```C
#include <stdio.h>  
  
int main() {  
  printf("Hello World!");  
  return 0;  
}
```

## \#include <stdio.h>
The include in C calls for headers. It is similar from the "import" in Python, however, it can calls for other files, not only modules and packages.

Here, it is calling the STanDard In and Out library of C.

C is a highly optimized language, hardly you'll call for libraries that you won't use extensively.

## int main()

The "int" is exactly what you are thinking. The main function is declared as an integer. Notice that at the end, there is a "return 0". This means that if the code runs well, it will return a 0 value to your OS.

Here we are create our "main" function. Without a main function your program won't do much besides declaring [Functions](Functions%20in%20C.md). The code inside the brackets {} will be executed.

## The "printf("Hello World!");" 

The printf is a basic print function of C. It shows the message inside " " in the terminal. Notice how the line ends with ; 

Every line in C needs a ; to close.

Yes, it is annoying.

C ignores white space completely, the code could be written as 

```C
int main(){printf("Hello World!");return 0;}
```

But why would you do that?

[Next: Declaring variables](Declaring%20and%20obtaining%20variables%20in%20C.md)
