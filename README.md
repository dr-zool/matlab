# matlab
Matlab for Beginner by Dr Zool
------------------------------------------------------------------------------------------------------------------------------
Chapter 1: 
Tutorial lessons 1

1.1	Introduction

The tutorials are independent of the rest of the document. The primarily objective is to help you learn quickly the flrst steps. The emphasis here is \learning by doing". Therefore, the best way to learn is by trying it yourself. Working through the examples will give you a feel for the way that MATLAB operates. In this introduction we will describe how MATLAB handles simple numerical expressions and mathematical formulas.
The name MATLAB stands for MATrix LABoratory. MATLAB was written originally to provide easy access to matrix software developed by the LINPACK (linear system package) and EISPACK (Eigen system package) projects.

1.2	A minimum MATLAB session

The goal of this minimum session (also called starting and exiting sessions) is to learn the flrst steps:
†	How to log on
†	Invoke MATLAB
†	Do a few simple calculations
†	How to quit MATLAB

1.3.1	Starting MATLAB
After logging into your account, you can enter MATLAB by double-clicking on the MATLAB shortcut icon (MATLAB 7.0.4) on your Windows desktop. When you start MATLAB, a special window called the MATLAB desktop appears. The desktop is a window that contains other windows. The major tools within or accessible from the desktop are:

†	The Command Window
†	The Command History
†	The Workspace
†	The Current Directory
†	The Help Browser
†	The Start button
 
When MATLAB is started for the flrst time, the screen looks like the one that shown in the Figure 1.1. This illustration also shows the default conflguration of the MATLAB desktop. You can customize the arrangement of tools and documents to suit your needs.
Now, we are interested in doing some simple calculations. We will assume that you have su–cient understanding of your computer under which MATLAB is being run.
You are now faced with the MATLAB desktop on your computer, which contains the prompt (>>) in the Command Window. Usually, there are 2 types of prompt:

>>	for full version
EDU>	for educational version

Note: To simplify the notation, we will use this prompt, >>, as a standard prompt sign, though our MATLAB version is for educational purpose.


1.3.2	Using MATLAB as a calculator
As an example of a simple interactive calculation, just type the expression you want to evaluate. Let’s start at the very beginning. For example, let’s suppose you want to calculate the expression, 1 + 2 £ 3. You type it at the prompt command (>>) as follows,

>>	1+2*3 

You will have noticed that if you do not specify an output variable, MATLAB uses a default variable ans, short for answer, to store the results of the current calculation. Note that the variable ans is created (or overwritten, if it is already existed). To avoid this, you may assign a value to a variable or output argument name. For example,

>>	x = 1+2*3;

will result in x being given the value 1 + 2 £ 3 = 7. This variable name can always be used to refer to the results of the previous computations. Therefore, computing 4x will result in

>>	4*x;

Before we conclude this minimum session, Table 1.1 gives the partial list of arithmetic operators.
 
Symbol	Operation	Example
		
+	Addition	2 + 3
-	Subtraction	2 - 3
*	Multiplication	2 * 3
/	Division	2/3
		
1.3.3	Quitting MATLAB
To end your MATLAB session, type quit in the Command Window, or select File then Exit MATLAB in the desktop main menu.

1.4	Getting started
After learning the minimum MATLAB session, we will now learn to use some additional operations.

1.4.1	Creating MATLAB variables
MATLAB variables are created with an assignment statement. The syntax of variable as-signment is variable name = a value (or an expression)

For example,
>> x = expression

where expression is a combination of numerical values, mathematical operators, variables, and function calls. On other words, expression can involve:

†	manual entry
†	built-in functions
†	user-deflned functions
 
1.4.2	Overwriting variable

Once a variable has been created, it can be reassigned. In addition, if you do not wish to see the intermediate results, you can suppress the numerical output by putting a semicolon (;) at the end of the line. Then the sequence of commands looks like this:

>>	t = 5;
>>	t = t+1 
t = 6

1.4.3	Error messages
If we enter an expression incorrectly, MATLAB will return an error message. For example, in the following, we left out the multiplication sign, *, in the following expression

>>	x = 10;
>>	5x;

1.4.4	Making corrections
To make corrections, we can, of course retype the expressions. But if the expression is lengthy, we make more mistakes by typing a second time. A previously typed command can be recalled with the up-arrow key ". When the command is displayed at the command prompt, it can be modifled if needed and executed.

1.4.5	Controlling the hierarchy of operations or precedence
Let’s consider the previous arithmetic operation, but now we will include parentheses. For example, 1 + 2 £ 3 will become (1 + 2) £ 3

>>	(1+2)*3;

and, from previous example

>>	1+2*3;

By adding parentheses, these two expressions give difierent results: 9 and 7.

The order in which MATLAB performs arithmetic operations is exactly that taught in high school algebra courses. Exponentiations are done flrst, followed by multiplications and divisions, and flnally by additions and subtractions. However, the standard order of precedence of arithmetic operations can be changed by inserting parentheses. For example, the result of 1+2£3 is quite difierent than the similar expression with parentheses (1+2)£3. The results are 7 and 9 respectively. Parentheses can always be used to overrule priority, and their use is recommended in some complex expressions to avoid ambiguity.
Therefore, to make the evaluation of expressions unambiguous, MATLAB has estab-lished a series of rules. The order in which the arithmetic operations are evaluated is given in below. MATLAB arithmetic operators obey the same precedence rules as those in most computer programs.

[Precedence	Mathematical operations]
First:	The contents of all parentheses are evaluated flrst, starting from the innermost parentheses and working outward.
Second:	All exponentials are evaluated, working from left to right
Third:	All multiplications and divisions are evaluated, working from left to right
Fourth	All additions and subtractions are evaluated, starting from left to right
	
For operators of equal precedence, evaluation is from left to right. Now, consider another example in MATLAB:

>>	1/(2+3^2)+4/5*6/7;

or, if parentheses are missing,
>>	1/2+3^2+4/5*6/7;
 
So here what we get: two different results. Therefore, we want to emphasize the importance of precedence rule in order to avoid ambiguity.

1.4.6	Controlling the appearance of floating point number
MATLAB by default displays only 4 decimals in the result of the calculations, for example -163.6667, as shown in above examples. However, MATLAB does numerical calculations in double precision, which is 15 digits. The command format controls how the results of computations are displayed. Here are some examples of the difierent formats together with the resulting outputs.

>>	format short
>>	x = -163.6667

If we want to see all 15 digits, we use the command format long

>>	format long
>>	x = -1.636666666666667e+002

To return to the standard format, enter format short, or simply format.
There are several other formats. For more details, see the MATLAB documentation, or type help format.

Note - Up to now, we have let MATLAB repeat everything that we enter at the prompt (>>). Sometimes this is not quite useful, in particular when the output is pages en length. To prevent MATLAB from echoing what we type, simply enter a semicolon (;) at the end of the command. For example,

>> x = -163.6667;

and then ask about the value of x by typing,

>>	x 
x = -163.6667

1.4.7	Managing the workspace
The contents of the workspace persist between the executions of separate commands. Therefore, it is possible for the results of one problem to have an efiect on the next one. To avoid this possibility, it is a good idea to issue a clear command at the start of each new inde-pendent calculation.

>> clear

The command clear or clear all removes all variables from the workspace. This frees up system memory. In order to display a list of the variables currently in the memory, type

>> who

while, whos will give more details which include size, space allocation, and class of the variables.


1.4.8	Keeping track of your work session
It is possible to keep track of everything done during a MATLAB session with the diary command.

>> diary

or give a name to a created flle,

>> diary FileName

where FileName could be any arbitrary name you choose.

The function diary is useful if you want to save a complete MATLAB session. They save all input and output as they appear in the MATLAB window. When you want to stop the recording, enter diary off. If you want to start recording again, enter diary on. The flle that is created is a simple text flle. It can be opened by an editor or a word processing program and edited to remove extraneous material, or to add your comments. You can use the function type to view the diary flle or you can edit in a text editor or print. This command is useful, for example in the process of preparing a homework or lab submission.

1.4.9	Entering multiple statements per line

It is possible to enter multiple statements per line. Use commas (,) or semicolons (;) to enter more than one statement at once. Commas (,) allow multiple statements per line without suppressing output.

>>	a=7; b=cos(a), c=cosh(a) 
b = 0.6570 
c = 548.3170
 
1.4.10	Miscellaneous commands

Here are few additional useful commands:
†	To clear the Command Window, type clc
†	To abort a MATLAB computation, type ctrl-c
†	To continue a line, type . . .

1.4.11	Getting help
To view the online documentation, select MATLAB Help from Help menu or MATLAB Help directly in the Command Window. The preferred method is to use the Help Browser. The Help Browser can be started by selecting the ? icon from the desktop toolbar. On the other hand, information about any command is available by typing
>> help Command

Another way to get help is to use the lookfor command. The lookfor command difiers from the help command. The help command searches for an exact function name match, while the lookfor command searches the quick summary information in each function for a match. For example, suppose that we were looking for a function to take the inverse of a matrix. Since MATLAB does not have a function named inverse, the command help inverse will produce nothing. On the other hand, the command lookfor inverse will produce detailed information, which includes the function of interest, inv.

>> lookfor inverse

Note - At this particular time of our study, it is important to emphasize one main point. Because MATLAB is a huge program; it is impossible to cover all the details of each function one by one. However, we will give you information how to get help. Here are some examples:

†	Use on-line help to request info on a speciflc function

>>	help sqrt

†	In the current version (MATLAB version 7), the doc function opens the on-line version of the help manual. This is very helpful for more complex commands.

>>	doc plot
 
†	Use lookfor to find functions by keywords. The general form is

>>	lookfor FunctionName


-------------------------------------------------------------------------------------------------------------------------------
Chapter 2

Tutorial lessons 2

2.1	Mathematical functions

MATLAB offers many predeflned mathematical functions for technical computing which contains a large set of mathematical functions.

Typing help elfun and help specfun calls up full lists of elementary and special functions respectively. There is a long list of mathematical functions that are built into MATLAB. These functions are called built-ins. Many standard mathematical functions, such as sin(x), cos(x), tan(x), ex, ln(x), are evaluated by the functions sin, cos, tan, exp, and log respectively in
MATLAB.

Table below lists some commonly used functions, where variables x and y can be numbers, vectors, or matrices.

Elementary functions
cos(x)	Cosine	abs(x)	Absolute value
sin(x)	Sine	sign(x)	Signum function
tan(x)	Tangent	max(x)	Maximum value
acos(x)	Arc cosine	min(x)	Minimum value
asin(x)	Arc sine	ceil(x)	Round towards +1
atan(x)	Arc tangent	floor(x)	Round towards ¡1
exp(x)	Exponential	round(x)	Round to nearest integer
sqrt(x)	Square root	rem(x)	Remainder after division
log(x)	Natural logarithm	angle(x)	Phase angle
log10(x)	Common logarithm	conj(x)	Complex conjugate
			

In addition to the elementary functions, MATLAB includes a number of predeflned constant values. A list of the most common values is given below.

Pre-defined constant values
pi	: The … number, … = 3:14159
i,j	: The imaginary unit i,	sqrt(-1)
Inf     : Infinity
NaN	: Not a number

2.1.1	Examples

We illustrate here some typical examples which related to the elementary functions previously deflned.

As a flrst example, the value of the expression y = e¡a sin(x) + 10py, for a = 5, x = 2, and y = 8 is computed by


>>	a = 5; x = 2; y = 8;
>>	y = exp(-a)*sin(x)+10*sqrt(y);

The subsequent examples are
>>	log(142);
>>	log10(142);

Note the difference between the natural logarithm log(x) and the decimal logarithm (base 10) log10(x). To calculate sin(…=4) and e10, we enter the following commands in MATLAB,

>>	sin(pi/4) 
ans = 0.7071

>>	exp(10) 
ans = 2.2026e+004

2.2	Basic plotting

2.2.1	Overview
MATLAB has an excellent set of graphic tools. Plotting a given data set or the results of computation is possible with very few commands. You are highly encouraged to plot mathematical functions and results of analysis as often as possible. Trying to understand mathematical equations with graphics is an enjoyable and very e–cient way of learning math-ematics. Being able to plot mathematical functions and data freely is the most important step, and this section is written to assist you to do just that.

2.2.2	Creating simple plots
The basic MATLAB graphing procedure, for example in 2D, is to take a vector of x-coordinates, x = (x1; : : : ; xN ), and a vector of y-coordinates, y = (y 1; : : : ; yN ), locate the points (xi; yi), with i = 1; 2; : : : ; n and then join them by straight lines. You need to prepare x and y in an identical array form; namely, x and y are both row arrays or column arrays of the same length.
The MATLAB command to plot a graph is plot(x,y). The vectors x = (1; 2; 3; 4; 5; 6) and y = (3; ¡1; 2; 4; 5; 1) produce the picture shown in Figure 2.1.

>>	x = [1 2 3 4 5 6];
>>	y = [3 -1 2 4 5 1];
>>	plot(x,y)

Note: The plot functions has difierent forms depending on the input arguments. If y is a vector plot(y)produces a piecewise linear graph of the elements of y versus the index of the elements of y. If we specify two vectors, as mentioned above, plot(x,y) produces a graph of y versus x.
For example, to plot the function sin (x) on the interval [0; 2…], we flrst create a vector of x values ranging from 0 to 2…, then compute the sine of these values, and flnally plot the result:
 
>>	x = 0:pi/100:2*pi;
>>	y = sin(x);
>>	plot(x,y)

Notes:

†	0:pi/100:2*pi yields a vector that { starts at 0, { takes steps (or increments) of …=100, { stops when 2… is reached.
†	If you omit the increment, MATLAB automatically increments by 1.

2.2.3	Adding titles, axis labels, and annotations

MATLAB enables you to add axis labels and titles. For example, using the graph from the previous example, add an x- and y-axis labels.
Now label the axes and add a title. The character \pi creates the symbol …. An example of 2D plot is shown in Figure 2.2.
 
>>	xlabel(’x = 0:2\pi’)
>>	ylabel(’Sine of x’)
>>	title(’Plot of the Sine function’)

The color of a single curve is, by default, blue, but other colors are possible. The desired color is indicated by a third argument. For example, red is selected by plot(x,y,’r’). Note the single quotes, ’ ’, around r.

2.2.4	Multiple data sets in one plot

Multiple (x; y) pairs arguments create multiple graphs with a single call to plot. For example, these statements plot three related functions of x: y1 = 2 cos(x), y2 = cos(x), and y3 = 0:5 ⁄ cos(x), in the interval 0 • x • 2….

>>	x = 0:pi/100:2*pi;
>>	y1 = 2*cos(x);
>>	y2 = cos(x);
>>	y3 = 0.5*cos(x);
>>	plot(x,y1,’--’,x,y2,’-’,x,y3,’:’)
>>	xlabel(’0 \leq x \leq 2\pi’)
>>	ylabel(’Cosine functions’)
>>	legend(’2*cos(x)’,’cos(x)’,’0.5*cos(x)’)
>>	title(’Typical example of multiple plots’)
>>	axis([0 2*pi -3 3])

The result of multiple data sets in one graph plot is shown in Figure 2.3.

By default, MATLAB uses line style and color to distinguish the data sets plotted in the graph. However, you can change the appearance of these graphic components or add annotations to the graph to help explain your data for presentation.


2.2.5	Specifying line styles and colors

It is possible to specify line styles, colors, and markers (e.g., circles, plus signs, . . . ) using the plot command:  plot(x,y,’style_color_marker’)
where style_color_marker is a triplet of values from Table 2.3.

To find additional information, type help plot or doc plot.

Attributes for plot

Symbol	Color	Symbol	Line Style	Symbol	Marker
k	Black	¡	Solid	+	Plus sign
r	Red	¡¡	Dashed	o	Circle
b	Blue	:	Dotted	⁄	Asterisk
g	Green	¡:	Dash-dot	:	Point
c	Cyan	none	No line	£	Cross
m	Magenta			s	Square
y	Yellow			d	Diamond
					
2.4	Introduction

Matrices are the basic elements of the MATLAB environment. A matrix is a two-dimensional array consisting of m rows and n columns. Special cases are column vectors (n = 1) and row vectors (m = 1).
In this section we will illustrate how to apply difierent operations on matrices. The following topics are discussed: vectors and matrices in MATLAB, the inverse of a matrix, determinants, and matrix manipulation.
MATLAB supports two types of operations, known as matrix operations and array opera-tions. Matrix operations will be discussed flrst.


2.5	Matrix generation
Matrices are fundamental to MATLAB. Therefore, we need to become familiar with matrix generation and manipulation. Matrices can be generated in several ways.

2.5.1	Entering a vector
A vector is a special case of a matrix. The purpose of this section is to show how to create vectors and matrices in MATLAB. As discussed earlier, an array of dimension 1 £n is called a row vector, whereas an array of dimension m £ 1 is called a column vector. The elements of vectors in MATLAB are enclosed by square brackets and are separated by spaces or by commas. For example, to enter a row vector, v, type

>>	v = [1 4 7 10 13];

Column vectors are created in a similar way, however, semicolon (;) must separate the components of a column vector,

>>	w = [1;4;7;10;13];

On the other hand, a row vector is converted to a column vector using the transpose operator. The transpose operation is denoted by an apostrophe or a single quote (’).
>>	w = v’;
 
Thus, v(1) is the flrst element of vector v, v(2) its second element, and so forth. Furthermore, to access blocks of elements, we use MATLAB’s colon notation (:). For exam-ple, to access the flrst three elements of v, we write,

>>	v(1:3);

Or, all elements from the third through the last elements,

>>	v(3,end);

where end signifles the last element in the vector. If v is a vector, writing

>> v(:)

produces a column vector, whereas writing

>> v(1:end)

produces a row vector.


2.5.2	Entering a matrix

A matrix is an array of numbers. To type a matrix into MATLAB you must

†	begin with a square bracket, [
†	separate elements in a row with spaces or commas (,)
†	use a semicolon (;) to separate rows
†	end the matrix with another square bracket, ].

Here is a typical example. To enter a matrix A, type,

>> A=[123;456;789]

MATLAB then displays the 3 x 3 matrix as follows,

A   =		[
1	2	3
4	5	6
7	8	9]

Note that the use of semicolons (;) here is difierent from their use mentioned earlier to suppress output or to write multiple commands in a single line.

Once we have entered the matrix, it is automatically stored and remembered in the Workspace. We can refer to it simply as matrix A. We can then view a particular element in a matrix by specifying its location. We write,

>>	A(2,1);

A(2,1) is an element located in the second row and flrst column. Its value is 4.


2.5.3	Matrix indexing

We select elements in a matrix just as we did for vectors, but now we need two indices. The element of row i and column j of the matrix A is denoted by A(i,j). Thus, A(i,j) in MATLAB refers to the element Aij of matrix A. The flrst index is the row number and the second index is the column number. For example, A(1,3) is an element of flrst row and third column. Here, A(1,3)=3.

Correcting any entry is easy through indexing. Here we substitute A(3,3)=9 by A(3,3)=0. The result is

>>	A(3,3) = 0;

Single elements of a matrix are accessed as A(i,j), where i ‚ 1 and j ‚ 1. Zero or negative subscripts are not supported in MATLAB.


2.5.4	Colon operator

The colon operator will prove very useful and understanding how it works is the key to e–cient and convenient usage of MATLAB. It occurs in several difierent forms.

Often we must deal with matrices or vectors that are too large to enter one ele-ment at a time. For example, suppose we want to enter a vector x consisting of points (0; 0:1; 0:2; 0:3; ¢ ¢ ¢ ; 5). We can use the command

>> x = 0:0.1:5;

The row vector has 51 elements.


2.5.5	Linear spacing

On the other hand, there is a command to generate linearly spaced vectors: linspace. It is similar to the colon operator (:), but gives direct control over the number of points. For example,

y = linspace(a,b)

generates a row vector y of 100 points linearly spaced between and including a and b.

y = linspace(a,b,n)

generates a row vector y of n points linearly spaced between and including a and b. This is useful when we want to divide an interval into a number of subintervals of the same length. For example,

>> theta = linspace(0,2*pi,101)

divides the interval [0; 2…] into 100 equal subintervals, then creating a vector of 101 elements.


2.5.6	Colon operator in a matrix

The colon operator can also be used to pick out a certain row or column. For example, the statement A(m:n,k:l specifles rows m to n and column k to l. Subscript expressions refer to portions of a matrix. For example,
 
>>	A(2,:);

is the second row elements of A.

The colon operator can also be used to extract a sub-matrix from a matrix A.

>>	A(:,2:3);

A(:,2:3) is a sub-matrix with the last two columns of A.

A row or a column of a matrix can be deleted by setting it to a null vector, [ ].

>>	A(:,2)=[];

2.5.7	Creating a sub-matrix

To extract a submatrix B consisting of rows 2 and 3 and columns 1 and 2 of the matrix A, do the following

>> B = A([2 3],[1 2]);

To interchange rows 1 and 2 of A, use the vector of row indices together with the colon operator.

>> C = A([2 1 3],:)

C	=		
	4	5	6
	1	2	3
	7	8	0

It is important to note that the colon operator (:) stands for all columns or all rows. To create a vector version of matrix A, do the following
 
 >>	A(:);

The submatrix comprising the intersection of rows p to q and columns r to s is denoted by A(p:q,r:s).

As a special case, a colon (:) as the row or column specifler covers all entries in that row or column; thus

†	A(:,j) is the jth column of A, while
†	A(i,:) is the ith row, and
†	A(end,:) picks out the last row of A.

The keyword end, used in A(end,:), denotes the last index in the specifled dimension. Here are some examples.

>> A		
A  =		
[1	2	3
4	5	6
7	8	9]


>>	A(2:3,2:3);
>>	A(end:-1:1,end);
>>	A([1 3],[2 3]);


2.5.8	Deleting row or column

To delete a row or column of a matrix, use the empty vector operator, [ ].

>>	A(3,:) = [];

Third row of matrix A is now deleted. To restore the third row, we use a technique for creating a matrix

>>	A = [A(1,:);A(2,:);[7 8 0]]

Matrix A is now restored to its original form.

2.5.9	Dimension

To determine the dimensions of a matrix or vector, use the command size. For example,

>>	size(A) 
Or
>> [m,n]=size(A)
 
2.5.10	Continuation

If it is not possible to type the entire input on the same line, use consecutive periods, called an ellipsis : : :, to signal continuation, then continue the input on the next line.

B = [4/5	7.23*tan(x)	sqrt(6); ...
1/x^2	0	3/(x*log(x)); ...
x-7	sqrt(3)	x*sin(x)];

Note that blank spaces around +, ¡, = signs are optional, but they improve readability.


2.5.11	Transposing a matrix

The transpose operation is denoted by an apostrophe or a single quote (’). It °ips a matrix about its main diagonal and it turns a row vector into a column vector. Thus,

>>	A’;

By using linear algebra notation, the transpose of m £ n real matrix A is the n £ m matrix that results from interchanging the rows and columns of A. 

2.5.12	Concatenating matrices

Matrices can be made up of sub-matrices. Here is an example. First, let’s recall our previous matrix A.

A   =		
[1	2	3
4	5	6
7	8	9];

The new matrix B will be,

>>	B=[A10*A;-A[100;010;001]] ;

2.5.13	Matrix generators
MATLAB provides functions that generates elementary matrices. The matrix of zeros, the matrix of ones, and the identity matrix are returned by the functions zeros, ones, and eye, respectively.

Elementary matrices
eye(m,n)	Returns an m-by-n matrix with 1 on the main diagonal
eye(n)	Returns an n-by-n square identity matrix
zeros(m,n)	Returns an m-by-n matrix of zeros
ones(m,n)	Returns an m-by-n matrix of ones
diag(A)	Extracts the diagonal of matrix A
rand(m,n)	Returns an m-by-n matrix of random numbers
	
Here are some examples:
>> b=ones(3,1);

Equivalently, we can deflne b as >> b=[1;1;1]

>> eye(3);	
>> c=zeros(2,3)

In addition, it is important to remember that the three elementary operations of ad-dition (+), subtraction (¡), and multiplication (⁄) apply also to matrices whenever the dimensions are compatible.
Two other important matrix generation functions are rand and randn, which generate matrices of (pseudo-)random numbers using the same syntax as eye.
In addition, matrices can be constructed in a block form. With C deflned by C = [1 2; 3 4], we may create a matrix D as follows

>>	D = [C zeros(2); ones(2) eye(2)];

2.5.14	Special matrices

MATLAB provides a number of special matrices (see Table 2.5). These matrices have inter-esting properties that make them useful for constructing examples and for testing algorithms. For more information, see MATLAB documentation.

Special matrices
hilb	Hilbert matrix
invhilb	Inverse Hilbert matrix
magic	Magic square
pascal	Pascal matrix
toeplitz	Toeplitz matrix
vander	Vandermonde matrix
wilkinson	Wilkinson’s eigenvalue test matrix
--------------------------------------------------------------------------------------------------------------------------
Chapter 3
Array operations and Linear equations

3.1	Array operations
MATLAB has two difierent types of arithmetic operations: matrix arithmetic operations and array arithmetic operations. We have seen matrix arithmetic operations in the previous lab. Now, we are interested in array operations.

3.1.1	Matrix arithmetic operations
As we mentioned earlier, MATLAB allows arithmetic operations: +, ¡, ⁄, and ^ to be carried out on matrices. 

3.1.2	Array arithmetic operations
On the other hand, array arithmetic operations or array operations for short, are done element-by-element. The period character, ., distinguishes the array operations from the matrix operations. However, since the matrix and array operations are the same for addition
(+)	and subtraction (¡), the character pairs (:+) and (:¡) are not used. The list of array operators is shown below in Table 3.2. If A and B are two matrices of the same size with elements A = [aij] and B = [bij], then the command
 
.*	Element-by-element multiplication
./	Element-by-element division
.^	Element-by-element exponentiation

>> C = A.*B

To raise a scalar to a power, we use for example the command 10^2. If we want the operation to be applied to each element of a matrix, we use .^2. For example, if we want to produce a new matrix whose elements are the square of the elements of the matrix A, we enter

>>	A.^2 

The relations below summarize the above operations. To simplify, let’s consider two vectors U and V with elements U = [ui] and V = [vj].

U:⁄V	produces	[u1v1 u2v2 : : : unvn]
U:=V	produces	[u1=v1 u2=v2 : : : un=vn]
U.^V	produces	[u1v1 u2v2 : : : unvn ]

Operation	Matrix	Array
Addition	+	+
Subtraction	-	-
Multiplication	⁄	.⁄
Division	=	.=
Left division	n	.n
Exponentiation	^	.^

3.2	Solving linear equations

One of the problems encountered most frequently in scientiflc computation is the solution of systems of simultaneous linear equations. With matrix notation, a system of simultaneous linear equations is written 
Ax = b	(3.1)

where there are as many equations as unknown. A is a given square matrix of order n, b is a given column vector of n components, and x is an unknown column vector of n components.

In linear algebra we learn that the solution to Ax = b can be written as x = (A^-1)*b

1. The flrst one is to use the matrix inverse, inv
>>	A=[123;456;780];
>>	b = [1; 1; 1];
>>	x = inv(A)*b;

2.	The second one is to use the backslash (n)operator. The numerical algorithm behind this operator is computationally e–cient. This is a numerically reliable way of solving system of linear equations by using a well-known process of Gaussian elimination.
>>	A=[123;456;780];
>>	b = [1; 1; 1];
>>	x = A\b;

This problem is at the heart of many problems in scientiflc computation. Hence it is impor-tant that we know how to solve this type of problem e–ciently.
Now, we know how to solve a system of linear equations. In addition to this, we will see some additional details which relate to this particular topic.

3.2.1	Matrix inverse

In MATLAB, however, it becomes as simple as the following commands:
 
>>	A=[123;456;780];
>>	inv(A);
and the determinant of A is

>>	det(A);

3.2.2	Matrix functions

MATLAB provides many matrix functions for various matrix/vector manipulations; see Table 3.3 for some of these functions. Use the online help of MATLAB to flnd how to use these functions.

Matrix functions
det	Determinant
diag	Diagonal matrices and diagonals of a matrix
eig	Eigenvalues and eigenvectors
inv	Matrix inverse
norm	Matrix and vector norms
rank	Number of linearly independent rows or columns
	
---------------------------------------------------------------------------------------------------------
Chapter 4
Introduction to programming in MATLAB

4.1	Introduction
So far in these lab sessions, all the commands were executed in the Command Window. The problem is that the commands entered in the Command Window cannot be saved and executed again for several times. Therefore, a difierent way of executing repeatedly commands with MATLAB is:

1.	to create a flle with a list of commands,
2.	save the flle, and
3.	run the flle.

If needed, corrections or changes can be made to the commands in the flle. The flles that are used for this purpose are called script flles or scripts for short.
This section covers the following topics:
†	M-File Scripts
†	M-File Functions

4.2	M-File Scripts

A script flle is an external flle that contains a sequence of MATLAB statements. Script flles have a fllename extension .m and are often called M-flles. M-flles can be scripts that simply execute a series of MATLAB statements, or they can be functions that can accept arguments and can produce one or more outputs.

4.2.1	Examples

Here are two simple scripts.

Example 1
†	Use the MATLAB editor to create a flle: File > New > M-flle.
†	Enter the following statements in the flle:

A=[123;334;233];
b = [1; 1; 2];
x = A\b


†	Save the flle, for example, example1.m.
†	Run the flle, in the command line, by typing:

>>	example1;

When execution completes, the variables (A, b, and x) remain in the workspace. To see a listing of them, enter whos at the command prompt.
Note: The MATLAB editor is both a text editor specialized for creating M-flles and a graphical MATLAB debugger. The MATLAB editor has numerous menus for tasks such as saving, viewing, and debugging. Because it performs some simple checks and also uses color to difierentiate between various elements of codes, this text editor is recommended as the tool of choice for writing and editing M-flles.

There is another way to open the editor:
 
>> edit
or
>> edit filename.m

Example 2

Plot the following cosine functions, y1 = 2 cos(x), y2 = cos(x), and y3 = 0:5 ⁄ cos(x), in the interval 0 • x • 2…. This example has been presented in previous Chapter. Here we put the commands in a flle.

†	Create a flle, say example2.m, which contains the following commands:
x = 0:pi/100:2*pi;
y1 = 2*cos(x);
y2 = cos(x);
y3 = 0.5*cos(x);

plot(x,y1,’--’,x,y2,’-’,x,y3,’:’)
xlabel(’0 \leq x \leq 2\pi’)
ylabel(’Cosine functions’)
legend(’2*cos(x)’,’cos(x)’,’0.5*cos(x)’)
title(’Typical example of multiple plots’)
axis([0 2*pi -3 3])

†	Run the flle by typing example2 in the Command Window.

4.2.2	Script side-efiects

All variables created in a script flle are added to the workspace. This may have undesirable efiects, because:
†	Variables already existing in the workspace may be overwritten.
†	The execution of the script can be afiected by the state variables in the workspace.

As a result, because scripts have some undesirable side-efiects, it is better to code any complicated applications using rather function M-flle.

4.3	M-File functions

As mentioned earlier, functions are programs (or routines) that accept input arguments and return output arguments. Each M-flle function (or function or M-flle for short) has its own area of workspace, separated from the MATLAB base workspace.

4.3.1	Anatomy of a M-File function

This simple function shows the basic parts of an M-flle.	
function f = factorial(n)	(1)
% FACTORIAL(N) returns the factorial of N.   (2)
% Compute a factorial value.	(3)
f = prod(1:n);	(4)

The first line of a function M-flle starts with the keyword function. It gives the function name and order of arguments. In the case of function factorial, there are up to one output argument and one input argument. Table 4.1 summarizes the M-flle function.
As an example, for n = 5, the result is,

>>	f = factorial(5);

Anatomy of a M-File function

Part no.	M-flle element	Description
(1)	Function	Deflne the function name, and the
	deflnition	number and order of input and
	line	output arguments
(2)	H1 line	A one line summary description
		of the program, displayed when you
		request Help
(3)	Help text	A more detailed description of
		the program
(4)	Function body	Program code that performs
		the actual computations
		
In addition, it is important to note that function name must begin with a letter, and must be no longer than than the maximum of 63 characters. Furthermore, the name of the text flle that you save will consist of the function name with the extension .m. Thus, the above example flle would be factorial.m.

4.3.2	Input and output arguments
As mentioned above, the input arguments are listed inside parentheses following the function name. The output arguments are listed inside the brackets on the left side. They are used to transfer the output from the function flle. The general form looks like this

function [outputs] = function_name(inputs)

Function flle can have none, one, or several output arguments. Table 4.3 illustrates some possible combinations of input and output arguments.

Example of input and output arguments
function C=FtoC(F)	One input argument and
	one output argument
function area=TrapArea(a,b,h)	Three inputs and one output
function [h,d]=motion(v,angle)	Two inputs and two outputs

4.4	Input to a script flle
When a script flle is executed, the variables that are used in the calculations within the flle must have assigned values. The assignment of a value to a variable can be done in three ways.

1.	The variable is deflned in the script flle.
2.	The variable is deflned in the command prompt.
3.	The variable is entered when the script is executed.

We have already seen the two flrst cases. Here, we will focus our attention on the third one. In this case, the variable is deflned in the script flle. When the flle is executed, the user is prompted to assign a value to the variable in the command prompt. This is done by using the input command. Here is an example.

%	This script file calculates the average of points
%	scored in three games.
%	The point from each game are assigned to a variable
%	by using the ‘input’ command.

game1 = input(’Enter the points scored in the first game ’);
game2 = input(’Enter the points scored in the second game ’); game3 = input(’Enter the points scored in the third game ’); average = (game1+game2+game3)/3

The following shows the command prompt when this script flle (saved as example3) is executed.

>> example3	
>> Enter the points scored in the first game	15
>> Enter	the points scored in the second game	23
>> Enter	the points scored in the third game	10

4.5	Output commands

As discussed before, MATLAB automatically generates a display when commands are exe-cuted. In addition to this automatic display, MATLAB has several commands that can be used to generate displays or outputs.
Two commands that are frequently used to generate output are: disp and fprintf. The main difierences between these two commands can be summarized as follows (Table 4.4).

Table 4.4: disp and fprintf commands
disp	. Simple to use.
. Provide limited control over the appearance of output
fprintf	. Slightly more complicated than disp.
. Provide total control over the appearance of output
-------------------------------------------------------------------------------------------------------------------------
Chapter 5
Control °ow and operators

5.1	Introduction
MATLAB is also a programming language. Like other computer programming languages, MATLAB has some decision making structures for control of command execution. These decision making or control °ow structures include for loops, while loops, and if-else-end constructions. Control °ow structures are often used in script M-flles and function M-flles.
By creating a flle with the extension .m, we can easily write and run programs. We do not need to compile the program since MATLAB is an interpretative (not compiled) language. MATLAB has thousand of functions, and you can add your own using m-flles.
MATLAB provides several tools that can be used to control the °ow of a program (script or function). In a simple program as shown in the previous Chapter, the commands are executed one after the other. Here we introduce the °ow control structure that make possible to skip commands or to execute speciflc group of commands.

5.2	Control 

MATLAB has four control structures: the if statement, the for loop, the while loop, and the switch statement.

5.2.1	The ‘‘if...end’’ structure
MATLAB supports the variants of \if" construct.

†	if ...  end
†	if ...  else ...  end
†	if ...  elseif ...  else ...  end

The simplest form of the if statement is

if expression
statements
end

Here are some examples based on the familiar quadratic formula.

1.	discr = b*b - 4*a*c; if discr < 0
disp(’Warning: discriminant is negative, roots are imaginary’);
end

2.	discr = b*b - 4*a*c; if discr < 0
disp(’Warning: discriminant is negative, roots are imaginary’);
else
disp(’Roots are real, but may be repeated’) end

3.	discr = b*b - 4*a*c; if discr < 0
disp(’Warning: discriminant is negative, roots are imaginary’);
elseif discr == 0
disp(’Discriminant is zero, roots are repeated’) else
disp(’Roots are real’) end

It should be noted that:

†	elseif has no space between else and if (one word)
†	no semicolon (;) is needed at the end of lines containing if, else, end
†	indentation of if block is not required, but facilitate the reading.
†	the end statement is required

5.2.2	Relational and logical operators

A relational operator compares two numbers by determining whether a comparison is true or false. Relational operators are shown in Table 5.1.

Relational and logical operators
Operator	Description
>	Greater than
<Less than
>=	Greater than or equal to
<=	Less than or equal to
==	Equal to
»=	Not equal to
&	AND operator
OR operator
»NOT operator

5.2.3	The ‘‘for...end’’ loop

In the for ... end loop, the execution of a command is repeated at a flxed and predeter-mined number of times. The syntax is

for variable = expression
statements
end

Usually, expression is a vector of the form i:s:j. A simple example of for loop is

for ii=1:5
x=ii*ii
end

It is a good idea to indent the loops for readability, especially when they are nested. Note that MATLAB editor does it automatically.
Multiple for loops can be nested, in which case indentation helps to improve the readability. The following statements form the 5-by-5 symmetric matrix A with (i; j) element i=j for j ‚ i:
 
5.2.4	The ‘‘while...end’’ loop

This loop is used when the number of passes is not specifled. The looping continues until a stated condition is satisfled. The while loop has the form:

while expression
statements
end

The statements are executed as long as expression is true.
x = 1
while x <= 10
x = 3*x
end

It is important to note that if the condition inside the looping is not well deflned, the looping will continue indeflnitely. If this happens, we can stop the execution by pressing Ctrl-C.

5.2.5	Other structures
†	The break statement. A while loop can be terminated with the break statement, which passes control to the flrst statement after the corresponding end. The break statement can also be used to exit a for loop.
†	The continue statement can also be used to exit a for loop to pass immediately to the next iteration of the loop, skipping the remaining statements in the loop.
†	Other control statements include return, continue, switch, etc. For more detail about these commands, consul MATLAB documentation.

5.2.6	Operator precedence
We can build expressions that use any combination of arithmetic, relational, and logical operators. Precedence rules determine the order in which MATLAB evaluates an expression. We have already seen this in the \Tutorial Lessons".
Here we add other operators in the list. The precedence rules for MATLAB are shown in this list (Table 5.2), ordered from highest (1) to lowest (9) precedence level. Operators are evaluated from left to right.

Precedence Operator
1	Parentheses ()
2	Transpose (: 0), power (.^), matrix power (^)
3	Unary plus (+), unary minus (¡), logical negation (»)
4 Multiplication (: ⁄), right division (: =), left division (:n), matrix multiplication (⁄), matrix right division (=), matrix left division (n)
5 Addition (+), subtraction (¡)
6 Colon operator (:)
7 Less than (<), less than or equal to (•), greater (>), greater than or equal to (‚), equal to (==), not equal to (»=)
8 Element-wise AND, (&)
9 Element-wise OR, (j)

5.3	Saving output to a flle
In addition to displaying output on the screen, the command fprintf can be used for writing the output to a flle. The saved data can subsequently be used by MATLAB or other softwares.

To save the results of some computation to a flle in a text format requires the following steps:
1.	Open a flle using fopen
2.	Write the output using fprintf
3.	Close the flle using fclose

Here is an example (script) of its use.
%	write some variable length strings to a file op = fopen(’weekdays.txt’,’wt’); fprintf(op,’Sunday\nMonday\nTuesday\nWednesday\n’); fprintf(op,’Thursday\nFriday\nSaturday\n’); fclose(op);

This flle (weekdays.txt) can be opened with any program that can read .txt flle.

---------------------------------------------------------------------------------------------------------------------
Chapter 6
Debugging M-flles

6.1	Introduction
This section introduces general techniques for flnding errors in M-flles. Debugging is the process by which you isolate and flx errors in your program or code.
Debugging helps to correct two kind of errors:
†	Syntax errors - For example omitting a parenthesis or misspelling a function name.
†	Run-time errors - Run-time errors are usually apparent and di–cult to track down. They produce unexpected results.

6.2	Debugging process

We can debug the M-flles using the Editor/Debugger as well as using debugging functions from the Command Window. The debugging process consists of
†	Preparing for debugging
†	Setting breakpoints
†	Running an M-flle with breakpoints
†	Stepping through an M-flle
†	Examining values
†	Correcting problems
†	Ending debugging

6.2.1	Preparing for debugging

Here we use the Editor/Debugger for debugging. Do the following to prepare for debugging:
†	Open the flle
†	Save changes
†	Be sure the flle you run and any flles it calls are in the directories that are on the search path.

6.2.2	Setting breakpoints

Set breakpoints to pause execution of the function, so we can examine where the problem might be. There are three basic types of breakpoints:

†	A standard breakpoint, which stops at a specifled line.
†	A conditional breakpoint, which stops at a specifled line and under specifled conditions.
†	An error breakpoint that stops when it produces the specifled type of warning, error, NaN, or inflnite value.

6.2.3	Running with breakpoints
After setting breakpoints, run the M-flle from the Editor/Debugger or from the Command Window. Running the M-flle results in the following:
†	The prompt in the Command Window changes to K>>
indicating that MATLAB is in debug mode.

†	The program pauses at the flrst breakpoint. This means that line will be executed when you continue. The pause is indicated by the green arrow.
†	In breakpoint, we can examine variable, step through programs, and run other calling functions.

6.2.4	Examining values
While the program is paused, we can view the value of any variable currently in the workspace. Examine values when we want to see whether a line of code has produced the expected result or not. If the result is as expected, step to the next line, and continue running. If the result is not as expected, then that line, or the previous line, contains an error. When we run a program, the current workspace is shown in the Stack fleld. Use who or whos to list the variables in the current workspace.
First, we position the cursor to the left of a variable on that line. Its current value appears. This is called a datatip, which is like a tooltip for data. If you have trouble getting the datatip to appear, click in the line and then move the cursor next to the variable.

6.2.5	Correcting and ending debugging
While debugging, we can change the value of a variable to see if the new value produces expected results. While the program is paused, assign a new value to the variable in the Com-mand Window, Workspace browser, or Array Editor. Then continue running and stepping through the program.

6.2.6	Ending debugging
After identifying a problem, end the debugging session. It is best to quit debug mode before editing an M-flle. Otherwise, you can get unexpected results when you run the flle. To end debugging, select Exit Debug Mode from the Debug menu.

6.2.7	Correcting an M-flle
To correct errors in an M-flle,
†	Quit debugging
†	Do not make changes to an M-flle while MATLAB is in debug mode
†	Make changes to the M-flle
†	Save the M-flle
†	Clear breakpoints
†	Run the M-flle again to be sure it produces the expected results. For details on debugging process, see MATLAB documentation.

-----------------------------------------------------------------------------------------------------------------------------------
Appendix A
Summary of commands

Table A.1: Arithmetic operators and special characters
Character	Description
+	Addition
¡	Subtraction
⁄	Multiplication (scalar and array)
=	Division (right)
^	Power or exponentiation
:	Colon; creates vectors with equally spaced elements
;	Semi-colon; suppresses display; ends row in array
,	Comma; separates array subscripts
. . .	Continuation of lines
%	Percent; denotes a comment; specifles output format
0	Single quote; creates string; specifles matrix transpose
=	Assignment operator
( )	Parentheses; encloses elements of arrays and input arguments
[ ]	Brackets; encloses matrix elements and output arguments
	
Table A.2: Array operators
Character	Description
:⁄	Array multiplication
:=	Array (right) division
.^	Array power
:n	Array (left) division
:0	Array (nonconjugated) transpose

Table A.3: Relational and logical operators
Character	Description
<	Less than
•	Less than or equal to
>	Greater than
‚	Greater than or equal to
==	Equal to
»=	Not equal to
&	Logical or element-wise AND
j	Logical or element-wise OR
&&	Short-circuit AND
j j	Short-circuit OR

Table A.4: Managing workspace and flle commands
Command	Description
cd	Change current directory
clc	Clear the Command Window
clear (all)	Removes all variables from the workspace
clear x	Remove x from the workspace
copyfile	Copy flle or directory
delete	Delete flles
dir	Display directory listing
exist	Check if variables or functions are deflned
help	Display help for MATLAB functions
lookfor	Search for specifled word in all help entries
mkdir	Make new directory
movefile	Move flle or directory
pwd	Identify current directory
rmdir	Remove directory
type	Display contents of flle
what	List MATLAB flles in current directory
which	Locate functions and flles
who	Display variables currently in the workspace
whos	Display information on variables in the workspace
	
Table A.5: Predeflned variables and math constants
Variable	Description
ans	Value of last variable (answer)
eps	Floating-point relative accuracy
i	Imaginary unit of a complex number
Inf	Inflnity (1)
eps	Floating-point relative accuracy
j	Imaginary unit of a complex number
NaN	Not a number
pi	The number … (3:14159 : : :)
	
Table A.6: Elementary matrices and arrays
Command	Description
eye	Identity matrix
linspace	Generate linearly space vectors
ones	Create array of all ones
rand	Uniformly distributed random numbers and arrays
zeros	Create array of all zeros
				
Table A.7: Arrays and Matrices: Basic information
  Command	Description	
	disp	Display text or array	
	isempty	Determine if input is empty matrix	
	isequal	Test arrays for equality	
	length	Length of vector	
	ndims	Number of dimensions	
	numel	Number of elements	
	size	Size of matrix	
				
Table A.8: Arrays and Matrices: operations and manipulation
Command	Description
cross	Vector cross product
diag	Diagonal matrices and diagonals of matrix
dot	Vector dot product
end	Indicate last index of array
find	Find indices of nonzero elements
kron	Kronecker tensor product
max	Maximum value of array
min	Minimum value of array
prod	Product of array elements
reshape	Reshape array
sort	Sort array elements
sum	Sum of array elements
size	Size of matrix
	
Table A.9: Arrays and Matrices: matrix analysis and linear equations
Command	Description
cond	Condition number with respect to inversion
det	Determinant
inv	Matrix inverse
linsolve	Solve linear system of equations
lu	LU factorization
norm	Matrix or vector norm
null	Null space
orth	Orthogonalization
rank	Matrix rank
rref	Reduced row echelon form
trace	Sum of diagonal elements
