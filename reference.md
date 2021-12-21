# cplx.js reference

## class Complex

### Constructor

#### constructor(re[, im])
Generate complex number in cartesian form
<sup>[note](https://en.wikipedia.org/wiki/Complex_number#Cartesian_complex_plane)</sup> (if the imaginary part equals zero, you may leave it out.)
```javascript
z = new Complex(1, 2); // 1+2j
```
|name|type|required|
|:---:|:---:|:---:|
|re|number|O|
|im|number|X|

#### constructor(arg, abs, polarTag)
Generate complex number in polar form
<sup>[note](https://en.wikipedia.org/wiki/Complex_number#Polar_complex_plane)</sup>
```javascript
z = new Complex(Math.PI, 2, 'polar'); // 2exp(jπ) = -2
```
|name|type|required|
|:---:|:---:|:---:|
|arg|number|O|
|abs|number|O|
|polar|string|O|

#### constructor(str)
Parse string
```javascript
z = new Complex('1+3j'); // 1+3j
z = new Complex('-7j'); // -7j
z = new Complex('-6-1j'); // -6-1j
```
|name|type|required|
|:---:|:---:|:---:|
|str|string|O|

#### constructor(cplx)
Copy a complex that has already been declared
```javascript
z = new Complex(z);
```
|name|type|required|
|:---:|:---:|:---:|
|cplx|Complex|O|

### Properties
#### number re
Real part
```javascript
z.re;
```

#### number im
Imaginary part
```javascript
z.im;
```

#### number abs
Absolute value (Modulus)
<sup>[note](https://en.wikipedia.org/wiki/Complex_number#Modulus_and_argument)</sup>
```javascript
z.abs;
```

#### number arg
Argument
<sup>[note](https://en.wikipedia.org/wiki/Complex_number#Modulus_and_argument)</sup>
```javascript
z.arg;
```

### Constants

#### Complex EPSILON
```javascript
Complex.EPSILON := new Complex(Number.EPSILON)
```

#### Complex PI
Pi
```javascript
Complex.PI := new Complex(Math.PI)
```

#### Complex E
Base of the natural logarithm
```javascript
Complex.E := new Complex(Math.E)
```

#### Complex ONE
1
```javascript
Complex.ONE := new Complex(1)
```

#### Complex UNIT
Imaginary unit
```javascript
Complex.UNIT := new Complex(0, 1)
```

### String Representation

#### string toString()
String representation
```javascript
z.toString()
```

### Equivalence

#### boolean equiv(z)
Equivalence
```javascript
w.equiv(z)
```

|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

### Basic 4 Operations
```javascript
let p = new Complex(1, 2);
let q = new Complex(3, -4);
```
#### Complex add(z)
Addition
<sup>[note](https://en.wikipedia.org/wiki/Complex_number#Addition_and_subtraction)</sup>
```javascript
p.add(q); // 4-2j
p.add(6); // 7+2j
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex sub(z)
Subtraction
<sup>[note](https://en.wikipedia.org/wiki/Complex_number#Addition_and_subtraction)</sup>
```javascript
p.sub(q); // -2+6j
p.sub(6); // -5+2j
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex mul(z)
Multiplication
<sup>[note1](https://en.wikipedia.org/wiki/Complex_number#Multiplication_and_square)</sup>
<sup>[note2](https://en.wikipedia.org/wiki/Complex_number#Multiplication_and_division_in_polar_form)</sup>
```javascript
p.mul(q); // 11+2j
p.mul(6); // 6+12j
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex div(z)
Division
<sup>[note1](https://en.wikipedia.org/wiki/Complex_number#Reciprocal_and_division)</sup>
<sup>[note2](https://en.wikipedia.org/wiki/Complex_number#Multiplication_and_division_in_polar_form)</sup>
```javascript
p.div(q); // -0.2+0.4j
p.div(4); // 0.25+0.5j
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

### Exponentiation

#### Complex inv(z)
Exponentiation
<sup>[note](https://en.wikipedia.org/wiki/Complex_number#Exponentiation)</sup>
```javascript
p.inv(q); // 932.1391946432212+95.9465336603415j
p.inv(6); // 117+44j
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

## class Cxmath (Mathematical Functions)

### Advanced Operations

#### Complex static opp(z)
Opposite number (Additive inverse)<sup>[note](https://en.wikipedia.org/wiki/Additive_inverse)</sup>
```javascript
Cxmath.opp(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex static con(z)
Complex conjugate
<sup>[note](https://en.wikipedia.org/wiki/Complex_conjugate)</sup>
```javascript
Cxmath.con(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex static rec(z)
Reciprocal
```javascript
Cxmath.rec(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

### [Radical Roots](https://en.wikipedia.org/wiki/Square_root#Square_roots_of_negative_and_complex_numbers)

#### Complex static sqrt(z)
Principal square root
<sup>[note](https://en.wikipedia.org/wiki/Complex_number#Square_root)</sup>
```javascript
Cxmath.sqrt(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex static cbrt(z)
Principal cube root
```javascript
Cxmath.cbrt(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

### Exponential Function & Logarithm

#### Complex static exp(z)
Exponential function
<sup>[note1](https://en.wikipedia.org/wiki/Exponential_function)</sup>
<sup>[note2](https://en.wikipedia.org/wiki/Complex_number#Exponentiation)</sup>
```javascript
Cxmath.exp(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex static log(a[, b=Math.E])
Logarithm
<sup>[note1](https://en.wikipedia.org/wiki/Logarithm)</sup>
<sup>[note2](https://en.wikipedia.org/wiki/Complex_number#Complex_logarithm)</sup>
defined in principal branch
<sup>[note1](https://en.wikipedia.org/wiki/Principal_branch)</sup>
<sup>[note2](https://en.wikipedia.org/wiki/Branch_point#Branch_cuts)</sup>
with base b and antilogarithm a (if the base equals e, you may leave it out.)
```javascript
Cxmath.log(a); // Natural Logarithm
Cxmath.log(a, 2); // Binary Logarithm
Cxmath.log(a, 10); // Decimal Logarithm
Cxmath.log(a, b);
```

> Parameters

|name|type|required|
|:---:|:---:|:---:|
|a|number/Complex|O|
|b|numner/Complex|X|

### [Trigonometric Functions](https://en.wikipedia.org/wiki/Trigonometric_functions)

#### Common Trigonometric Functions (static)

```javascript
Cxmath.sin(z);
Cxmath.cos(z);
Cxmath.tan(z);

Cxmath.csc(z);
Cxmath.sec(z);
Cxmath.cot(z);
```

> Functions

|name|description|return type|
|:---:|:---:|:---:|
|sin|Sine|Complex|
|cos|Cosine|Complex|
|tan|Tangent|Complex|
|csc|Cosecant|Complex|
|sec|Secant|Complex|
|cot|Cotangent|Complex|

> Parameters

|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

### [Inverse Trigonometric Functions](https://en.wikipedia.org/wiki/Inverse_trigonometric_functions)

#### Common Inverse Trigonometric Functions (static)

```javascript
Cxmath.asin(z);
Cxmath.acos(z);
Cxmath.atan(z);

Cxmath.acsc(z);
Cxmath.asec(z);
Cxmath.acot(z);
```

> Functions

|name|description|return type|
|:---:|:---:|:---:|
|asin|Arcsine|Complex|
|acos|Arccosine|Complex|
|atan|Arctangent|Complex|
|acsc|Arccosecant|Complex|
|asec|Arcsecant|Complex|
|acot|Arccotangent|Complex|

> Parameters

|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### Complex static atan2(w, z)
2-argument-arctangent
<sup>[Note](https://en.m.wikipedia.org/wiki/Atan2)</sup>
```javascript
Cxmath.atan2(w, z);
```
|name|type|required|
|:---:|:---:|:---:|
|w|number/Complex|O|
|z|number/Complex|O|

### [Hyperbolic Functions](https://en.wikipedia.org/wiki/Hyperbolic_functions)

#### Common Hyperbolic Functions (static)

```javascript
Cxmath.sinh(z);
Cxmath.cosh(z);
Cxmath.tanh(z);
```

> Functions

|name|description|return type|
|:---:|:---:|:---:|
|sinh|Hyperbolic-sine|Complex|
|cosh|Hyperbolic-cosine|Complex|
|tanh|Hyperbolic-tangent|Complex|

> Parameters

|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

### [Inverse(Area-) Hyperbolic Functions](https://en.wikipedia.org/wiki/Inverse_hyperbolic_functions)

#### Common Inverse Hyperbolic Functions (static)

```javascript
Cxmath.asinh(z);
Cxmath.acosh(z);
Cxmath.atanh(z);
```

> Functions

|name|description|return type|
|:---:|:---:|:---:|
|asinh|Inverse-hyperbolic-sine|Complex|
|acosh|Inverse-hyperbolic-cosine|Complex|
|atanh|Inverse-hyperbolic-tangent|Complex|

> Parameters

|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

### Sign Function

#### number static csgn(z)
Complex sign function
<sup>[note](https://en.wikipedia.org/wiki/Sign_function#Complex_signum)</sup>
```javascript
Cxmath.csgn(z);
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

### Vector

#### number static norm(z)
Norm
```javascript
Cxmath.norm(z) := z.abs()
```
|name|type|required|
|:---:|:---:|:---:|
|z|number/Complex|O|

#### number static inp(a, b)
Inner Product
```javascript
Cxmath.inp(a, b);
```
|name|type|required|
|:---:|:---:|:---:|
|a|number/Complex|O|
|b|number/Complex|O|

#### number static dist(a, b)
Distance from point a to point b
```javascript
Cxmath.dist(a, b);
```
|name|type|required|
|:---:|:---:|:---:|
|a|number/Complex|O|
|b|number/omplex|O|

### Random

#### Complex static random()
Random complex (both real part and imaginary part are more than or equal to 0 and less than 1)
```javascript
Cxmath.random();
```