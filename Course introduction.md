This course is made minding people who already know how to program. However, we won't leave the non-programmers exploded in the sidewalk. If you don't know what I am talking about, and it is in purple, click on it to lead you to an explanation.

So, we start the course talking about what is different between C and F90 from Python and R (maybe others but idk).

## C

C is a general-purpose programming language. It was created in the 1970s by Dennis Ritchie and remains very widely used and influential.

A successor to the programming language B, C was originally developed at Bell Labs by Ritchie between 1972 and 1973 to construct utilities running on Unix. It was applied to re-implementing the kernel of the Unix operating system. During the 1980s, C gradually gained popularity. It has become one of the most widely used programming languages, with C compilers available for practically all modern computer architectures and operating systems. [Source: Wikipedia](https://en.wikipedia.org/wiki/C_(programming_language))

## Fortran 90

Fortran (FORmula TRANslation) was originally developed by IBM with a reference manual being released in 1956, however the first compilers only began to produce accurate code two years later. Fortran computer programs have been written to support scientific and engineering applications, such as numerical weather prediction, finite element analysis, computational fluid dynamics, plasma physics, geophysics, computational physics, crystallography and computational chemistry. It is a popular language for high-performance computing and is used for programs that benchmark and rank the world's fastest supercomputers. [Source: Wikipedia](https://en.wikipedia.org/wiki/Fortran) 
## Compiled language
### Advantages
- [Lower level language](Lower%20level%20language.md);
- Better hardware control;
- Embedded optimization in the [Compiler](Compiler.md); 
- Faster code execution.
### Disadvantages
- Harder to programmers understand;
- Easier to make a mess;
- Windows hates you if you try to compile things.

## [Variables](Variables.md)
The basic types, same as Python and R. But a little different:
#### They have to be declared before you use them and they are not [Objects](Objects.md).

In Python all variables are objects. Most of them have built-in functions i.e. list.append(x) called methods. However, if you want an object in C and F90 you need to create it yourself (and it is boooooooooring, and kind of advanced, so I'm not going to teach it here).

What does it means? Let's see in the example: [#Same operation in Python, C and F90](#Same%20operation%20in%20Python,%20C%20and%20F90)

## Running and creating [vectors](vectors)

You have to know the size of the vector you are going to need. If you do not, you are looking for a [List](List).
## Same operation in Python, C and F90

### Multiplying matrices in C
``` C
// C program to multiply two matrices
#include <stdio.h>
#include <stdlib.h>

// matrix dimensions so that we dont have to pass them as
// parameters mat1[R1][C1] and mat2[R2][C2]
#define R1 2 // number of rows in Matrix-1
#define C1 2 // number of columns in Matrix-1
#define R2 2 // number of rows in Matrix-2
#define C2 3 // number of columns in Matrix-2
void multiplyMatrix(int m1[][C1], int m2[][C2]){
	int result[R1][C2];
	printf("Resultant Matrix is:\n");
	for (int i = 0; i < R1; i++) {
		for (int j = 0; j < C2; j++) {
			result[i][j] = 0;
			for (int k = 0; k < R2; k++) {
				result[i][j] += m1[i][k] * m2[k][j];
			}
			printf("%d\t", result[i][j]);
		}
		printf("\n");
	}
}

// Driver code
int main(){
	int m1[R1][C1] = { { 1, 1 }, { 2, 2 } };
	int m2[R2][C2] = { { 1, 1, 1 }, { 2, 2, 2 } };
	// if coloumn of m1 not equal to rows of m2
	if (C1 != R2) {
		printf("The number of columns in Matrix-1 must be "
			"equal to the number of rows in "
			"Matrix-2\n");
		printf("Please update MACROs value according to "
			"your array dimension in "
			"#define section\n");
		exit(EXIT_FAILURE);
	}
	// Function call
	multiplyMatrix(m1, m2);
	return 0;
}
```

### Multiplying matrices in F90

```Fortran
program matmul_example
  implicit none

  real, allocatable, dimension(:,:) :: A, B, C
  integer :: n
  integer :: i, j

  n = 3

  allocate( A(n,n), B(n,n), C(n,n) )

  ! Make A and B unit matrices
  A = 0.0
  B = 0.0

  do i=1,n
    A(i,i) = 1.0
    B(i,i) = 1.0
  end do

  ! Make C a zero matrix
  C = 0.0

  ! Multiply C = A * B, C should be a unit matrix now
  C = matmul(A,B)

  do i=1,n
      print *, ( C(i,j), j=1,n )
  end do

  deallocate(A,B,C)

end program matmul_example
```


### Multiplying matrices in Python
```Python
import numpy as np
np.random.seed(666)
N = 10
A = np.random.rand(N,N)
B = np.random.rand(N,N)
AxB = np.dot(A,B)

AxB
```
Notice that we even generated a random matrix, while in the others we did it as a single pre-defined matrix.

Actually C can be way simpler (and faster) than that when using LAPACK (Linear Algebra Package). But installing and using LAPACK isn't as easy as "pip install LAPACK"

We are going to use the website https://onecompiler.com to run our code, since it is simpler than installing GCC

Let's start to understand the language in [Dissecting the Hello world](Dissecting%20the%20Hello%20world.md).