Sum-Product Probabilistic Language
==================================

SPPL is a probabilistic programming language that delivers exact inferences
to a broad range of probabilistic inference queries. SPPL handles
continuous and discrete distributions, many-to-one numerical
transformations, and a query language that includes general predicates on
random variables.

Users express generative models using imperative code with standard
programming constructs (arrays, if/else, for loops, etc.). This code is
then translated to a sum-product representation (a of probabilistic
graphical model that generalizes [sum-product networks](https://arxiv.org/pdf/2004.01167.pdf))
that statically represents the probability distribution on all random
variables in the program and is used as the basis of probabilistic
inference.

A system description of SPPL is given in:

> Exact Symbolic Inference in Probabilistic Programs via Sum-Product Representations. <br/>
> Feras A. Saad, Martin C. Rinard, and Vikash K. Mansinghka. <br/>
> https://arxiv.org/abs/2010.03485

### Installation

This software is tested on Ubuntu 18.04 and requires a Python 3.6+
environment. SPPL is available on PyPI

    $ pip install sppl

It may be necessary to install the system-wide dependencies in
[./requirements.sh](./requirements.sh).

### Tests

To run the test suite as a user:

    $ python -m pytest --pyargs sppl

To run the test suite as a developer:

- To run crash tests:             `$ ./check.sh`
- To run integration tests:       `$ ./check.sh ci`
- To run a specific test:         `$ ./check.sh [<pytest-opts>] /path/to/test.py`
- To run the examples:            `$ ./check.sh examples`
- To build a docker image:        `$ ./check.sh docker`
- To generate a coverage report:  `$ ./check.sh coverage`

To view the coverage report, open `htmlcov/index.html` in the browser.

### Examples

Refer to the `.ipynb` notebooks under the [examples](./examples/) directory.

### Benchmarks

Refer to https://github.com/probcomp/sppl-benchmarks-oct20

### Language Reference

Coming Soon!

### License

Apache 2.0; see [LICENSE.txt](./LICENSE.txt)
