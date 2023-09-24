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

# Standard Normal Random Numbers

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Create a [readable stream][readable-stream] for generating pseudorandom numbers drawn from a [standard normal][normal] distribution using the [Box-Muller transform][@stdlib/random/base/box-muller].









<!-- Section for describing a command-line interface. -->



<section class="cli">



<section class="installation">

## Installation

To use as a general utility, install the CLI package globally

```bash
npm install -g @stdlib/random-streams-box-muller-cli
```

</section>
<!-- CLI usage documentation. -->


<section class="usage">

## Usage

```text
Usage: random-box-muller [options]

Options:

  -h,  --help               Print this message.
  -V,  --version            Print the package version.
       --sep sep            Separator used to join streamed data. Default: '\n'.
  -n,  --iter iterations    Number of pseudorandom numbers.
       --seed seed          Pseudorandom number generator seed.
       --state filepath     Path to a file containing the pseudorandom number
                            generator state.
       --snapshot filepath  Output file path for saving the pseudorandom number
                            generator state upon exit.
```

</section>

<!-- /.usage -->

<!-- CLI usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

## Notes

-   In accordance with POSIX convention, a trailing newline is **always** appended to generated output prior to exit.
-   Specifying a "snapshot" file path is useful when wanting to resume pseudorandom number generation due to, e.g., a downstream failure in an analysis pipeline. Before exiting, the process will store the pseudorandom number generator state in a file specified according to a provided file path. Upon loading a snapshot (state), the process will generate pseudorandom numbers starting from the loaded state, thus avoiding having to seed and replay an entire analysis.

</section>

<!-- /.notes -->

<!-- CLI usage examples. -->

<section class="examples">

## Examples

```bash
$ random-box-muller -n 10 --seed 1234
```

</section>

<!-- /.examples -->

</section>

<!-- /.cli -->

* * *

<section class="references">

## References

-   Box, G. E. P., and Mervin E. Muller. 1958. "A Note on the Generation of Random Normal Deviates." _The Annals of Mathematical Statistics_ 29 (2). The Institute of Mathematical Statistics: 610–11. doi:[10.1214/aoms/1177706645][@box:1958].
-   Bell, James R. 1968. "Algorithm 334: Normal Random Deviates." _Communications of the ACM_ 11 (7). New York, NY, USA: ACM: 498. doi:[10.1145/363397.363547][@bell:1968].
-   Knop, R. 1969. "Remark on Algorithm 334 \[G5]: Normal Random Deviates." _Communications of the ACM_ 12 (5). New York, NY, USA: ACM: 281. doi:[10.1145/362946.362996][@knop:1969].
-   Marsaglia, G., and T. A. Bray. 1964. "A Convenient Method for Generating Normal Variables." _SIAM Review_ 6 (3). Society for Industrial; Applied Mathematics: 260–64. doi:[10.1137/1006063][@marsaglia:1964a].
-   Thomas, David B., Wayne Luk, Philip H.W. Leong, and John D. Villasenor. 2007. "Gaussian Random Number Generators." _ACM Computing Surveys_ 39 (4). New York, NY, USA: ACM. doi:[10.1145/1287620.1287622][@thomas:2007].

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

## See Also

-   <span class="package-name">[`@stdlib/random-streams-box-muller`][@stdlib/random-streams-box-muller]</span><span class="delimiter">: </span><span class="description">create a readable stream for generating pseudorandom numbers drawn from a standard normal distribution using the Box-Muller transform.</span>
-   <span class="package-name">[`@stdlib/random-base/box-muller`][@stdlib/random/base/box-muller]</span><span class="delimiter">: </span><span class="description">normally distributed pseudorandom numbers using the Box-Muller transform.</span>
-   <span class="package-name">[`@stdlib/random-iter/box-muller`][@stdlib/random/iter/box-muller]</span><span class="delimiter">: </span><span class="description">create an iterator for generating pseudorandom numbers drawn from a standard normal distribution using the Box-Muller transform.</span>
-   <span class="package-name">[`@stdlib/random-streams/improved-ziggurat`][@stdlib/random/streams/improved-ziggurat]</span><span class="delimiter">: </span><span class="description">create a readable stream for generating pseudorandom numbers drawn from a standard normal distribution using the Improved Ziggurat algorithm.</span>
-   <span class="package-name">[`@stdlib/random-streams/randn`][@stdlib/random/streams/randn]</span><span class="delimiter">: </span><span class="description">create a readable stream for generating pseudorandom numbers drawn from a standard normal distribution.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/random-streams-box-muller-cli.svg
[npm-url]: https://npmjs.org/package/@stdlib/random-streams-box-muller-cli

[test-image]: https://github.com/stdlib-js/random-streams-box-muller@v0.1.0/actions/workflows/test.yml/badge.svg?branch=v0.1.0
[test-url]: https://github.com/stdlib-js/random-streams-box-muller@v0.1.0/actions/workflows/test.yml?query=branch:v0.1.0

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/random-streams-box-muller@v0.1.0/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/random-streams-box-muller@v0.1.0?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/random-streams-box-muller@v0.1.0.svg
[dependencies-url]: https://david-dm.org/stdlib-js/random-streams-box-muller@v0.1.0/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[cli-section]: https://github.com/stdlib-js/random-streams-box-muller@v0.1.0#cli
[cli-url]: https://github.com/stdlib-js/random-streams-box-muller@v0.1.0/tree/cli
[@stdlib/random-streams-box-muller]: https://github.com/stdlib-js/random-streams-box-muller@v0.1.0/tree/main

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/random-streams-box-muller@v0.1.0/tree/deno
[umd-url]: https://github.com/stdlib-js/random-streams-box-muller@v0.1.0/tree/umd
[esm-url]: https://github.com/stdlib-js/random-streams-box-muller@v0.1.0/tree/esm
[branches-url]: https://github.com/stdlib-js/random-streams-box-muller@v0.1.0/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/random-streams-box-muller@v0.1.0/main/LICENSE

[stream]: https://nodejs.org/api/stream.html

[object-mode]: https://nodejs.org/api/stream.html#stream_object_mode

[readable-stream]: https://nodejs.org/api/stream.html

[normal]: https://en.wikipedia.org/wiki/Normal_distribution

[@stdlib/array/uint32]: https://github.com/stdlib-js/array-uint32

[@box:1958]: http://dx.doi.org/10.1214/aoms/1177706645

[@bell:1968]: http://dx.doi.org/10.1145/363397.363547

[@knop:1969]: http://dx.doi.org/10.1145/362946.362996

[@marsaglia:1964a]: http://dx.doi.org/10.1137/1006063

[@thomas:2007]: http://dx.doi.org/10.1145/1287620.128762

<!-- <related-links> -->

[@stdlib/random/base/box-muller]: https://github.com/stdlib-js/random-base-box-muller

[@stdlib/random/iter/box-muller]: https://github.com/stdlib-js/random-iter-box-muller

[@stdlib/random/streams/improved-ziggurat]: https://github.com/stdlib-js/random-streams-improved-ziggurat

[@stdlib/random/streams/randn]: https://github.com/stdlib-js/random-streams-randn

<!-- </related-links> -->

</section>

<!-- /.links -->
