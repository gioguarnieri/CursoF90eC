
## Fundamental data types

### Declaring variables and their size in memory


```C
#include <stdio.h>

int main() {
    // Basic types
    char c;
    short s;
    int i;
    long l;
    long long ll;
    float f;
    double d;
    long double ld;
    
    // Print sizes using sizeof
    printf("Basic types:\n");
    printf("char:          %2zu bytes\n", sizeof(c));
    printf("short:         %2zu bytes\n", sizeof(s));
    printf("int:           %2zu bytes\n", sizeof(i));
    printf("long:          %2zu bytes\n", sizeof(l));
    printf("long long:     %2zu bytes\n", sizeof(ll));
    printf("float:         %2zu bytes\n", sizeof(f));
    printf("double:        %2zu bytes\n", sizeof(d));
    printf("long double:   %2zu bytes\n", sizeof(ld));


    return 0;
}
```

>[!question]- Output
>Basic types:
char:           1 bytes
short:          2 bytes
int:            4 bytes
long:           8 bytes
long long:      8 bytes
float:          4 bytes
double:         8 bytes
long double:   16 bytes



### Limits

```C
#include <stdio.h>
#include <stdlib.h>
#include <limits.h>
#include <float.h>

int main(int argc, char** argv) {

   printf("CHAR_BIT    :   %d\n", CHAR_BIT);
   printf("CHAR_MAX    :   %d\n", CHAR_MAX);
   printf("CHAR_MIN    :   %d\n", CHAR_MIN);
   printf("INT_MAX     :   %d\n", INT_MAX);
   printf("INT_MIN     :   %d\n", INT_MIN);
   printf("LONG_MAX    :   %ld\n", (long) LONG_MAX);
   printf("LONG_MIN    :   %ld\n", (long) LONG_MIN);
   printf("SCHAR_MAX   :   %d\n", SCHAR_MAX);
   printf("SCHAR_MIN   :   %d\n", SCHAR_MIN);
   printf("SHRT_MAX    :   %d\n", SHRT_MAX);
   printf("SHRT_MIN    :   %d\n", SHRT_MIN);
   printf("UCHAR_MAX   :   %d\n", UCHAR_MAX);
   printf("UINT_MAX    :   %u\n", (unsigned int) UINT_MAX);
   printf("ULONG_MAX   :   %lu\n", (unsigned long) ULONG_MAX);
   printf("USHRT_MAX   :   %d\n", (unsigned short) USHRT_MAX);

   return 0;
}

```

>[!question]- Output
>CHAR_BIT    :   8
>CHAR_MAX    :   127
>CHAR_MIN    :   -128
>INT_MAX     :   2147483647
>INT_MIN     :   -2147483648
>LONG_MAX    :   9223372036854775807
>LONG_MIN    :   -9223372036854775808
>SCHAR_MAX   :   127
>SCHAR_MIN   :   -128
>SHRT_MAX    :   32767
>SHRT_MIN    :   -32768
>UCHAR_MAX   :   255
>UINT_MAX    :   4294967295
>ULONG_MAX   :   18446744073709551615
>USHRT_MAX   :   65535

## Output and input

### Specifiers

```C
#include <stdio.h>
#include <stdint.h>

int main() {
    // Character types
    char c = 'A';

    // Integer types
    short s = -32768;
    unsigned short us = 65535;
    int i = -2147483648;
    unsigned int ui = 4294967295U;
    long l = -2147483647L;
    unsigned long ul = 4294967295UL;
    long long ll = -9223372036854775807LL;
    unsigned long long ull = 18446744073709551615ULL;

    // Floating-point types
    float f = 3.14159F;
    double d = 3.141592653589793;
    long double ld = 3.14159265358979323846L;

    // String
    char str[] = "Hello, World!";


    // Printing using format specifiers
    printf("Character types:\n");
    printf("char:          %c\n", c);          // %c for character

    printf("Integer types:\n");
    printf("short:         %hd\n", s);        // %hd for short
    printf("unsigned short:%hu\n", us);       // %hu for unsigned short
    printf("int:           %d\n", i);         // %d for int
    printf("unsigned int:  %u\n", ui);        // %u for unsigned int
    printf("long:          %ld\n", l);        // %ld for long
    printf("unsigned long: %lu\n", ul);       // %lu for unsigned long
    printf("long long:     %lld\n", ll);      // %lld for long long
    printf("unsigned llong:%llu\n\n", ull);   // %llu for unsigned long long

    printf("Floating-point types:\n");
    printf("float:         %.2f\n", f);       // %f for float (6 decimal digits default)
    printf("double:        %.15lf\n", d);     // %lf for double
    printf("long double:   %.21Lf\n\n", ld);  // %Lf for long double

    printf("String:\n");
    printf("string:        %s\n\n", str);     // %s for null-terminated strings

    return 0;
}
```




[Next: Vectors and Matrices](Vectors%20and%20Matrices%20in%20C)
