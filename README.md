<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# Assert

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Assertion utilities.

<section class="installation">

## Installation

```bash
npm install @hishprorg/placeat-iste
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm`][esm-url] branch (see [README][esm-readme]).
-   If you are using Deno, visit the [`deno`][deno-url] branch (see [README][deno-readme] for usage intructions).
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd`][umd-url] branch (see [README][umd-readme]).

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

To view installation and usage instructions specific to each branch build, be sure to explicitly navigate to the respective README files on each branch, as linked to above.

</section>

<section class="usage">

## Usage

```javascript
var assert = require( '@hishprorg/placeat-iste' );
```

#### assert

Namespace providing utilities for data type testing and feature detection.

```javascript
var o = assert;
// returns {...}
```

To validate the built-in JavaScript data types, the namespace includes the following assertion utilities:

<!-- <toc pattern="is-+(array|boolean|date-object|function|string|symbol|nan|null|number|object|regexp|symbol|undefined)" > -->

<div class="namespace-toc">

-   <span class="signature">[`isArray( value )`][@hishprorg/placeat-iste/is-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array.</span>
-   <span class="signature">[`isBoolean( value )`][@hishprorg/placeat-iste/is-boolean]</span><span class="delimiter">: </span><span class="description">test if a value is a boolean.</span>
-   <span class="signature">[`isDateObject( value )`][@hishprorg/placeat-iste/is-date-object]</span><span class="delimiter">: </span><span class="description">test if a value is a Date object.</span>
-   <span class="signature">[`isFunction( value )`][@hishprorg/placeat-iste/is-function]</span><span class="delimiter">: </span><span class="description">test if a value is a function.</span>
-   <span class="signature">[`isnan( value )`][@hishprorg/placeat-iste/is-nan]</span><span class="delimiter">: </span><span class="description">test if a value is NaN.</span>
-   <span class="signature">[`isNull( value )`][@hishprorg/placeat-iste/is-null]</span><span class="delimiter">: </span><span class="description">test if a value is null.</span>
-   <span class="signature">[`isNumber( value )`][@hishprorg/placeat-iste/is-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number.</span>
-   <span class="signature">[`isObject( value )`][@hishprorg/placeat-iste/is-object]</span><span class="delimiter">: </span><span class="description">test if a value is an object.</span>
-   <span class="signature">[`isRegExp( value )`][@hishprorg/placeat-iste/is-regexp]</span><span class="delimiter">: </span><span class="description">test if a value is a regular expression.</span>
-   <span class="signature">[`isString( value )`][@hishprorg/placeat-iste/is-string]</span><span class="delimiter">: </span><span class="description">test if a value is a string.</span>
-   <span class="signature">[`isSymbol( value )`][@hishprorg/placeat-iste/is-symbol]</span><span class="delimiter">: </span><span class="description">test if a value is a symbol.</span>
-   <span class="signature">[`isUndefined( value )`][@hishprorg/placeat-iste/is-undefined]</span><span class="delimiter">: </span><span class="description">test if a value is undefined.</span>

</div>

<!-- </toc> -->

For primitive types having corresponding object wrappers, assertion utilities provide `isObject` and `isPrimitive` methods to test for either objects or primitives, respectively.

<!-- eslint-disable no-new-wrappers -->

```javascript
var Boolean = require( '@stdlib/boolean/ctor' );
var isBoolean = require( '@hishprorg/placeat-iste/is-boolean' );

var bool = isBoolean.isObject( new Boolean( false ) );
// returns true

bool = isBoolean.isObject( false );
// returns false

bool = isBoolean.isPrimitive( false );
// returns true
```

Many of the assertion utilities have corresponding packages that test whether array elements are of the given data type:

<!-- <toc pattern="is-+(array|boolean|date-object|function|string|nan|number|object|regexp|symbol|null|undefined)-array" > -->

<div class="namespace-toc">

-   <span class="signature">[`isArrayArray( value )`][@hishprorg/placeat-iste/is-array-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array of arrays.</span>
-   <span class="signature">[`isBooleanArray( value )`][@hishprorg/placeat-iste/is-boolean-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object of booleans.</span>
-   <span class="signature">[`isDateObjectArray( value )`][@hishprorg/placeat-iste/is-date-object-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only Date objects.</span>
-   <span class="signature">[`isFunctionArray( value )`][@hishprorg/placeat-iste/is-function-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only functions.</span>
-   <span class="signature">[`isNaNArray( value )`][@hishprorg/placeat-iste/is-nan-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only NaN values.</span>
-   <span class="signature">[`isNullArray( value )`][@hishprorg/placeat-iste/is-null-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only null values.</span>
-   <span class="signature">[`isNumberArray( value )`][@hishprorg/placeat-iste/is-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object of numbers.</span>
-   <span class="signature">[`isObjectArray( value )`][@hishprorg/placeat-iste/is-object-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only objects.</span>
-   <span class="signature">[`isStringArray( value )`][@hishprorg/placeat-iste/is-string-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array of strings.</span>
-   <span class="signature">[`isSymbolArray( value )`][@hishprorg/placeat-iste/is-symbol-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only symbols.</span>

</div>

<!-- </toc> -->

Where applicable, similar to the assertion utilities for built-in data types, array assertion utilities provides methods for testing for an array of primitives or objects.

<!-- eslint-disable no-new-wrappers -->

```javascript
var isStringArray = require( '@hishprorg/placeat-iste/is-string-array' );

var bool = isStringArray( [ 'hello', 'world' ] );
// returns true

bool = isStringArray.primitives( [ 'hello', 'world' ] );
// returns true

bool = isStringArray.objects( [ 'hello', 'world' ] );
// returns false

bool = isStringArray.objects( [ new String( 'hello' ), new String( 'world' ) ] );
// returns true
```

The namespace also contains utilities to test for numbers within a certain range or for numbers satisfying a particular "type":

<!-- <toc pattern="is-*+(number|integer)*" ignore="is-number-array" ignore="is-number" > -->

<div class="namespace-toc">

-   <span class="signature">[`isCubeNumber( value )`][@hishprorg/placeat-iste/is-cube-number]</span><span class="delimiter">: </span><span class="description">test if a value is a cube number.</span>
-   <span class="signature">[`isIntegerArray( value )`][@hishprorg/placeat-iste/is-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only integers.</span>
-   <span class="signature">[`isInteger( value )`][@hishprorg/placeat-iste/is-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having an integer value.</span>
-   <span class="signature">[`isNegativeIntegerArray( value )`][@hishprorg/placeat-iste/is-negative-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only negative integers.</span>
-   <span class="signature">[`isNegativeInteger( value )`][@hishprorg/placeat-iste/is-negative-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a negative integer value.</span>
-   <span class="signature">[`isNegativeNumberArray( value )`][@hishprorg/placeat-iste/is-negative-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only negative numbers.</span>
-   <span class="signature">[`isNegativeNumber( value )`][@hishprorg/placeat-iste/is-negative-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a negative value.</span>
-   <span class="signature">[`isNonNegativeIntegerArray( value )`][@hishprorg/placeat-iste/is-nonnegative-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonnegative integers.</span>
-   <span class="signature">[`isNonNegativeInteger( value )`][@hishprorg/placeat-iste/is-nonnegative-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonnegative integer value.</span>
-   <span class="signature">[`isNonNegativeNumberArray( value )`][@hishprorg/placeat-iste/is-nonnegative-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonnegative numbers.</span>
-   <span class="signature">[`isNonNegativeNumber( value )`][@hishprorg/placeat-iste/is-nonnegative-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonnegative value.</span>
-   <span class="signature">[`isNonPositiveIntegerArray( value )`][@hishprorg/placeat-iste/is-nonpositive-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonpositive integers.</span>
-   <span class="signature">[`isNonPositiveInteger( value )`][@hishprorg/placeat-iste/is-nonpositive-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonpositive integer value.</span>
-   <span class="signature">[`isNonPositiveNumberArray( value )`][@hishprorg/placeat-iste/is-nonpositive-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonpositive numbers.</span>
-   <span class="signature">[`isNonPositiveNumber( value )`][@hishprorg/placeat-iste/is-nonpositive-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonpositive value.</span>
-   <span class="signature">[`isPositiveIntegerArray( value )`][@hishprorg/placeat-iste/is-positive-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only positive integers.</span>
-   <span class="signature">[`isPositiveInteger( value )`][@hishprorg/placeat-iste/is-positive-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a positive integer value.</span>
-   <span class="signature">[`isPositiveNumberArray( value )`][@hishprorg/placeat-iste/is-positive-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only positive numbers.</span>
-   <span class="signature">[`isPositiveNumber( value )`][@hishprorg/placeat-iste/is-positive-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a positive value.</span>
-   <span class="signature">[`isSafeIntegerArray( value )`][@hishprorg/placeat-iste/is-safe-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only safe integers.</span>
-   <span class="signature">[`isSafeInteger( value )`][@hishprorg/placeat-iste/is-safe-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a safe integer value.</span>
-   <span class="signature">[`isSquareNumber( value )`][@hishprorg/placeat-iste/is-square-number]</span><span class="delimiter">: </span><span class="description">test if a value is a square number.</span>
-   <span class="signature">[`isSquareTriangularNumber( value )`][@hishprorg/placeat-iste/is-square-triangular-number]</span><span class="delimiter">: </span><span class="description">test if a value is a square triangular number.</span>
-   <span class="signature">[`isTriangularNumber( value )`][@hishprorg/placeat-iste/is-triangular-number]</span><span class="delimiter">: </span><span class="description">test if a value is a triangular number.</span>

</div>

<!-- </toc> -->

The namespace provides utilities for validating typed arrays:

<!-- <toc pattern="is-+(int8|int16|int32|uint8clamped|uint8|uint16|uint32|float32|float64)array"> -->

<div class="namespace-toc">

-   <span class="signature">[`isFloat32Array( value )`][@hishprorg/placeat-iste/is-float32array]</span><span class="delimiter">: </span><span class="description">test if a value is a Float32Array.</span>
-   <span class="signature">[`isFloat64Array( value )`][@hishprorg/placeat-iste/is-float64array]</span><span class="delimiter">: </span><span class="description">test if a value is a Float64Array.</span>
-   <span class="signature">[`isInt16Array( value )`][@hishprorg/placeat-iste/is-int16array]</span><span class="delimiter">: </span><span class="description">test if a value is an Int16Array.</span>
-   <span class="signature">[`isInt32Array( value )`][@hishprorg/placeat-iste/is-int32array]</span><span class="delimiter">: </span><span class="description">test if a value is an Int32Array.</span>
-   <span class="signature">[`isInt8Array( value )`][@hishprorg/placeat-iste/is-int8array]</span><span class="delimiter">: </span><span class="description">test if a value is an Int8Array.</span>
-   <span class="signature">[`isUint16Array( value )`][@hishprorg/placeat-iste/is-uint16array]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint16Array.</span>
-   <span class="signature">[`isUint32Array( value )`][@hishprorg/placeat-iste/is-uint32array]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint32Array.</span>
-   <span class="signature">[`isUint8Array( value )`][@hishprorg/placeat-iste/is-uint8array]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint8Array.</span>
-   <span class="signature">[`isUint8ClampedArray( value )`][@hishprorg/placeat-iste/is-uint8clampedarray]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint8ClampedArray.</span>

</div>

<!-- </toc> -->

The namespace includes utilities for validating `ndarray`s (n-dimensional arrays).

<!-- <toc keywords="+ndarray" > -->

<div class="namespace-toc">

-   <span class="signature">[`isCentrosymmetricMatrix( value )`][@hishprorg/placeat-iste/is-centrosymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a centrosymmetric matrix.</span>
-   <span class="signature">[`isComplex128MatrixLike( value )`][@hishprorg/placeat-iste/is-complex128matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing double-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex128ndarrayLike( value )`][@hishprorg/placeat-iste/is-complex128ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing double-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex128VectorLike( value )`][@hishprorg/placeat-iste/is-complex128vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing double-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex64MatrixLike( value )`][@hishprorg/placeat-iste/is-complex64matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing single-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex64ndarrayLike( value )`][@hishprorg/placeat-iste/is-complex64ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing single-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex64VectorLike( value )`][@hishprorg/placeat-iste/is-complex64vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing single-precision complex floating-point numbers.</span>
-   <span class="signature">[`isFloat32MatrixLike( value )`][@hishprorg/placeat-iste/is-float32matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing single-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat32ndarrayLike( value )`][@hishprorg/placeat-iste/is-float32ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing single-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat32VectorLike( value )`][@hishprorg/placeat-iste/is-float32vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing single-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat64MatrixLike( value )`][@hishprorg/placeat-iste/is-float64matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing double-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat64ndarrayLike( value )`][@hishprorg/placeat-iste/is-float64ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing double-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat64VectorLike( value )`][@hishprorg/placeat-iste/is-float64vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing double-precision floating-point numbers.</span>
-   <span class="signature">[`isMatrixLike( value )`][@hishprorg/placeat-iste/is-matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is 2-dimensional ndarray-like object.</span>
-   <span class="signature">[`isndarrayLike( value )`][@hishprorg/placeat-iste/is-ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is ndarray-like.</span>
-   <span class="signature">[`isNonSymmetricMatrix( value )`][@hishprorg/placeat-iste/is-nonsymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a non-symmetric matrix.</span>
-   <span class="signature">[`isPersymmetricMatrix( value )`][@hishprorg/placeat-iste/is-persymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a persymmetric matrix.</span>
-   <span class="signature">[`isSkewCentrosymmetricMatrix( value )`][@hishprorg/placeat-iste/is-skew-centrosymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a skew-centrosymmetric matrix.</span>
-   <span class="signature">[`isSkewPersymmetricMatrix( value )`][@hishprorg/placeat-iste/is-skew-persymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a skew-persymmetric matrix.</span>
-   <span class="signature">[`isSkewSymmetricMatrix( value )`][@hishprorg/placeat-iste/is-skew-symmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a skew-symmetric matrix.</span>
-   <span class="signature">[`isSquareMatrix( value )`][@hishprorg/placeat-iste/is-square-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object having equal dimensions.</span>
-   <span class="signature">[`isSymmetricMatrix( value )`][@hishprorg/placeat-iste/is-symmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a symmetric matrix.</span>
-   <span class="signature">[`isVectorLike( value )`][@hishprorg/placeat-iste/is-vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object.</span>

</div>

<!-- </toc> -->

The namespace includes utilities for validating complex numbers and arrays of complex numbers:

<!-- <toc pattern="is-complex*" > -->

<div class="namespace-toc">

-   <span class="signature">[`isComplexLike( value )`][@hishprorg/placeat-iste/is-complex-like]</span><span class="delimiter">: </span><span class="description">test if a value is a complex number-like object.</span>
-   <span class="signature">[`isComplexTypedArrayLike( value )`][@hishprorg/placeat-iste/is-complex-typed-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is complex-typed-array-like.</span>
-   <span class="signature">[`isComplexTypedArray( value )`][@hishprorg/placeat-iste/is-complex-typed-array]</span><span class="delimiter">: </span><span class="description">test if a value is a complex typed array.</span>
-   <span class="signature">[`isComplex( value )`][@hishprorg/placeat-iste/is-complex]</span><span class="delimiter">: </span><span class="description">test if a value is a 64-bit or 128-bit complex number.</span>
-   <span class="signature">[`isComplex128( value )`][@hishprorg/placeat-iste/is-complex128]</span><span class="delimiter">: </span><span class="description">test if a value is a 128-bit complex number.</span>
-   <span class="signature">[`isComplex128Array( value )`][@hishprorg/placeat-iste/is-complex128array]</span><span class="delimiter">: </span><span class="description">test if a value is a Complex128Array.</span>
-   <span class="signature">[`isComplex64( value )`][@hishprorg/placeat-iste/is-complex64]</span><span class="delimiter">: </span><span class="description">test if a value is a 64-bit complex number.</span>
-   <span class="signature">[`isComplex64Array( value )`][@hishprorg/placeat-iste/is-complex64array]</span><span class="delimiter">: </span><span class="description">test if a value is a Complex64Array.</span>

</div>

<!-- </toc> -->

The namespace includes utilities for validating other special arrays or buffers:

<!-- <toc pattern="is-*array*" ignore="is-+(int8|int16|int32|uint8clamped|uint8|uint16|uint32|float32|float64)array" ignore="is-*+(number|integer)*" ignore="is-+(array|boolean|date-object|function|string|nan|number|object|primitive|regexp|symbol|null|undefined)-array" ignore="is-array" keywords="-ndarray" > -->

<div class="namespace-toc">

-   <span class="signature">[`isAccessorArray( value )`][@hishprorg/placeat-iste/is-accessor-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object supporting the accessor (get/set) protocol.</span>
-   <span class="signature">[`isArrayLength( value )`][@hishprorg/placeat-iste/is-array-length]</span><span class="delimiter">: </span><span class="description">test if a value is a valid array length.</span>
-   <span class="signature">[`isArrayLikeObject( value )`][@hishprorg/placeat-iste/is-array-like-object]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object.</span>
-   <span class="signature">[`isArrayLike( value )`][@hishprorg/placeat-iste/is-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is array-like.</span>
-   <span class="signature">[`isArrayBufferView( value )`][@hishprorg/placeat-iste/is-arraybuffer-view]</span><span class="delimiter">: </span><span class="description">test if a value is an ArrayBuffer view.</span>
-   <span class="signature">[`isArrayBuffer( value )`][@hishprorg/placeat-iste/is-arraybuffer]</span><span class="delimiter">: </span><span class="description">test if a value is an ArrayBuffer.</span>
-   <span class="signature">[`isBetweenArray( value, a, b[, left, right] )`][@hishprorg/placeat-iste/is-between-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object where every element is between two values.</span>
-   <span class="signature">[`isBigInt64Array( value )`][@hishprorg/placeat-iste/is-bigint64array]</span><span class="delimiter">: </span><span class="description">test if a value is a BigInt64Array.</span>
-   <span class="signature">[`isBigUint64Array( value )`][@hishprorg/placeat-iste/is-biguint64array]</span><span class="delimiter">: </span><span class="description">test if a value is a BigUint64Array.</span>
-   <span class="signature">[`isCircularArray( value )`][@hishprorg/placeat-iste/is-circular-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array containing a circular reference.</span>
-   <span class="signature">[`isEmptyArrayLikeObject( value )`][@hishprorg/placeat-iste/is-empty-array-like-object]</span><span class="delimiter">: </span><span class="description">test if a value is an empty array-like object.</span>
-   <span class="signature">[`isEmptyArray( value )`][@hishprorg/placeat-iste/is-empty-array]</span><span class="delimiter">: </span><span class="description">test if a value is an empty array.</span>
-   <span class="signature">[`isFalsyArray( value )`][@hishprorg/placeat-iste/is-falsy-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only falsy values.</span>
-   <span class="signature">[`isFiniteArray( value )`][@hishprorg/placeat-iste/is-finite-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only finite numbers.</span>
-   <span class="signature">[`isNumericArray( value )`][@hishprorg/placeat-iste/is-numeric-array]</span><span class="delimiter">: </span><span class="description">test if a value is a numeric array.</span>
-   <span class="signature">[`isPlainObjectArray( value )`][@hishprorg/placeat-iste/is-plain-object-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only plain objects.</span>
-   <span class="signature">[`isProbabilityArray( value )`][@hishprorg/placeat-iste/is-probability-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only probabilities.</span>
-   <span class="signature">[`isSameArray( v1, v2 )`][@hishprorg/placeat-iste/is-same-array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both generic arrays and have the same values.</span>
-   <span class="signature">[`isSameComplex128Array( v1, v2 )`][@hishprorg/placeat-iste/is-same-complex128array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Complex128Arrays and have the same values.</span>
-   <span class="signature">[`isSameComplex64Array( v1, v2 )`][@hishprorg/placeat-iste/is-same-complex64array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Complex64Arrays and have the same values.</span>
-   <span class="signature">[`isSameFloat32Array( v1, v2 )`][@hishprorg/placeat-iste/is-same-float32array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Float32Arrays and have the same values.</span>
-   <span class="signature">[`isSameFloat64Array( v1, v2 )`][@hishprorg/placeat-iste/is-same-float64array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Float64Arrays and have the same values.</span>
-   <span class="signature">[`isSharedArrayBuffer( value )`][@hishprorg/placeat-iste/is-sharedarraybuffer]</span><span class="delimiter">: </span><span class="description">test if a value is a SharedArrayBuffer.</span>
-   <span class="signature">[`isTruthyArray( value )`][@hishprorg/placeat-iste/is-truthy-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only truthy values.</span>
-   <span class="signature">[`isTypedArrayLength( value )`][@hishprorg/placeat-iste/is-typed-array-length]</span><span class="delimiter">: </span><span class="description">test if a value is a valid typed array length.</span>
-   <span class="signature">[`isTypedArrayLike( value )`][@hishprorg/placeat-iste/is-typed-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is typed-array-like.</span>
-   <span class="signature">[`isTypedArray( value )`][@hishprorg/placeat-iste/is-typed-array]</span><span class="delimiter">: </span><span class="description">test if a value is a typed array.</span>
-   <span class="signature">[`isUnityProbabilityArray( value )`][@hishprorg/placeat-iste/is-unity-probability-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array of probabilities that sum to one.</span>

</div>

<!-- </toc> -->

To test for error objects, the namespace includes the following utilities:

<!-- <toc pattern="is-*error*" > -->

<div class="namespace-toc">

-   <span class="signature">[`isError( value )`][@hishprorg/placeat-iste/is-error]</span><span class="delimiter">: </span><span class="description">test if a value is an Error object.</span>
-   <span class="signature">[`isEvalError( value )`][@hishprorg/placeat-iste/is-eval-error]</span><span class="delimiter">: </span><span class="description">test if a value is an EvalError object.</span>
-   <span class="signature">[`isRangeError( value )`][@hishprorg/placeat-iste/is-range-error]</span><span class="delimiter">: </span><span class="description">test if a value is a RangeError object.</span>
-   <span class="signature">[`isReferenceError( value )`][@hishprorg/placeat-iste/is-reference-error]</span><span class="delimiter">: </span><span class="description">test if a value is a ReferenceError object.</span>
-   <span class="signature">[`isSyntaxError( value )`][@hishprorg/placeat-iste/is-syntax-error]</span><span class="delimiter">: </span><span class="description">test if a value is a SyntaxError object.</span>
-   <span class="signature">[`isTypeError( value )`][@hishprorg/placeat-iste/is-type-error]</span><span class="delimiter">: </span><span class="description">test if a value is a TypeError object.</span>
-   <span class="signature">[`isURIError( value )`][@hishprorg/placeat-iste/is-uri-error]</span><span class="delimiter">: </span><span class="description">test if a value is a URIError object.</span>

</div>

<!-- </toc> -->

The namespace exposes the following constants concerning the current running process:

<!-- <toc pattern="is-+(browser|darwin|electron|electron-main|electron-renderer|little-endian|big-endian|node|web-worker|windows|docker|mobile|touch-device)" > -->

<div class="namespace-toc">

-   <span class="signature">[`IS_BIG_ENDIAN`][@hishprorg/placeat-iste/is-big-endian]</span><span class="delimiter">: </span><span class="description">check if an environment is big endian.</span>
-   <span class="signature">[`IS_BROWSER`][@hishprorg/placeat-iste/is-browser]</span><span class="delimiter">: </span><span class="description">check if the runtime is a web browser.</span>
-   <span class="signature">[`IS_DARWIN`][@hishprorg/placeat-iste/is-darwin]</span><span class="delimiter">: </span><span class="description">boolean indicating if the current process is running on Darwin.</span>
-   <span class="signature">[`IS_DOCKER`][@hishprorg/placeat-iste/is-docker]</span><span class="delimiter">: </span><span class="description">check if the process is running in a Docker container.</span>
-   <span class="signature">[`IS_ELECTRON_MAIN`][@hishprorg/placeat-iste/is-electron-main]</span><span class="delimiter">: </span><span class="description">check if the runtime is the main Electron process.</span>
-   <span class="signature">[`IS_ELECTRON_RENDERER`][@hishprorg/placeat-iste/is-electron-renderer]</span><span class="delimiter">: </span><span class="description">check if the runtime is the Electron renderer process.</span>
-   <span class="signature">[`IS_ELECTRON`][@hishprorg/placeat-iste/is-electron]</span><span class="delimiter">: </span><span class="description">check if the runtime is Electron.</span>
-   <span class="signature">[`IS_LITTLE_ENDIAN`][@hishprorg/placeat-iste/is-little-endian]</span><span class="delimiter">: </span><span class="description">check if an environment is little endian.</span>
-   <span class="signature">[`IS_MOBILE`][@hishprorg/placeat-iste/is-mobile]</span><span class="delimiter">: </span><span class="description">check if the current environment is a mobile device.</span>
-   <span class="signature">[`IS_NODE`][@hishprorg/placeat-iste/is-node]</span><span class="delimiter">: </span><span class="description">check if the runtime is Node.js.</span>
-   <span class="signature">[`IS_TOUCH_DEVICE`][@hishprorg/placeat-iste/is-touch-device]</span><span class="delimiter">: </span><span class="description">check if the current environment is a touch device.</span>
-   <span class="signature">[`IS_WEB_WORKER`][@hishprorg/placeat-iste/is-web-worker]</span><span class="delimiter">: </span><span class="description">check if the runtime is a web worker.</span>
-   <span class="signature">[`IS_WINDOWS`][@hishprorg/placeat-iste/is-windows]</span><span class="delimiter">: </span><span class="description">boolean indicating if the current process is running on Windows.</span>

</div>

<!-- </toc> -->

To test whether a runtime environment supports certain features, the namespace includes the following utilities:

<!-- <toc pattern="has-*-support" > -->

<div class="namespace-toc">

-   <span class="signature">[`hasArrayBufferSupport()`][@hishprorg/placeat-iste/has-arraybuffer-support]</span><span class="delimiter">: </span><span class="description">detect native `ArrayBuffer` support.</span>
-   <span class="signature">[`hasArrowFunctionSupport()`][@hishprorg/placeat-iste/has-arrow-function-support]</span><span class="delimiter">: </span><span class="description">detect native `arrow function` support.</span>
-   <span class="signature">[`hasAsyncAwaitSupport()`][@hishprorg/placeat-iste/has-async-await-support]</span><span class="delimiter">: </span><span class="description">detect native `async`/`await` support.</span>
-   <span class="signature">[`hasAsyncIteratorSymbolSupport()`][@hishprorg/placeat-iste/has-async-iterator-symbol-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol.asyncIterator` support.</span>
-   <span class="signature">[`hasBigIntSupport()`][@hishprorg/placeat-iste/has-bigint-support]</span><span class="delimiter">: </span><span class="description">detect native `BigInt` support.</span>
-   <span class="signature">[`hasBigInt64ArraySupport()`][@hishprorg/placeat-iste/has-bigint64array-support]</span><span class="delimiter">: </span><span class="description">detect native `BigInt64Array` support.</span>
-   <span class="signature">[`hasBigUint64ArraySupport()`][@hishprorg/placeat-iste/has-biguint64array-support]</span><span class="delimiter">: </span><span class="description">detect native `BigUint64Array` support.</span>
-   <span class="signature">[`hasClassSupport()`][@hishprorg/placeat-iste/has-class-support]</span><span class="delimiter">: </span><span class="description">detect native `class` support.</span>
-   <span class="signature">[`hasDataViewSupport()`][@hishprorg/placeat-iste/has-dataview-support]</span><span class="delimiter">: </span><span class="description">detect native `DataView` support.</span>
-   <span class="signature">[`hasDefinePropertiesSupport()`][@hishprorg/placeat-iste/has-define-properties-support]</span><span class="delimiter">: </span><span class="description">detect `Object.defineProperties` support.</span>
-   <span class="signature">[`hasDefinePropertySupport()`][@hishprorg/placeat-iste/has-define-property-support]</span><span class="delimiter">: </span><span class="description">detect `Object.defineProperty` support.</span>
-   <span class="signature">[`hasFloat32ArraySupport()`][@hishprorg/placeat-iste/has-float32array-support]</span><span class="delimiter">: </span><span class="description">detect native `Float32Array` support.</span>
-   <span class="signature">[`hasFloat64ArraySupport()`][@hishprorg/placeat-iste/has-float64array-support]</span><span class="delimiter">: </span><span class="description">detect native `Float64Array` support.</span>
-   <span class="signature">[`hasFunctionNameSupport()`][@hishprorg/placeat-iste/has-function-name-support]</span><span class="delimiter">: </span><span class="description">detect native function `name` support.</span>
-   <span class="signature">[`hasGeneratorSupport()`][@hishprorg/placeat-iste/has-generator-support]</span><span class="delimiter">: </span><span class="description">detect native `generator function` support.</span>
-   <span class="signature">[`hasGlobalThisSupport()`][@hishprorg/placeat-iste/has-globalthis-support]</span><span class="delimiter">: </span><span class="description">detect `globalThis` support.</span>
-   <span class="signature">[`hasInt16ArraySupport()`][@hishprorg/placeat-iste/has-int16array-support]</span><span class="delimiter">: </span><span class="description">detect native `Int16Array` support.</span>
-   <span class="signature">[`hasInt32ArraySupport()`][@hishprorg/placeat-iste/has-int32array-support]</span><span class="delimiter">: </span><span class="description">detect native `Int32Array` support.</span>
-   <span class="signature">[`hasInt8ArraySupport()`][@hishprorg/placeat-iste/has-int8array-support]</span><span class="delimiter">: </span><span class="description">detect native `Int8Array` support.</span>
-   <span class="signature">[`hasIteratorSymbolSupport()`][@hishprorg/placeat-iste/has-iterator-symbol-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol.iterator` support.</span>
-   <span class="signature">[`hasMapSupport()`][@hishprorg/placeat-iste/has-map-support]</span><span class="delimiter">: </span><span class="description">detect native `Map` support.</span>
-   <span class="signature">[`hasNodeBufferSupport()`][@hishprorg/placeat-iste/has-node-buffer-support]</span><span class="delimiter">: </span><span class="description">detect native `Buffer` support.</span>
-   <span class="signature">[`hasProxySupport()`][@hishprorg/placeat-iste/has-proxy-support]</span><span class="delimiter">: </span><span class="description">detect native `Proxy` support.</span>
-   <span class="signature">[`hasSetSupport()`][@hishprorg/placeat-iste/has-set-support]</span><span class="delimiter">: </span><span class="description">detect native `Set` support.</span>
-   <span class="signature">[`hasSharedArrayBufferSupport()`][@hishprorg/placeat-iste/has-sharedarraybuffer-support]</span><span class="delimiter">: </span><span class="description">detect native `SharedArrayBuffer` support.</span>
-   <span class="signature">[`hasSymbolSupport()`][@hishprorg/placeat-iste/has-symbol-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol` support.</span>
-   <span class="signature">[`hasToStringTagSupport()`][@hishprorg/placeat-iste/has-tostringtag-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol.toStringTag` support.</span>
-   <span class="signature">[`hasUint16ArraySupport()`][@hishprorg/placeat-iste/has-uint16array-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint16Array` support.</span>
-   <span class="signature">[`hasUint32ArraySupport()`][@hishprorg/placeat-iste/has-uint32array-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint32Array` support.</span>
-   <span class="signature">[`hasUint8ArraySupport()`][@hishprorg/placeat-iste/has-uint8array-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint8Array` support.</span>
-   <span class="signature">[`hasUint8ClampedArraySupport()`][@hishprorg/placeat-iste/has-uint8clampedarray-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint8ClampedArray` support.</span>
-   <span class="signature">[`hasWebAssemblySupport()`][@hishprorg/placeat-iste/has-wasm-support]</span><span class="delimiter">: </span><span class="description">detect native WebAssembly support.</span>
-   <span class="signature">[`hasWeakMapSupport()`][@hishprorg/placeat-iste/has-weakmap-support]</span><span class="delimiter">: </span><span class="description">detect native `WeakMap` support.</span>
-   <span class="signature">[`hasWeakSetSupport()`][@hishprorg/placeat-iste/has-weakset-support]</span><span class="delimiter">: </span><span class="description">detect native `WeakSet` support.</span>

</div>

<!-- </toc> -->

The remaining namespace utilities are as follows:

<!-- <toc ignore="is-+(array|boolean|date-object|function|string|symbol|nan|null|number|object|regexp|symbol|undefined)" ignore="is-*+(number|integer)*" ignore="is-*array*" ignore="is-*error*" ignore="is-+(browser|darwin|electron|electron-main|electron-renderer|little-endian|node|web-worker|windows)" ignore="has-*-support" keywords="-ndarray" > -->

<div class="namespace-toc">

-   <span class="signature">[`contains( val, searchValue[, position] )`][@hishprorg/placeat-iste/contains]</span><span class="delimiter">: </span><span class="description">test if an array-like value contains a search value.</span>
-   <span class="signature">[`deepEqual( a, b )`][@hishprorg/placeat-iste/deep-equal]</span><span class="delimiter">: </span><span class="description">test for deep equality between two values.</span>
-   <span class="signature">[`deepHasOwnProp( value, path[, options] )`][@hishprorg/placeat-iste/deep-has-own-property]</span><span class="delimiter">: </span><span class="description">test whether an object contains a nested key path.</span>
-   <span class="signature">[`deepHasProp( value, path[, options] )`][@hishprorg/placeat-iste/deep-has-property]</span><span class="delimiter">: </span><span class="description">test whether an object contains a nested key path, either own or inherited.</span>
-   <span class="signature">[`hasOwnProp( value, property )`][@hishprorg/placeat-iste/has-own-property]</span><span class="delimiter">: </span><span class="description">test if an object has a specified property.</span>
-   <span class="signature">[`hasProp( value, property )`][@hishprorg/placeat-iste/has-property]</span><span class="delimiter">: </span><span class="description">test if an object has a specified property, either own or inherited.</span>
-   <span class="signature">[`hasUTF16SurrogatePairAt( string, position )`][@hishprorg/placeat-iste/has-utf16-surrogate-pair-at]</span><span class="delimiter">: </span><span class="description">test if a position in a string marks the start of a UTF-16 surrogate pair.</span>
-   <span class="signature">[`instanceOf( value, constructor )`][@hishprorg/placeat-iste/instance-of]</span><span class="delimiter">: </span><span class="description">test whether a value has in its prototype chain a specified constructor as a prototype property.</span>
-   <span class="signature">[`isAbsoluteHttpURI( value )`][@hishprorg/placeat-iste/is-absolute-http-uri]</span><span class="delimiter">: </span><span class="description">test whether a value is an absolute HTTP(S) URI.</span>
-   <span class="signature">[`isAbsolutePath( value )`][@hishprorg/placeat-iste/is-absolute-path]</span><span class="delimiter">: </span><span class="description">test if a value is an absolute path.</span>
-   <span class="signature">[`isAbsoluteURI( value )`][@hishprorg/placeat-iste/is-absolute-uri]</span><span class="delimiter">: </span><span class="description">test whether a value is an absolute URI.</span>
-   <span class="signature">[`isAccessorPropertyIn( value, property )`][@hishprorg/placeat-iste/is-accessor-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property has an accessor descriptor.</span>
-   <span class="signature">[`isAccessorProperty( value, property )`][@hishprorg/placeat-iste/is-accessor-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property has an accessor descriptor.</span>
-   <span class="signature">[`isAlphagram( value )`][@hishprorg/placeat-iste/is-alphagram]</span><span class="delimiter">: </span><span class="description">test if a value is an alphagram.</span>
-   <span class="signature">[`isAlphaNumeric( value )`][@hishprorg/placeat-iste/is-alphanumeric]</span><span class="delimiter">: </span><span class="description">test whether a string contains only alphanumeric characters.</span>
-   <span class="signature">[`isAnagram( str, value )`][@hishprorg/placeat-iste/is-anagram]</span><span class="delimiter">: </span><span class="description">test if a value is an anagram.</span>
-   <span class="signature">[`isArguments( value )`][@hishprorg/placeat-iste/is-arguments]</span><span class="delimiter">: </span><span class="description">test if a value is an arguments object.</span>
-   <span class="signature">[`isArrowFunction( value )`][@hishprorg/placeat-iste/is-arrow-function]</span><span class="delimiter">: </span><span class="description">test if a value is an `arrow function`.</span>
-   <span class="signature">[`isASCII( value )`][@hishprorg/placeat-iste/is-ascii]</span><span class="delimiter">: </span><span class="description">test whether a character belongs to the ASCII character set and whether this is true for all characters in a provided string.</span>
-   <span class="signature">[`isBetween( value, a, b[, left, right] )`][@hishprorg/placeat-iste/is-between]</span><span class="delimiter">: </span><span class="description">test if a value is between two values.</span>
-   <span class="signature">[`isBigInt( value )`][@hishprorg/placeat-iste/is-bigint]</span><span class="delimiter">: </span><span class="description">test if a value is a BigInt.</span>
-   <span class="signature">[`isBinaryString( value )`][@hishprorg/placeat-iste/is-binary-string]</span><span class="delimiter">: </span><span class="description">test if a value is a binary string.</span>
-   <span class="signature">[`isBlankString( value )`][@hishprorg/placeat-iste/is-blank-string]</span><span class="delimiter">: </span><span class="description">test if a value is a blank string.</span>
-   <span class="signature">[`isBoxedPrimitive( value )`][@hishprorg/placeat-iste/is-boxed-primitive]</span><span class="delimiter">: </span><span class="description">test if a value is a JavaScript boxed primitive.</span>
-   <span class="signature">[`isBuffer( value )`][@hishprorg/placeat-iste/is-buffer]</span><span class="delimiter">: </span><span class="description">test if a value is a Buffer object.</span>
-   <span class="signature">[`isCamelcase( value )`][@hishprorg/placeat-iste/is-camelcase]</span><span class="delimiter">: </span><span class="description">test if a value is a camelcase string.</span>
-   <span class="signature">[`isCapitalized( value )`][@hishprorg/placeat-iste/is-capitalized]</span><span class="delimiter">: </span><span class="description">test if a value is a string having an uppercase first character.</span>
-   <span class="signature">[`isCircular( value )`][@hishprorg/placeat-iste/is-circular]</span><span class="delimiter">: </span><span class="description">test if a value is a plain object containing a circular reference.</span>
-   <span class="signature">[`isCircular( value )`][@hishprorg/placeat-iste/is-circular]</span><span class="delimiter">: </span><span class="description">test if an object-like value contains a circular reference.</span>
-   <span class="signature">[`isClass( value )`][@hishprorg/placeat-iste/is-class]</span><span class="delimiter">: </span><span class="description">test if a value is a class.</span>
-   <span class="signature">[`isCollection( value )`][@hishprorg/placeat-iste/is-collection]</span><span class="delimiter">: </span><span class="description">test if a value is a collection.</span>
-   <span class="signature">[`isComposite( value )`][@hishprorg/placeat-iste/is-composite]</span><span class="delimiter">: </span><span class="description">test if a value is a composite number.</span>
-   <span class="signature">[`isConfigurablePropertyIn( value, property )`][@hishprorg/placeat-iste/is-configurable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is configurable.</span>
-   <span class="signature">[`isConfigurableProperty( value, property )`][@hishprorg/placeat-iste/is-configurable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is configurable.</span>
-   <span class="signature">[`isConstantcase( value )`][@hishprorg/placeat-iste/is-constantcase]</span><span class="delimiter">: </span><span class="description">test if a value is a constantcase string.</span>
-   <span class="signature">[`isCurrentYear( value )`][@hishprorg/placeat-iste/is-current-year]</span><span class="delimiter">: </span><span class="description">test if a value is the current year.</span>
-   <span class="signature">[`isDataPropertyIn( value, property )`][@hishprorg/placeat-iste/is-data-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property has a data descriptor.</span>
-   <span class="signature">[`isDataProperty( value, property )`][@hishprorg/placeat-iste/is-data-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property has a data descriptor.</span>
-   <span class="signature">[`isDataView( value )`][@hishprorg/placeat-iste/is-dataview]</span><span class="delimiter">: </span><span class="description">test if a value is a DataView.</span>
-   <span class="signature">[`isDigitString( value )`][@hishprorg/placeat-iste/is-digit-string]</span><span class="delimiter">: </span><span class="description">test whether a string contains only numeric digits.</span>
-   <span class="signature">[`isDomainName( value )`][@hishprorg/placeat-iste/is-domain-name]</span><span class="delimiter">: </span><span class="description">test if a value is a domain name.</span>
-   <span class="signature">[`isDurationString( value )`][@hishprorg/placeat-iste/is-duration-string]</span><span class="delimiter">: </span><span class="description">test if a value is a duration string.</span>
-   <span class="signature">[`isEmailAddress( value )`][@hishprorg/placeat-iste/is-email-address]</span><span class="delimiter">: </span><span class="description">test if a value is an email address.</span>
-   <span class="signature">[`isEmptyCollection( value )`][@hishprorg/placeat-iste/is-empty-collection]</span><span class="delimiter">: </span><span class="description">test if a value is an empty collection.</span>
-   <span class="signature">[`isEmptyObject( value )`][@hishprorg/placeat-iste/is-empty-object]</span><span class="delimiter">: </span><span class="description">test if a value is an empty object.</span>
-   <span class="signature">[`isEmptyString( value )`][@hishprorg/placeat-iste/is-empty-string]</span><span class="delimiter">: </span><span class="description">test if a value is an empty string.</span>
-   <span class="signature">[`isEnumerablePropertyIn( value, property )`][@hishprorg/placeat-iste/is-enumerable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is enumerable.</span>
-   <span class="signature">[`isEnumerableProperty( value, property )`][@hishprorg/placeat-iste/is-enumerable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is enumerable.</span>
-   <span class="signature">[`isEven( value )`][@hishprorg/placeat-iste/is-even]</span><span class="delimiter">: </span><span class="description">test if a value is an even number.</span>
-   <span class="signature">[`isFalsy( value )`][@hishprorg/placeat-iste/is-falsy]</span><span class="delimiter">: </span><span class="description">test if a value is falsy.</span>
-   <span class="signature">[`isFinite( value )`][@hishprorg/placeat-iste/is-finite]</span><span class="delimiter">: </span><span class="description">test if a value is a finite number.</span>
-   <span class="signature">[`isGeneratorObjectLike( value )`][@hishprorg/placeat-iste/is-generator-object-like]</span><span class="delimiter">: </span><span class="description">test if a value is `generator` object-like.</span>
-   <span class="signature">[`isGeneratorObject( value )`][@hishprorg/placeat-iste/is-generator-object]</span><span class="delimiter">: </span><span class="description">test if a value is a `generator` object.</span>
-   <span class="signature">[`isgzipBuffer( value )`][@hishprorg/placeat-iste/is-gzip-buffer]</span><span class="delimiter">: </span><span class="description">test if a value is a gzip buffer.</span>
-   <span class="signature">[`isHexString( value )`][@hishprorg/placeat-iste/is-hex-string]</span><span class="delimiter">: </span><span class="description">test whether a string contains only hexadecimal digits.</span>
-   <span class="signature">[`isInfinite( value )`][@hishprorg/placeat-iste/is-infinite]</span><span class="delimiter">: </span><span class="description">test if a value is an infinite number.</span>
-   <span class="signature">[`isInheritedProperty( value, property )`][@hishprorg/placeat-iste/is-inherited-property]</span><span class="delimiter">: </span><span class="description">test if an object has an inherited property.</span>
-   <span class="signature">[`isIterableLike( value )`][@hishprorg/placeat-iste/is-iterable-like]</span><span class="delimiter">: </span><span class="description">test if a value is `iterable`-like.</span>
-   <span class="signature">[`isIteratorLike( value )`][@hishprorg/placeat-iste/is-iterator-like]</span><span class="delimiter">: </span><span class="description">test if a value is `iterator`-like.</span>
-   <span class="signature">[`isJSON( value )`][@hishprorg/placeat-iste/is-json]</span><span class="delimiter">: </span><span class="description">test if a value is a parseable JSON string.</span>
-   <span class="signature">[`isKebabcase( value )`][@hishprorg/placeat-iste/is-kebabcase]</span><span class="delimiter">: </span><span class="description">test if a value is a string in kebab case.</span>
-   <span class="signature">[`isLeapYear( [value] )`][@hishprorg/placeat-iste/is-leap-year]</span><span class="delimiter">: </span><span class="description">test if a value corresponds to a leap year in the Gregorian calendar.</span>
-   <span class="signature">[`isLocalhost( value )`][@hishprorg/placeat-iste/is-localhost]</span><span class="delimiter">: </span><span class="description">test whether a value is a localhost hostname.</span>
-   <span class="signature">[`isLowercase( value )`][@hishprorg/placeat-iste/is-lowercase]</span><span class="delimiter">: </span><span class="description">test if a value is a lowercase string.</span>
-   <span class="signature">[`isMethodIn( value, property )`][@hishprorg/placeat-iste/is-method-in]</span><span class="delimiter">: </span><span class="description">test if an object has a specified method name, either own or inherited.</span>
-   <span class="signature">[`isMethod( value, property )`][@hishprorg/placeat-iste/is-method]</span><span class="delimiter">: </span><span class="description">test if an object has a specified method name.</span>
-   <span class="signature">[`isMultiSlice( value )`][@hishprorg/placeat-iste/is-multi-slice]</span><span class="delimiter">: </span><span class="description">test if a value is a `MultiSlice`.</span>
-   <span class="signature">[`isNamedTypedTupleLike( value )`][@hishprorg/placeat-iste/is-named-typed-tuple-like]</span><span class="delimiter">: </span><span class="description">test if a value is named typed tuple-like.</span>
-   <span class="signature">[`isNativeFunction( value )`][@hishprorg/placeat-iste/is-native-function]</span><span class="delimiter">: </span><span class="description">test if a value is a native function.</span>
-   <span class="signature">[`isNegativeZero( value )`][@hishprorg/placeat-iste/is-negative-zero]</span><span class="delimiter">: </span><span class="description">test if a value is a number equal to negative zero.</span>
-   <span class="signature">[`isNodeBuiltin( value )`][@hishprorg/placeat-iste/is-node-builtin]</span><span class="delimiter">: </span><span class="description">test whether a string matches a Node.js built-in module name.</span>
-   <span class="signature">[`isNodeDuplexStreamLike( value )`][@hishprorg/placeat-iste/is-node-duplex-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node duplex stream-like.</span>
-   <span class="signature">[`isNodeReadableStreamLike( value )`][@hishprorg/placeat-iste/is-node-readable-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node readable stream-like.</span>
-   <span class="signature">[`isNodeREPL()`][@hishprorg/placeat-iste/is-node-repl]</span><span class="delimiter">: </span><span class="description">check if running in a Node.js REPL environment.</span>
-   <span class="signature">[`isNodeStreamLike( value )`][@hishprorg/placeat-iste/is-node-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node stream-like.</span>
-   <span class="signature">[`isNodeTransformStreamLike( value )`][@hishprorg/placeat-iste/is-node-transform-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node transform stream-like.</span>
-   <span class="signature">[`isNodeWritableStreamLike( value )`][@hishprorg/placeat-iste/is-node-writable-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node writable stream-like.</span>
-   <span class="signature">[`isNonConfigurablePropertyIn( value, property )`][@hishprorg/placeat-iste/is-nonconfigurable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is non-configurable.</span>
-   <span class="signature">[`isNonConfigurableProperty( value, property )`][@hishprorg/placeat-iste/is-nonconfigurable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is non-configurable.</span>
-   <span class="signature">[`isNonEnumerablePropertyIn( value, property )`][@hishprorg/placeat-iste/is-nonenumerable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is non-enumerable.</span>
-   <span class="signature">[`isNonEnumerableProperty( value, property )`][@hishprorg/placeat-iste/is-nonenumerable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is non-enumerable.</span>
-   <span class="signature">[`isNonNegativeFinite( value )`][@hishprorg/placeat-iste/is-nonnegative-finite]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonnegative finite value.</span>
-   <span class="signature">[`isObjectLike( value )`][@hishprorg/placeat-iste/is-object-like]</span><span class="delimiter">: </span><span class="description">test if a value is object-like.</span>
-   <span class="signature">[`isOdd( value )`][@hishprorg/placeat-iste/is-odd]</span><span class="delimiter">: </span><span class="description">test if a value is an odd number.</span>
-   <span class="signature">[`isPascalcase( value )`][@hishprorg/placeat-iste/is-pascalcase]</span><span class="delimiter">: </span><span class="description">test if a value is a string in Pascal case.</span>
-   <span class="signature">[`isPlainObject( value )`][@hishprorg/placeat-iste/is-plain-object]</span><span class="delimiter">: </span><span class="description">test if a value is a plain object.</span>
-   <span class="signature">[`isPositiveZero( value )`][@hishprorg/placeat-iste/is-positive-zero]</span><span class="delimiter">: </span><span class="description">test if a value is a number equal to positive zero.</span>
-   <span class="signature">[`isPrime( value )`][@hishprorg/placeat-iste/is-prime]</span><span class="delimiter">: </span><span class="description">test if a value is a prime number.</span>
-   <span class="signature">[`isPrimitive( value )`][@hishprorg/placeat-iste/is-primitive]</span><span class="delimiter">: </span><span class="description">test if a value is a JavaScript primitive.</span>
-   <span class="signature">[`isPRNGLike( value )`][@hishprorg/placeat-iste/is-prng-like]</span><span class="delimiter">: </span><span class="description">test if a value is PRNG-like.</span>
-   <span class="signature">[`isProbability( value )`][@hishprorg/placeat-iste/is-probability]</span><span class="delimiter">: </span><span class="description">test if a value is a probability.</span>
-   <span class="signature">[`isPropertyKey( value )`][@hishprorg/placeat-iste/is-property-key]</span><span class="delimiter">: </span><span class="description">test whether a value is a property key.</span>
-   <span class="signature">[`isPrototypeOf( obj, prototype )`][@hishprorg/placeat-iste/is-prototype-of]</span><span class="delimiter">: </span><span class="description">test if an object's prototype chain contains a provided prototype.</span>
-   <span class="signature">[`isReadOnlyPropertyIn( value, property )`][@hishprorg/placeat-iste/is-read-only-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is read-only.</span>
-   <span class="signature">[`isReadOnlyProperty( value, property )`][@hishprorg/placeat-iste/is-read-only-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is read-only.</span>
-   <span class="signature">[`isReadWritePropertyIn( value, property )`][@hishprorg/placeat-iste/is-read-write-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is readable and writable.</span>
-   <span class="signature">[`isReadWriteProperty( value, property )`][@hishprorg/placeat-iste/is-read-write-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is readable and writable.</span>
-   <span class="signature">[`isReadablePropertyIn( value, property )`][@hishprorg/placeat-iste/is-readable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is readable.</span>
-   <span class="signature">[`isReadableProperty( value, property )`][@hishprorg/placeat-iste/is-readable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is readable.</span>
-   <span class="signature">[`isRegExpString( value )`][@hishprorg/placeat-iste/is-regexp-string]</span><span class="delimiter">: </span><span class="description">test if a value is a regular expression string.</span>
-   <span class="signature">[`isRelativePath( value )`][@hishprorg/placeat-iste/is-relative-path]</span><span class="delimiter">: </span><span class="description">test if a value is a relative path.</span>
-   <span class="signature">[`isRelativeURI( value )`][@hishprorg/placeat-iste/is-relative-uri]</span><span class="delimiter">: </span><span class="description">test whether a value is a relative URI.</span>
-   <span class="signature">[`isSameComplex128( v1, v2 )`][@hishprorg/placeat-iste/is-same-complex128]</span><span class="delimiter">: </span><span class="description">test if two arguments are both double-precision complex floating-point numbers and have the same value.</span>
-   <span class="signature">[`isSameComplex64( v1, v2 )`][@hishprorg/placeat-iste/is-same-complex64]</span><span class="delimiter">: </span><span class="description">test if two arguments are both single-precision complex floating-point numbers and have the same value.</span>
-   <span class="signature">[`isSameNativeClass( a, b )`][@hishprorg/placeat-iste/is-same-native-class]</span><span class="delimiter">: </span><span class="description">test if two arguments have the same native class.</span>
-   <span class="signature">[`isSameType( a, b )`][@hishprorg/placeat-iste/is-same-type]</span><span class="delimiter">: </span><span class="description">test if two arguments have the same type.</span>
-   <span class="signature">[`isSameValueZero( a, b )`][@hishprorg/placeat-iste/is-same-value-zero]</span><span class="delimiter">: </span><span class="description">test if two arguments are the same value.</span>
-   <span class="signature">[`isSameValue( a, b )`][@hishprorg/placeat-iste/is-same-value]</span><span class="delimiter">: </span><span class="description">test if two arguments are the same value.</span>
-   <span class="signature">[`isSemVer( value )`][@hishprorg/placeat-iste/is-semver]</span><span class="delimiter">: </span><span class="description">test if a value is a semantic version string.</span>
-   <span class="signature">[`isSlice( value )`][@hishprorg/placeat-iste/is-slice]</span><span class="delimiter">: </span><span class="description">test if a value is a `Slice`.</span>
-   <span class="signature">[`isSnakecase( value )`][@hishprorg/placeat-iste/is-snakecase]</span><span class="delimiter">: </span><span class="description">test if a value is a string in snake case.</span>
-   <span class="signature">[`isStartcase( value )`][@hishprorg/placeat-iste/is-startcase]</span><span class="delimiter">: </span><span class="description">test if a value is a startcase string.</span>
-   <span class="signature">[`isStrictEqual( a, b )`][@hishprorg/placeat-iste/is-strict-equal]</span><span class="delimiter">: </span><span class="description">test if two arguments are strictly equal.</span>
-   <span class="signature">[`isTruthy( value )`][@hishprorg/placeat-iste/is-truthy]</span><span class="delimiter">: </span><span class="description">test if a value is truthy.</span>
-   <span class="signature">[`isUNCPath( value )`][@hishprorg/placeat-iste/is-unc-path]</span><span class="delimiter">: </span><span class="description">test if a value is a UNC path.</span>
-   <span class="signature">[`isUndefinedOrNull( value )`][@hishprorg/placeat-iste/is-undefined-or-null]</span><span class="delimiter">: </span><span class="description">test if a value is undefined or null.</span>
-   <span class="signature">[`isUppercase( value )`][@hishprorg/placeat-iste/is-uppercase]</span><span class="delimiter">: </span><span class="description">test if a value is an uppercase string.</span>
-   <span class="signature">[`isURI( value )`][@hishprorg/placeat-iste/is-uri]</span><span class="delimiter">: </span><span class="description">test if a value is a URI.</span>
-   <span class="signature">[`isWhitespace( value )`][@hishprorg/placeat-iste/is-whitespace]</span><span class="delimiter">: </span><span class="description">test whether a string contains only white space characters.</span>
-   <span class="signature">[`isWritablePropertyIn( value, property )`][@hishprorg/placeat-iste/is-writable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is writable.</span>
-   <span class="signature">[`isWritableProperty( value, property )`][@hishprorg/placeat-iste/is-writable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is writable.</span>
-   <span class="signature">[`isWriteOnlyPropertyIn( value, property )`][@hishprorg/placeat-iste/is-write-only-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is write-only.</span>
-   <span class="signature">[`isWriteOnlyProperty( value, property )`][@hishprorg/placeat-iste/is-write-only-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is write-only.</span>
-   <span class="signature">[`tools`][@hishprorg/placeat-iste/tools]</span><span class="delimiter">: </span><span class="description">assertion utility tools.</span>

</div>

<!-- </toc> -->

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- TODO: better examples -->

<!-- eslint no-undef: "error" -->

```javascript
var objectKeys = require( '@stdlib/utils/keys' );
var assert = require( '@hishprorg/placeat-iste' );

console.log( objectKeys( assert ) );
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@hishprorg/placeat-iste.svg
[npm-url]: https://npmjs.org/package/@hishprorg/placeat-iste

[test-image]: https://github.com/hishprorg/placeat-iste/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/hishprorg/placeat-iste/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/hishprorg/placeat-iste/main.svg
[coverage-url]: https://codecov.io/github/hishprorg/placeat-iste?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/hishprorg/placeat-iste.svg
[dependencies-url]: https://david-dm.org/hishprorg/placeat-iste/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/hishprorg/placeat-iste/tree/deno
[deno-readme]: https://github.com/hishprorg/placeat-iste/blob/deno/README.md
[umd-url]: https://github.com/hishprorg/placeat-iste/tree/umd
[umd-readme]: https://github.com/hishprorg/placeat-iste/blob/umd/README.md
[esm-url]: https://github.com/hishprorg/placeat-iste/tree/esm
[esm-readme]: https://github.com/hishprorg/placeat-iste/blob/esm/README.md
[branches-url]: https://github.com/hishprorg/placeat-iste/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/hishprorg/placeat-iste/main/LICENSE

<!-- <toc-links> -->

[@hishprorg/placeat-iste/contains]: https://github.com/hishprorg/placeat-iste/tree/main/contains

[@hishprorg/placeat-iste/deep-equal]: https://github.com/hishprorg/placeat-iste/tree/main/deep-equal

[@hishprorg/placeat-iste/deep-has-own-property]: https://github.com/hishprorg/placeat-iste/tree/main/deep-has-own-property

[@hishprorg/placeat-iste/deep-has-property]: https://github.com/hishprorg/placeat-iste/tree/main/deep-has-property

[@hishprorg/placeat-iste/has-own-property]: https://github.com/hishprorg/placeat-iste/tree/main/has-own-property

[@hishprorg/placeat-iste/has-property]: https://github.com/hishprorg/placeat-iste/tree/main/has-property

[@hishprorg/placeat-iste/has-utf16-surrogate-pair-at]: https://github.com/hishprorg/placeat-iste/tree/main/has-utf16-surrogate-pair-at

[@hishprorg/placeat-iste/instance-of]: https://github.com/hishprorg/placeat-iste/tree/main/instance-of

[@hishprorg/placeat-iste/is-absolute-http-uri]: https://github.com/hishprorg/placeat-iste/tree/main/is-absolute-http-uri

[@hishprorg/placeat-iste/is-absolute-path]: https://github.com/hishprorg/placeat-iste/tree/main/is-absolute-path

[@hishprorg/placeat-iste/is-absolute-uri]: https://github.com/hishprorg/placeat-iste/tree/main/is-absolute-uri

[@hishprorg/placeat-iste/is-accessor-property-in]: https://github.com/hishprorg/placeat-iste/tree/main/is-accessor-property-in

[@hishprorg/placeat-iste/is-accessor-property]: https://github.com/hishprorg/placeat-iste/tree/main/is-accessor-property

[@hishprorg/placeat-iste/is-alphagram]: https://github.com/hishprorg/placeat-iste/tree/main/is-alphagram

[@hishprorg/placeat-iste/is-alphanumeric]: https://github.com/hishprorg/placeat-iste/tree/main/is-alphanumeric

[@hishprorg/placeat-iste/is-anagram]: https://github.com/hishprorg/placeat-iste/tree/main/is-anagram

[@hishprorg/placeat-iste/is-arguments]: https://github.com/hishprorg/placeat-iste/tree/main/is-arguments

[@hishprorg/placeat-iste/is-arrow-function]: https://github.com/hishprorg/placeat-iste/tree/main/is-arrow-function

[@hishprorg/placeat-iste/is-ascii]: https://github.com/hishprorg/placeat-iste/tree/main/is-ascii

[@hishprorg/placeat-iste/is-between]: https://github.com/hishprorg/placeat-iste/tree/main/is-between

[@hishprorg/placeat-iste/is-bigint]: https://github.com/hishprorg/placeat-iste/tree/main/is-bigint

[@hishprorg/placeat-iste/is-binary-string]: https://github.com/hishprorg/placeat-iste/tree/main/is-binary-string

[@hishprorg/placeat-iste/is-blank-string]: https://github.com/hishprorg/placeat-iste/tree/main/is-blank-string

[@hishprorg/placeat-iste/is-boxed-primitive]: https://github.com/hishprorg/placeat-iste/tree/main/is-boxed-primitive

[@hishprorg/placeat-iste/is-buffer]: https://github.com/hishprorg/placeat-iste/tree/main/is-buffer

[@hishprorg/placeat-iste/is-camelcase]: https://github.com/hishprorg/placeat-iste/tree/main/is-camelcase

[@hishprorg/placeat-iste/is-capitalized]: https://github.com/hishprorg/placeat-iste/tree/main/is-capitalized

[@hishprorg/placeat-iste/is-circular]: https://github.com/hishprorg/placeat-iste/tree/main/is-circular

[@hishprorg/placeat-iste/is-class]: https://github.com/hishprorg/placeat-iste/tree/main/is-class

[@hishprorg/placeat-iste/is-collection]: https://github.com/hishprorg/placeat-iste/tree/main/is-collection

[@hishprorg/placeat-iste/is-composite]: https://github.com/hishprorg/placeat-iste/tree/main/is-composite

[@hishprorg/placeat-iste/is-configurable-property-in]: https://github.com/hishprorg/placeat-iste/tree/main/is-configurable-property-in

[@hishprorg/placeat-iste/is-configurable-property]: https://github.com/hishprorg/placeat-iste/tree/main/is-configurable-property

[@hishprorg/placeat-iste/is-constantcase]: https://github.com/hishprorg/placeat-iste/tree/main/is-constantcase

[@hishprorg/placeat-iste/is-current-year]: https://github.com/hishprorg/placeat-iste/tree/main/is-current-year

[@hishprorg/placeat-iste/is-data-property-in]: https://github.com/hishprorg/placeat-iste/tree/main/is-data-property-in

[@hishprorg/placeat-iste/is-data-property]: https://github.com/hishprorg/placeat-iste/tree/main/is-data-property

[@hishprorg/placeat-iste/is-dataview]: https://github.com/hishprorg/placeat-iste/tree/main/is-dataview

[@hishprorg/placeat-iste/is-digit-string]: https://github.com/hishprorg/placeat-iste/tree/main/is-digit-string

[@hishprorg/placeat-iste/is-domain-name]: https://github.com/hishprorg/placeat-iste/tree/main/is-domain-name

[@hishprorg/placeat-iste/is-duration-string]: https://github.com/hishprorg/placeat-iste/tree/main/is-duration-string

[@hishprorg/placeat-iste/is-email-address]: https://github.com/hishprorg/placeat-iste/tree/main/is-email-address

[@hishprorg/placeat-iste/is-empty-collection]: https://github.com/hishprorg/placeat-iste/tree/main/is-empty-collection

[@hishprorg/placeat-iste/is-empty-object]: https://github.com/hishprorg/placeat-iste/tree/main/is-empty-object

[@hishprorg/placeat-iste/is-empty-string]: https://github.com/hishprorg/placeat-iste/tree/main/is-empty-string

[@hishprorg/placeat-iste/is-enumerable-property-in]: https://github.com/hishprorg/placeat-iste/tree/main/is-enumerable-property-in

[@hishprorg/placeat-iste/is-enumerable-property]: https://github.com/hishprorg/placeat-iste/tree/main/is-enumerable-property

[@hishprorg/placeat-iste/is-even]: https://github.com/hishprorg/placeat-iste/tree/main/is-even

[@hishprorg/placeat-iste/is-falsy]: https://github.com/hishprorg/placeat-iste/tree/main/is-falsy

[@hishprorg/placeat-iste/is-finite]: https://github.com/hishprorg/placeat-iste/tree/main/is-finite

[@hishprorg/placeat-iste/is-generator-object-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-generator-object-like

[@hishprorg/placeat-iste/is-generator-object]: https://github.com/hishprorg/placeat-iste/tree/main/is-generator-object

[@hishprorg/placeat-iste/is-gzip-buffer]: https://github.com/hishprorg/placeat-iste/tree/main/is-gzip-buffer

[@hishprorg/placeat-iste/is-hex-string]: https://github.com/hishprorg/placeat-iste/tree/main/is-hex-string

[@hishprorg/placeat-iste/is-infinite]: https://github.com/hishprorg/placeat-iste/tree/main/is-infinite

[@hishprorg/placeat-iste/is-inherited-property]: https://github.com/hishprorg/placeat-iste/tree/main/is-inherited-property

[@hishprorg/placeat-iste/is-iterable-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-iterable-like

[@hishprorg/placeat-iste/is-iterator-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-iterator-like

[@hishprorg/placeat-iste/is-json]: https://github.com/hishprorg/placeat-iste/tree/main/is-json

[@hishprorg/placeat-iste/is-kebabcase]: https://github.com/hishprorg/placeat-iste/tree/main/is-kebabcase

[@hishprorg/placeat-iste/is-leap-year]: https://github.com/hishprorg/placeat-iste/tree/main/is-leap-year

[@hishprorg/placeat-iste/is-localhost]: https://github.com/hishprorg/placeat-iste/tree/main/is-localhost

[@hishprorg/placeat-iste/is-lowercase]: https://github.com/hishprorg/placeat-iste/tree/main/is-lowercase

[@hishprorg/placeat-iste/is-method-in]: https://github.com/hishprorg/placeat-iste/tree/main/is-method-in

[@hishprorg/placeat-iste/is-method]: https://github.com/hishprorg/placeat-iste/tree/main/is-method

[@hishprorg/placeat-iste/is-multi-slice]: https://github.com/hishprorg/placeat-iste/tree/main/is-multi-slice

[@hishprorg/placeat-iste/is-named-typed-tuple-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-named-typed-tuple-like

[@hishprorg/placeat-iste/is-native-function]: https://github.com/hishprorg/placeat-iste/tree/main/is-native-function

[@hishprorg/placeat-iste/is-negative-zero]: https://github.com/hishprorg/placeat-iste/tree/main/is-negative-zero

[@hishprorg/placeat-iste/is-node-builtin]: https://github.com/hishprorg/placeat-iste/tree/main/is-node-builtin

[@hishprorg/placeat-iste/is-node-duplex-stream-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-node-duplex-stream-like

[@hishprorg/placeat-iste/is-node-readable-stream-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-node-readable-stream-like

[@hishprorg/placeat-iste/is-node-repl]: https://github.com/hishprorg/placeat-iste/tree/main/is-node-repl

[@hishprorg/placeat-iste/is-node-stream-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-node-stream-like

[@hishprorg/placeat-iste/is-node-transform-stream-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-node-transform-stream-like

[@hishprorg/placeat-iste/is-node-writable-stream-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-node-writable-stream-like

[@hishprorg/placeat-iste/is-nonconfigurable-property-in]: https://github.com/hishprorg/placeat-iste/tree/main/is-nonconfigurable-property-in

[@hishprorg/placeat-iste/is-nonconfigurable-property]: https://github.com/hishprorg/placeat-iste/tree/main/is-nonconfigurable-property

[@hishprorg/placeat-iste/is-nonenumerable-property-in]: https://github.com/hishprorg/placeat-iste/tree/main/is-nonenumerable-property-in

[@hishprorg/placeat-iste/is-nonenumerable-property]: https://github.com/hishprorg/placeat-iste/tree/main/is-nonenumerable-property

[@hishprorg/placeat-iste/is-nonnegative-finite]: https://github.com/hishprorg/placeat-iste/tree/main/is-nonnegative-finite

[@hishprorg/placeat-iste/is-object-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-object-like

[@hishprorg/placeat-iste/is-odd]: https://github.com/hishprorg/placeat-iste/tree/main/is-odd

[@hishprorg/placeat-iste/is-pascalcase]: https://github.com/hishprorg/placeat-iste/tree/main/is-pascalcase

[@hishprorg/placeat-iste/is-plain-object]: https://github.com/hishprorg/placeat-iste/tree/main/is-plain-object

[@hishprorg/placeat-iste/is-positive-zero]: https://github.com/hishprorg/placeat-iste/tree/main/is-positive-zero

[@hishprorg/placeat-iste/is-prime]: https://github.com/hishprorg/placeat-iste/tree/main/is-prime

[@hishprorg/placeat-iste/is-primitive]: https://github.com/hishprorg/placeat-iste/tree/main/is-primitive

[@hishprorg/placeat-iste/is-prng-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-prng-like

[@hishprorg/placeat-iste/is-probability]: https://github.com/hishprorg/placeat-iste/tree/main/is-probability

[@hishprorg/placeat-iste/is-property-key]: https://github.com/hishprorg/placeat-iste/tree/main/is-property-key

[@hishprorg/placeat-iste/is-prototype-of]: https://github.com/hishprorg/placeat-iste/tree/main/is-prototype-of

[@hishprorg/placeat-iste/is-read-only-property-in]: https://github.com/hishprorg/placeat-iste/tree/main/is-read-only-property-in

[@hishprorg/placeat-iste/is-read-only-property]: https://github.com/hishprorg/placeat-iste/tree/main/is-read-only-property

[@hishprorg/placeat-iste/is-read-write-property-in]: https://github.com/hishprorg/placeat-iste/tree/main/is-read-write-property-in

[@hishprorg/placeat-iste/is-read-write-property]: https://github.com/hishprorg/placeat-iste/tree/main/is-read-write-property

[@hishprorg/placeat-iste/is-readable-property-in]: https://github.com/hishprorg/placeat-iste/tree/main/is-readable-property-in

[@hishprorg/placeat-iste/is-readable-property]: https://github.com/hishprorg/placeat-iste/tree/main/is-readable-property

[@hishprorg/placeat-iste/is-regexp-string]: https://github.com/hishprorg/placeat-iste/tree/main/is-regexp-string

[@hishprorg/placeat-iste/is-relative-path]: https://github.com/hishprorg/placeat-iste/tree/main/is-relative-path

[@hishprorg/placeat-iste/is-relative-uri]: https://github.com/hishprorg/placeat-iste/tree/main/is-relative-uri

[@hishprorg/placeat-iste/is-same-complex128]: https://github.com/hishprorg/placeat-iste/tree/main/is-same-complex128

[@hishprorg/placeat-iste/is-same-complex64]: https://github.com/hishprorg/placeat-iste/tree/main/is-same-complex64

[@hishprorg/placeat-iste/is-same-native-class]: https://github.com/hishprorg/placeat-iste/tree/main/is-same-native-class

[@hishprorg/placeat-iste/is-same-type]: https://github.com/hishprorg/placeat-iste/tree/main/is-same-type

[@hishprorg/placeat-iste/is-same-value-zero]: https://github.com/hishprorg/placeat-iste/tree/main/is-same-value-zero

[@hishprorg/placeat-iste/is-same-value]: https://github.com/hishprorg/placeat-iste/tree/main/is-same-value

[@hishprorg/placeat-iste/is-semver]: https://github.com/hishprorg/placeat-iste/tree/main/is-semver

[@hishprorg/placeat-iste/is-slice]: https://github.com/hishprorg/placeat-iste/tree/main/is-slice

[@hishprorg/placeat-iste/is-snakecase]: https://github.com/hishprorg/placeat-iste/tree/main/is-snakecase

[@hishprorg/placeat-iste/is-startcase]: https://github.com/hishprorg/placeat-iste/tree/main/is-startcase

[@hishprorg/placeat-iste/is-strict-equal]: https://github.com/hishprorg/placeat-iste/tree/main/is-strict-equal

[@hishprorg/placeat-iste/is-truthy]: https://github.com/hishprorg/placeat-iste/tree/main/is-truthy

[@hishprorg/placeat-iste/is-unc-path]: https://github.com/hishprorg/placeat-iste/tree/main/is-unc-path

[@hishprorg/placeat-iste/is-undefined-or-null]: https://github.com/hishprorg/placeat-iste/tree/main/is-undefined-or-null

[@hishprorg/placeat-iste/is-uppercase]: https://github.com/hishprorg/placeat-iste/tree/main/is-uppercase

[@hishprorg/placeat-iste/is-uri]: https://github.com/hishprorg/placeat-iste/tree/main/is-uri

[@hishprorg/placeat-iste/is-whitespace]: https://github.com/hishprorg/placeat-iste/tree/main/is-whitespace

[@hishprorg/placeat-iste/is-writable-property-in]: https://github.com/hishprorg/placeat-iste/tree/main/is-writable-property-in

[@hishprorg/placeat-iste/is-writable-property]: https://github.com/hishprorg/placeat-iste/tree/main/is-writable-property

[@hishprorg/placeat-iste/is-write-only-property-in]: https://github.com/hishprorg/placeat-iste/tree/main/is-write-only-property-in

[@hishprorg/placeat-iste/is-write-only-property]: https://github.com/hishprorg/placeat-iste/tree/main/is-write-only-property

[@hishprorg/placeat-iste/tools]: https://github.com/hishprorg/placeat-iste/tree/main/tools

[@hishprorg/placeat-iste/has-arraybuffer-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-arraybuffer-support

[@hishprorg/placeat-iste/has-arrow-function-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-arrow-function-support

[@hishprorg/placeat-iste/has-async-await-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-async-await-support

[@hishprorg/placeat-iste/has-async-iterator-symbol-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-async-iterator-symbol-support

[@hishprorg/placeat-iste/has-bigint-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-bigint-support

[@hishprorg/placeat-iste/has-bigint64array-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-bigint64array-support

[@hishprorg/placeat-iste/has-biguint64array-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-biguint64array-support

[@hishprorg/placeat-iste/has-class-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-class-support

[@hishprorg/placeat-iste/has-dataview-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-dataview-support

[@hishprorg/placeat-iste/has-define-properties-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-define-properties-support

[@hishprorg/placeat-iste/has-define-property-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-define-property-support

[@hishprorg/placeat-iste/has-float32array-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-float32array-support

[@hishprorg/placeat-iste/has-float64array-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-float64array-support

[@hishprorg/placeat-iste/has-function-name-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-function-name-support

[@hishprorg/placeat-iste/has-generator-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-generator-support

[@hishprorg/placeat-iste/has-globalthis-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-globalthis-support

[@hishprorg/placeat-iste/has-int16array-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-int16array-support

[@hishprorg/placeat-iste/has-int32array-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-int32array-support

[@hishprorg/placeat-iste/has-int8array-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-int8array-support

[@hishprorg/placeat-iste/has-iterator-symbol-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-iterator-symbol-support

[@hishprorg/placeat-iste/has-map-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-map-support

[@hishprorg/placeat-iste/has-node-buffer-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-node-buffer-support

[@hishprorg/placeat-iste/has-proxy-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-proxy-support

[@hishprorg/placeat-iste/has-set-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-set-support

[@hishprorg/placeat-iste/has-sharedarraybuffer-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-sharedarraybuffer-support

[@hishprorg/placeat-iste/has-symbol-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-symbol-support

[@hishprorg/placeat-iste/has-tostringtag-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-tostringtag-support

[@hishprorg/placeat-iste/has-uint16array-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-uint16array-support

[@hishprorg/placeat-iste/has-uint32array-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-uint32array-support

[@hishprorg/placeat-iste/has-uint8array-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-uint8array-support

[@hishprorg/placeat-iste/has-uint8clampedarray-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-uint8clampedarray-support

[@hishprorg/placeat-iste/has-wasm-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-wasm-support

[@hishprorg/placeat-iste/has-weakmap-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-weakmap-support

[@hishprorg/placeat-iste/has-weakset-support]: https://github.com/hishprorg/placeat-iste/tree/main/has-weakset-support

[@hishprorg/placeat-iste/is-big-endian]: https://github.com/hishprorg/placeat-iste/tree/main/is-big-endian

[@hishprorg/placeat-iste/is-browser]: https://github.com/hishprorg/placeat-iste/tree/main/is-browser

[@hishprorg/placeat-iste/is-darwin]: https://github.com/hishprorg/placeat-iste/tree/main/is-darwin

[@hishprorg/placeat-iste/is-docker]: https://github.com/hishprorg/placeat-iste/tree/main/is-docker

[@hishprorg/placeat-iste/is-electron-main]: https://github.com/hishprorg/placeat-iste/tree/main/is-electron-main

[@hishprorg/placeat-iste/is-electron-renderer]: https://github.com/hishprorg/placeat-iste/tree/main/is-electron-renderer

[@hishprorg/placeat-iste/is-electron]: https://github.com/hishprorg/placeat-iste/tree/main/is-electron

[@hishprorg/placeat-iste/is-little-endian]: https://github.com/hishprorg/placeat-iste/tree/main/is-little-endian

[@hishprorg/placeat-iste/is-mobile]: https://github.com/hishprorg/placeat-iste/tree/main/is-mobile

[@hishprorg/placeat-iste/is-node]: https://github.com/hishprorg/placeat-iste/tree/main/is-node

[@hishprorg/placeat-iste/is-touch-device]: https://github.com/hishprorg/placeat-iste/tree/main/is-touch-device

[@hishprorg/placeat-iste/is-web-worker]: https://github.com/hishprorg/placeat-iste/tree/main/is-web-worker

[@hishprorg/placeat-iste/is-windows]: https://github.com/hishprorg/placeat-iste/tree/main/is-windows

[@hishprorg/placeat-iste/is-error]: https://github.com/hishprorg/placeat-iste/tree/main/is-error

[@hishprorg/placeat-iste/is-eval-error]: https://github.com/hishprorg/placeat-iste/tree/main/is-eval-error

[@hishprorg/placeat-iste/is-range-error]: https://github.com/hishprorg/placeat-iste/tree/main/is-range-error

[@hishprorg/placeat-iste/is-reference-error]: https://github.com/hishprorg/placeat-iste/tree/main/is-reference-error

[@hishprorg/placeat-iste/is-syntax-error]: https://github.com/hishprorg/placeat-iste/tree/main/is-syntax-error

[@hishprorg/placeat-iste/is-type-error]: https://github.com/hishprorg/placeat-iste/tree/main/is-type-error

[@hishprorg/placeat-iste/is-uri-error]: https://github.com/hishprorg/placeat-iste/tree/main/is-uri-error

[@hishprorg/placeat-iste/is-accessor-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-accessor-array

[@hishprorg/placeat-iste/is-array-length]: https://github.com/hishprorg/placeat-iste/tree/main/is-array-length

[@hishprorg/placeat-iste/is-array-like-object]: https://github.com/hishprorg/placeat-iste/tree/main/is-array-like-object

[@hishprorg/placeat-iste/is-array-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-array-like

[@hishprorg/placeat-iste/is-arraybuffer-view]: https://github.com/hishprorg/placeat-iste/tree/main/is-arraybuffer-view

[@hishprorg/placeat-iste/is-arraybuffer]: https://github.com/hishprorg/placeat-iste/tree/main/is-arraybuffer

[@hishprorg/placeat-iste/is-between-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-between-array

[@hishprorg/placeat-iste/is-bigint64array]: https://github.com/hishprorg/placeat-iste/tree/main/is-bigint64array

[@hishprorg/placeat-iste/is-biguint64array]: https://github.com/hishprorg/placeat-iste/tree/main/is-biguint64array

[@hishprorg/placeat-iste/is-circular-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-circular-array

[@hishprorg/placeat-iste/is-empty-array-like-object]: https://github.com/hishprorg/placeat-iste/tree/main/is-empty-array-like-object

[@hishprorg/placeat-iste/is-empty-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-empty-array

[@hishprorg/placeat-iste/is-falsy-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-falsy-array

[@hishprorg/placeat-iste/is-finite-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-finite-array

[@hishprorg/placeat-iste/is-numeric-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-numeric-array

[@hishprorg/placeat-iste/is-plain-object-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-plain-object-array

[@hishprorg/placeat-iste/is-probability-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-probability-array

[@hishprorg/placeat-iste/is-same-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-same-array

[@hishprorg/placeat-iste/is-same-complex128array]: https://github.com/hishprorg/placeat-iste/tree/main/is-same-complex128array

[@hishprorg/placeat-iste/is-same-complex64array]: https://github.com/hishprorg/placeat-iste/tree/main/is-same-complex64array

[@hishprorg/placeat-iste/is-same-float32array]: https://github.com/hishprorg/placeat-iste/tree/main/is-same-float32array

[@hishprorg/placeat-iste/is-same-float64array]: https://github.com/hishprorg/placeat-iste/tree/main/is-same-float64array

[@hishprorg/placeat-iste/is-sharedarraybuffer]: https://github.com/hishprorg/placeat-iste/tree/main/is-sharedarraybuffer

[@hishprorg/placeat-iste/is-truthy-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-truthy-array

[@hishprorg/placeat-iste/is-typed-array-length]: https://github.com/hishprorg/placeat-iste/tree/main/is-typed-array-length

[@hishprorg/placeat-iste/is-typed-array-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-typed-array-like

[@hishprorg/placeat-iste/is-typed-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-typed-array

[@hishprorg/placeat-iste/is-unity-probability-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-unity-probability-array

[@hishprorg/placeat-iste/is-complex-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-complex-like

[@hishprorg/placeat-iste/is-complex-typed-array-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-complex-typed-array-like

[@hishprorg/placeat-iste/is-complex-typed-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-complex-typed-array

[@hishprorg/placeat-iste/is-complex]: https://github.com/hishprorg/placeat-iste/tree/main/is-complex

[@hishprorg/placeat-iste/is-complex128]: https://github.com/hishprorg/placeat-iste/tree/main/is-complex128

[@hishprorg/placeat-iste/is-complex128array]: https://github.com/hishprorg/placeat-iste/tree/main/is-complex128array

[@hishprorg/placeat-iste/is-complex64]: https://github.com/hishprorg/placeat-iste/tree/main/is-complex64

[@hishprorg/placeat-iste/is-complex64array]: https://github.com/hishprorg/placeat-iste/tree/main/is-complex64array

[@hishprorg/placeat-iste/is-centrosymmetric-matrix]: https://github.com/hishprorg/placeat-iste/tree/main/is-centrosymmetric-matrix

[@hishprorg/placeat-iste/is-complex128matrix-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-complex128matrix-like

[@hishprorg/placeat-iste/is-complex128ndarray-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-complex128ndarray-like

[@hishprorg/placeat-iste/is-complex128vector-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-complex128vector-like

[@hishprorg/placeat-iste/is-complex64matrix-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-complex64matrix-like

[@hishprorg/placeat-iste/is-complex64ndarray-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-complex64ndarray-like

[@hishprorg/placeat-iste/is-complex64vector-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-complex64vector-like

[@hishprorg/placeat-iste/is-float32matrix-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-float32matrix-like

[@hishprorg/placeat-iste/is-float32ndarray-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-float32ndarray-like

[@hishprorg/placeat-iste/is-float32vector-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-float32vector-like

[@hishprorg/placeat-iste/is-float64matrix-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-float64matrix-like

[@hishprorg/placeat-iste/is-float64ndarray-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-float64ndarray-like

[@hishprorg/placeat-iste/is-float64vector-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-float64vector-like

[@hishprorg/placeat-iste/is-matrix-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-matrix-like

[@hishprorg/placeat-iste/is-ndarray-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-ndarray-like

[@hishprorg/placeat-iste/is-nonsymmetric-matrix]: https://github.com/hishprorg/placeat-iste/tree/main/is-nonsymmetric-matrix

[@hishprorg/placeat-iste/is-persymmetric-matrix]: https://github.com/hishprorg/placeat-iste/tree/main/is-persymmetric-matrix

[@hishprorg/placeat-iste/is-skew-centrosymmetric-matrix]: https://github.com/hishprorg/placeat-iste/tree/main/is-skew-centrosymmetric-matrix

[@hishprorg/placeat-iste/is-skew-persymmetric-matrix]: https://github.com/hishprorg/placeat-iste/tree/main/is-skew-persymmetric-matrix

[@hishprorg/placeat-iste/is-skew-symmetric-matrix]: https://github.com/hishprorg/placeat-iste/tree/main/is-skew-symmetric-matrix

[@hishprorg/placeat-iste/is-square-matrix]: https://github.com/hishprorg/placeat-iste/tree/main/is-square-matrix

[@hishprorg/placeat-iste/is-symmetric-matrix]: https://github.com/hishprorg/placeat-iste/tree/main/is-symmetric-matrix

[@hishprorg/placeat-iste/is-vector-like]: https://github.com/hishprorg/placeat-iste/tree/main/is-vector-like

[@hishprorg/placeat-iste/is-float32array]: https://github.com/hishprorg/placeat-iste/tree/main/is-float32array

[@hishprorg/placeat-iste/is-float64array]: https://github.com/hishprorg/placeat-iste/tree/main/is-float64array

[@hishprorg/placeat-iste/is-int16array]: https://github.com/hishprorg/placeat-iste/tree/main/is-int16array

[@hishprorg/placeat-iste/is-int32array]: https://github.com/hishprorg/placeat-iste/tree/main/is-int32array

[@hishprorg/placeat-iste/is-int8array]: https://github.com/hishprorg/placeat-iste/tree/main/is-int8array

[@hishprorg/placeat-iste/is-uint16array]: https://github.com/hishprorg/placeat-iste/tree/main/is-uint16array

[@hishprorg/placeat-iste/is-uint32array]: https://github.com/hishprorg/placeat-iste/tree/main/is-uint32array

[@hishprorg/placeat-iste/is-uint8array]: https://github.com/hishprorg/placeat-iste/tree/main/is-uint8array

[@hishprorg/placeat-iste/is-uint8clampedarray]: https://github.com/hishprorg/placeat-iste/tree/main/is-uint8clampedarray

[@hishprorg/placeat-iste/is-cube-number]: https://github.com/hishprorg/placeat-iste/tree/main/is-cube-number

[@hishprorg/placeat-iste/is-integer-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-integer-array

[@hishprorg/placeat-iste/is-integer]: https://github.com/hishprorg/placeat-iste/tree/main/is-integer

[@hishprorg/placeat-iste/is-negative-integer-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-negative-integer-array

[@hishprorg/placeat-iste/is-negative-integer]: https://github.com/hishprorg/placeat-iste/tree/main/is-negative-integer

[@hishprorg/placeat-iste/is-negative-number-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-negative-number-array

[@hishprorg/placeat-iste/is-negative-number]: https://github.com/hishprorg/placeat-iste/tree/main/is-negative-number

[@hishprorg/placeat-iste/is-nonnegative-integer-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-nonnegative-integer-array

[@hishprorg/placeat-iste/is-nonnegative-integer]: https://github.com/hishprorg/placeat-iste/tree/main/is-nonnegative-integer

[@hishprorg/placeat-iste/is-nonnegative-number-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-nonnegative-number-array

[@hishprorg/placeat-iste/is-nonnegative-number]: https://github.com/hishprorg/placeat-iste/tree/main/is-nonnegative-number

[@hishprorg/placeat-iste/is-nonpositive-integer-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-nonpositive-integer-array

[@hishprorg/placeat-iste/is-nonpositive-integer]: https://github.com/hishprorg/placeat-iste/tree/main/is-nonpositive-integer

[@hishprorg/placeat-iste/is-nonpositive-number-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-nonpositive-number-array

[@hishprorg/placeat-iste/is-nonpositive-number]: https://github.com/hishprorg/placeat-iste/tree/main/is-nonpositive-number

[@hishprorg/placeat-iste/is-positive-integer-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-positive-integer-array

[@hishprorg/placeat-iste/is-positive-integer]: https://github.com/hishprorg/placeat-iste/tree/main/is-positive-integer

[@hishprorg/placeat-iste/is-positive-number-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-positive-number-array

[@hishprorg/placeat-iste/is-positive-number]: https://github.com/hishprorg/placeat-iste/tree/main/is-positive-number

[@hishprorg/placeat-iste/is-safe-integer-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-safe-integer-array

[@hishprorg/placeat-iste/is-safe-integer]: https://github.com/hishprorg/placeat-iste/tree/main/is-safe-integer

[@hishprorg/placeat-iste/is-square-number]: https://github.com/hishprorg/placeat-iste/tree/main/is-square-number

[@hishprorg/placeat-iste/is-square-triangular-number]: https://github.com/hishprorg/placeat-iste/tree/main/is-square-triangular-number

[@hishprorg/placeat-iste/is-triangular-number]: https://github.com/hishprorg/placeat-iste/tree/main/is-triangular-number

[@hishprorg/placeat-iste/is-array-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-array-array

[@hishprorg/placeat-iste/is-boolean-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-boolean-array

[@hishprorg/placeat-iste/is-date-object-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-date-object-array

[@hishprorg/placeat-iste/is-function-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-function-array

[@hishprorg/placeat-iste/is-nan-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-nan-array

[@hishprorg/placeat-iste/is-null-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-null-array

[@hishprorg/placeat-iste/is-number-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-number-array

[@hishprorg/placeat-iste/is-object-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-object-array

[@hishprorg/placeat-iste/is-string-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-string-array

[@hishprorg/placeat-iste/is-symbol-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-symbol-array

[@hishprorg/placeat-iste/is-array]: https://github.com/hishprorg/placeat-iste/tree/main/is-array

[@hishprorg/placeat-iste/is-boolean]: https://github.com/hishprorg/placeat-iste/tree/main/is-boolean

[@hishprorg/placeat-iste/is-date-object]: https://github.com/hishprorg/placeat-iste/tree/main/is-date-object

[@hishprorg/placeat-iste/is-function]: https://github.com/hishprorg/placeat-iste/tree/main/is-function

[@hishprorg/placeat-iste/is-nan]: https://github.com/hishprorg/placeat-iste/tree/main/is-nan

[@hishprorg/placeat-iste/is-null]: https://github.com/hishprorg/placeat-iste/tree/main/is-null

[@hishprorg/placeat-iste/is-number]: https://github.com/hishprorg/placeat-iste/tree/main/is-number

[@hishprorg/placeat-iste/is-object]: https://github.com/hishprorg/placeat-iste/tree/main/is-object

[@hishprorg/placeat-iste/is-regexp]: https://github.com/hishprorg/placeat-iste/tree/main/is-regexp

[@hishprorg/placeat-iste/is-string]: https://github.com/hishprorg/placeat-iste/tree/main/is-string

[@hishprorg/placeat-iste/is-symbol]: https://github.com/hishprorg/placeat-iste/tree/main/is-symbol

[@hishprorg/placeat-iste/is-undefined]: https://github.com/hishprorg/placeat-iste/tree/main/is-undefined

<!-- </toc-links> -->

</section>

<!-- /.links -->
