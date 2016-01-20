# Introduction

*Assigned: 2016-01-20*

*Due: 2016-01-29 11:59:59 PM EST*

This is the Lab 2 assignment for ECE 1120 - C Programming for ECE.

The goals of this lab are to introduce you to different C types,
arithmetic, and printing.

**Be sure to put your name in a comment at the top of each program you
write.**

# Steps

## Part 1

Write a program called `part1.c` that declares and initializes two
integer variables `x` and `y` with the values `35` and `14`, and
displays and calculates their sum, product, integer quotient and
floating-point division quotient.


The output should exactly look like this:
```
35 + 14 = 49
35 * 14 = 490
35 // 14 = 2
35 % 14 = 7
35 / 14 = 22.500000
```

In order to produce this output, use printf to display text
combined with values of variables!

If you change the initial values of `x` and `y`, you should only have
to modify this in a single place in the program.

Add a comment to explain what you had to do in order to do
floating-point division, and why it was necessary.

## Part 2

Copy the previous program into a file called `part2.c`. 

In this copy, modify the values of `x` and `y` to `a=123456789` and
`b=1000`. Run the program and explain the results in a comment. Do the
modifications needed in order to get the correct result.

## Part 3

Write a program called `part3.c` that declares a variable named letter
of type `char` and initializes it with the constant 'C'.

Print this variable as a character *and* as an integer.  Add the
following statement: `letter=letter+1;` Print the updated value for
variable letter, as a character and as an integer, explain the result
in comment.

## Part 4 -- Floating-point Precision

Write a program called `part4.c` with the following contents. Run it
and add a comment to explain the output.

```
#include <stdio.h>

/* ECE1120 - Lab 2 part 4
 * by Your Name Here.
 */

int main(void)
{
	double a, b;
	b = 2.0e20 + 1.0;
	a = b - 2.0e20;
	printf("%f \n", a);
	return 0;
}

```

## Part 5 -- Floating-point Overflow

Write a program called `part5.c` with the following contents. Run it
and add a comment to explain the output.

```
#include <stdio.h>

/* ECE1120 - Lab 2 part 5
 * by Your Name Here.
 */

int main(void)
{
	double number = 3.4E307;
	printf("number is %e\n", number);
	number=number * 10000.0;
	printf("number multiplied by 10000 is %e\n", number);
	return 0;
}

```

## Part 6 -- Simple Calculator (30 points)

Write a program called `part6.c` with the following contents.

```
#include <stdio.h>

/* ECE1120 - Lab 2 part 6
 * by Your Name Here.
 */

int main(void)
{
	int x, y;
	char c;

	printf("enter first number:\n");
	scanf("%d", &x);
	printf("the first number is %d\n", x);

	printf("enter second number:\n");
	scanf("%d", &y);
	printf("the second number is %d\n", y);

	printf("enter a character:\n");
	scanf("\n%c", &c);
	printf("the character is %c\n", c);

	/* Note: the newline in the scanf for a single character is needed
	 * because the %c specifier does not ignore whitespace by
	 * default.
	 */

	if (c == '&') {
		printf("the character is an ampersand\n");
	}

	return 0;
}
```

What happens when an invalid integer is entered in the above program?
Write this in a comment.

Modify the above code to compute a result in a new variable based on
the character. For example, if the user enters a `*`, compute and
print `x * y`. Do this for the operators: `+`, `-`, `*`, `/`. 

You will have to write a conditional `if` statement to do
this. Use the `if` statement in the example as a guidline.

### Example Output
Make the program output look like the following:

```
$. /part6
enter first number:
11
enter second number:
22
enter an operator:
+
11 + 22 is 33

$ ./part6
enter first number:
16
enter second number:
137
enter an operator:
*
16 * 137 is 2192

```

(In the above, the `$ ./part6` shows the program being started. You
don't have to print this from inside your program.)

## Grading Rubric

Parts 1-5 are worth 10 points each. Part 6 is worth 30 points.

For each part, the rubric is:


```
Program compiles                       : 10%
Program compiles with no warnings      : 10%
Some output generated                  : 10%

Correct output                         : 40%
Quality of explanation in comment      : 30%


Total : 100%
```

You will receive *at most* 10% if your program does not compile. You
will receive *at most* 20%if your program compiles with warnings.

You will lose 2 points if you do not put your name in a comment near
the top of the program. 

