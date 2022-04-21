#   Gaining Confidence in Your Code through Testing

##  Objectives

-   Use assertions as fences to check that the program state is correct.
-   Apply test-driven development to specify an effective code before
    development.
-   Compose a unit test to ensure proper positive behavior (i.e., when
    the behavior should succeed).
-   Compose a unit test to handle proper negative behavior (i.e., when
    failure should happen).
-   Apply unit testing to diagnose a buggy program.
-   Employ a unit-testing framework such as **pytest** to automate
    testing.

##  Introduction

[**Test-driven
development**](https://katyhuff.github.io/python-testing/09-tdd/) refers
to the practice of fully specifying desired function
behavior *before* composing the function itself. The advantage of this
approach is that it forces you to clarify ahead of time what you expect,
rather than making it up on the fly.

In this lesson, we will discuss aspects and implementation of
test-driven development as a philosophy. Many languages offer testing
frameworks which automatically run tests.

##  Methods

### Fences

The first weapon in our battle for correct software is the *fence*.
Fences are barriers employed to block program execution if the state
isn\'t adequate to the intended task. Different languages deal with data
validation differently: this can be a major problem for dynamically
typed languages like Python, whereas C/C++ and even Cython avoid much of
the difficulty.

For instance, what happens if someone passes non-numeric data to an
absolute value function **abs**?

**def abs_uf( x ):**

* *return x if x \>= 0 else -x**

We can avoid this problem by providing a fence:

**def abs_f( x ):**

* *assert type( x ) in ( float,int )**

* *return x if x \>= 0 else -x**

The fence prevents the program from raising a **TypeError**. (Of course,
now there is an **AssertionError** to deal with!) But this process can
help you locate where invalid data are being generated before
processing.

-   Why have an **assert**-based fence rather than a conditional
    statement? When would each be better suited?

    The advantage of assertions is their ease of use. They are rarely
    more than one line of code. The disadvantage is that assertions halt
    execution indiscriminately and the helpfulness of the resulting
    error message is usually quite limited. Input checking may require
    decending a rabbit hole of exceptional cases. (Huff)

-   What is the difference in speed between the fenced and unfenced
    versions of **abs**? Run the following in IPython.

    **%timeit abs_uf( 1 )**

    **%timeit abs_f( 1 )**

    Fences take little time to write and do not contribute appreciably
    to the program run time.

Useful features of Python
include **isinstance**, **is**, **np.isclose**, and **np.allclose**.
Other modern languages provide analogues.

### Test-Driven Development

\"Unit tests are so called because they exercise the functionality of
the code by interrogating individual functions and methods. Functions
and methods can often be considered the atomic units of software because
they are indivisible. However, what is considered to be the smallest
code unit is subjective. The body of a function can be long are short,
and shorter functions are arguably more unit-like than long ones.\"
(Huff)

In Python and many other languages, unit tests refer to functions, often
prefixed **test\_**, that specify (and enforce) the expected behavior of
a given function. Unit tests typically contain setup, assertions, and
tear-down. In academic terms, they\'re a grading script.

Discussion: Fences and Unit Tests
---------------------------------

-   Are unit tests a replacement of fences?

Consider an absolute value function, here written in Python:

**def absolute( x ):**

* *return x if x \> 0 else -x**

A unit test for **absolute** above could look like this:

**def test_absolute():**

* *assert absolute( 5 ) == 5**

* *assert absolute( 0 ) == 0**

* *assert absolute( -5 ) == 5**

* *assert absolute( 5.0 ) == 5.0**

* *assert absolute( 0.0 ) == 0.0**

* *assert absolute( -5.0 ) == 5.0**

* *assert absolute( -12345678901234567890 ) == 12345678901234567890**

* *try:**

* *assert absolute( \"5\" ) == 5 \# should raise exception**

* *except e:**

* *assert isinstance( e,TypeError )**

### Positive Unit Tests

*Our working language for the next examples will be Python.*

Unit tests come in two categories:

1.  Positive: the function should succeed or handle a case correctly.
2.  Negative: the function should fail or reject a condition.

In this module, we examine positive behavior.

Consider an absolute value function. The positive unit tests
for **absolute** should accomplish a few things:

1.  Verify correct behavior for positive numeric input.
2.  Verify correct behavior for negative numeric input.
3.  Verify correct behavior for zero input.
4.  Verify that the function works for **int**, **long** (Python
    2.x), **float**, and **complex** (if implemented).

Note that at this point *we don\'t care what the function looks like*,
only how it behaves.

This portion of the tests could look like this:

**def test_absolute():**

* *\# Test integer behavior**

* *assert absolute( 5 ) == 5**

* *assert absolute( 0 ) == 0**

* *assert absolute( -5 ) == 5**

* *\# Test float behavior**

* *assert absolute( 5.0 ) == 5.0**

* *assert absolute( 0.0 ) == 0.0**

* *assert absolute( -5.0 ) == 5.0**

* *\# Test long behavior (obsolete in Python 3)**

* *assert absolute( -12345678901234567890 ) == 12345678901234567890**

### Negative Unit Tests

Negative unit tests are designed to make a function or module fail. This
can include fuzzing or ill-formed input.

Consider again an absolute value function. The negative unit tests
for **absolute** should:

1.  Verify an exception is raised for nonnumeric input.
2.  Verify *correct* exceptions are raised for various kinds of input.

Again, at this point *we don\'t care what the function looks like*, only
how it behaves.

This portion of the tests could look like this:

**def test_absolute():**

* *\# Check exceptions**

* *try:**

* *assert absolute( \"5\" ) == 5 \# should raise exception**

* *except e:**

* *assert isinstance( e,TypeError )**

* *try:**

* *assert absolute( \[ 0 \] ) == 0 \# should raise exception**

* *except e:**

* *assert isinstance( e,TypeError )**

### Unit-Testing Frameworks

A testing framework locates all unit tests (that adhere to a certain
naming convention) and runs them in a block with a report. For instance,
Python developers typically use **pytest**.

**pytest** is straightforward. Download the files

-   [**mean.py**](https://raw.githubusercontent.com/katyhuff/python-testing/gh-pages/code/mean.py)
-   [**test_mean.py**](https://raw.githubusercontent.com/katyhuff/python-testing/gh-pages/code/test_mean.py)

In a directory with them, enter:

**py.test**

Code Coverage
=============

[**Code coverage**](https://en.wikipedia.org/wiki/Code_coverage) refers
to the proportion of the code which is subject to testing (rather than
the completeness of those tests).

Code coverage can be classified into function coverage, loop coverage,
etc. The basic idea is to test every part of the code that can be
tested. Naturally, code coverage pairs with test-driven development.

If code coverage is good, more code coverage is better, right? You\'ll
never get to 100% though. For one thing, coverage tests themselves add
code (although you can factor this out of the denominator). For another,
you can actually trick yourself: having good code coverage isn\'t the
same as having good tests. Runtime bugs could be missed anyway, such as
race conditions or performance under load.

### Introduction

Software verification and validation are separate quality assurance
processes. V&V plays various rôles in different industries, but for
software tends to take the form:

-   **Validation**: Is the software product the correct product for the
    customer or application?
-   **Verification**: Is the software product built correctly?

Well-posed specifications and requirements are necessary to ensure that
V&V can be carried out properly.

Independent V&V processes can be carried out by a third party auditor
for mission-critical or safety-critical applications.

### Software Verification

Software verification is the process of methodically evaluating your
code, using tests to determine if behavior adheres to the specification.

Complete *verification* is a misnomer: a program can never be
demonstrated correct, only to not have certain faults. Thus verification
is really much more like the principle of falsification in the
philosophy of science.

Program testing can be used to show the presence of bugs, but never to
show their absence. (Dijkstra)

We have extensively discussed unit testing already in **dev/tdd**; the
main idea to keep in mind is that software verification tests are those
tests which check that processes work as they should. (*Most* tests fall
into this category, or the opposite category of ensuring appropriate
failure.)

Various kinds of tests are available, beyond basic unit tests:

Five typologies of experiments can be distinguished in the process of
specifying, implementing, and evaluating computing artifacts. -
Feasibility experiments are performed to evaluate whether an artifact of
interest performs the functions specified by users and stakeholders; -
trial experiments are more specific experiments carried out to evaluate
isolated capabilities of the system given some set of initial
conditions; - field experiment are performed in real environments and
not in simulated ones; - comparison experiments test similar artifacts,
instantiating in different ways the same function, to evaluate which
instantiation better performs the desired function both in real-like and
real environments; - finally, controlled experiments are used to
appraise advanced hypotheses on the behaviors of the testing artifact.
(SEP, \"Philosophy of Computer Science\")

Computer security techniques are occasionally used in software
verification. For
instance, [**fuzzing**](https://en.wikipedia.org/wiki/Fuzzing) is a
technique of throwing random or targeted data at a particular interface
to discover its behavior and limitations. Fuzzing can be used
maliciously to obtain access to restricted data, but fuzzing can also be
used to test software behavior.

Notably, the process and aims of software verification and validation
differ dramatically from verification and validation in scientific
computing. (See **dev/v-and-v-scientific** in CS 491SC for more
information.)

### References

-   [**Stanford Encyclopedia of
    Philosophy**](https://plato.stanford.edu/entries/computer-science/)[*,
    \"Philosophy of Computer
    Science\"*](https://plato.stanford.edu/entries/computer-science/)

### Software Validation

Software validation is the process of making sure that the software
product being developed can actually speak to the desired end.

To keep things straight, think of a physical model used in
engineering. *Verification* would mean making sure that the mathematical
model is correctly implemented. *Validation* would mean making sure that
the mathematical model actually describes reality.

In software, requirements are used to validate software. Requirements
are spoken of as coming from a *customer*, but not infrequently the
\"customer\" will be the general public, a legal requirement, or the
software developer himself or herself.

A validation action applied to an engineering element includes the
following: - Identification of the element on which the validation
action will be performed. - Identification of the reference that defines
the expected result of the validation action.

Performing the validation action includes the following: - Obtaining a
result by performing the validation action onto the submitted element. -
Comparing the obtained result with the expected result. - Deducing the
degree of compliance of the element. - Deciding on the acceptability of
this compliance, because sometimes the result of the comparison may
require a value judgment to decide whether or not to accept the obtained
result as compared to the relevance of the context of use. (SEBoK)

### References

-   [*\"System
    Validation\", *](https://sebokwiki.org/wiki/System_Validation)[**Systems
    Engineering Body of
    Knowledge**](https://sebokwiki.org/wiki/System_Validation) (this is
    a treasure trove, by the by)

### Continuous Integration

The logical consummation of test-driven development is that *all* code
should be tested *all the time*. Continuous integration services make
this possible by running suites of unit tests on all new code that comes
into the repository.

Essentially, there\'s a hook that gets activated whenever you merge a
pull request or submit commits to the development branch of a
repository. This process runs the suite of test cases you have created
and reports back to you which pass and which fail.

- [GitHub Actions example](https://github.com/actions/starter-workflows/blob/main/ci/python-app.yml)
