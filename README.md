<!--

@license Apache-2.0

Copyright (c) 2024 The Stdlib Authors.

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

# isBooleanArray

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Test if a value is a [`BooleanArray`][@stdlib/array/bool].

<section class="intro">

</section>

<!-- ./intro -->

<section class="installation">

## Installation

```bash
npm install @stdlib/array-base-assert-is-booleanarray
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
var isBooleanArray = require( '@stdlib/array-base-assert-is-booleanarray' );
```

#### isBooleanArray( value )

Tests if a value is a [`BooleanArray`][@stdlib/array/bool].

```javascript
var BooleanArray = require( '@stdlib/array-bool' );

var arr = new BooleanArray( 10 );
var bool = isBooleanArray( arr );
// returns true
```

</section>

<!-- /.usage -->

<section class="notes">

## Notes

-   This function is not robust and that is intentional. This function provides a lower cost way to reasonably determine whether an input value is a [`BooleanArray`][@stdlib/array/bool] in order to avoid walking the prototype chain and resolving constructors, which is necessary for robust identification of cross-realm instances. For more robust validation, see [`@stdlib/assert-is-booleanarray`][@stdlib/assert/is-booleanarray].

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint-disable object-curly-newline -->

<!-- eslint no-undef: "error" -->

```javascript
var Int8Array = require( '@stdlib/array-int8' );
var Uint8Array = require( '@stdlib/array-uint8' );
var Uint8ClampedArray = require( '@stdlib/array-uint8c' );
var Int16Array = require( '@stdlib/array-int16' );
var Uint16Array = require( '@stdlib/array-uint16' );
var Int32Array = require( '@stdlib/array-int32' );
var Uint32Array = require( '@stdlib/array-uint32' );
var Float32Array = require( '@stdlib/array-float32' );
var Float64Array = require( '@stdlib/array-float64' );
var Complex128Array = require( '@stdlib/array-complex128' );
var Complex64Array = require( '@stdlib/array-complex64' );
var BooleanArray = require( '@stdlib/array-bool' );
var isBooleanArray = require( '@stdlib/array-base-assert-is-booleanarray' );

var bool = isBooleanArray( new BooleanArray( 10 ) );
// returns true

bool = isBooleanArray( new Complex64Array( 10 ) );
// returns false

bool = isBooleanArray( new Complex128Array( 10 ) );
// returns false

bool = isBooleanArray( [] );
// returns false

bool = isBooleanArray( new Float64Array( 10 ) );
// returns false

bool = isBooleanArray( new Float32Array( 10 ) );
// returns false

bool = isBooleanArray( new Int32Array( 10 ) );
// returns false

bool = isBooleanArray( new Uint32Array( 10 ) );
// returns false

bool = isBooleanArray( new Int16Array( 10 ) );
// returns false

bool = isBooleanArray( new Uint16Array( 10 ) );
// returns false

bool = isBooleanArray( new Int8Array( 10 ) );
// returns false

bool = isBooleanArray( new Uint8Array( 10 ) );
// returns false

bool = isBooleanArray( new Uint8ClampedArray( 10 ) );
// returns false

bool = isBooleanArray( { 'length': 0 } );
// returns false
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

Copyright &copy; 2016-2025. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/array-base-assert-is-booleanarray.svg
[npm-url]: https://npmjs.org/package/@stdlib/array-base-assert-is-booleanarray

[test-image]: https://github.com/stdlib-js/array-base-assert-is-booleanarray/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/array-base-assert-is-booleanarray/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/array-base-assert-is-booleanarray/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/array-base-assert-is-booleanarray?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/array-base-assert-is-booleanarray.svg
[dependencies-url]: https://david-dm.org/stdlib-js/array-base-assert-is-booleanarray/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/array-base-assert-is-booleanarray/tree/deno
[deno-readme]: https://github.com/stdlib-js/array-base-assert-is-booleanarray/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/array-base-assert-is-booleanarray/tree/umd
[umd-readme]: https://github.com/stdlib-js/array-base-assert-is-booleanarray/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/array-base-assert-is-booleanarray/tree/esm
[esm-readme]: https://github.com/stdlib-js/array-base-assert-is-booleanarray/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/array-base-assert-is-booleanarray/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/array-base-assert-is-booleanarray/main/LICENSE

[@stdlib/array/bool]: https://github.com/stdlib-js/array-bool

[@stdlib/assert/is-booleanarray]: https://github.com/stdlib-js/assert-is-booleanarray

<!-- <related-links> -->

<!-- </related-links> -->

</section>

<!-- /.links -->
