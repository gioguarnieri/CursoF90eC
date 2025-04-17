
## Fundamental data types

### Size in memory

| Type           | Size in memory |
| -------------- | -------------- |
| char           | 1 byte         |
| unsigned char  | 1 byte         |
| signed char    | 1 byte         |
| int            | 2 or 4 bytes   |
| unsigned int   | 2 or 4 bytes   |
| short          | 2 bytes        |
| unsigned short | 2 bytes        |
| long           | 8 bytes        |
| unsigned long  | 8 bytes        |


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





## Input and output



[Next: Vectors and Matrices](Vectors%20and%20Matrices%20in%20C)
