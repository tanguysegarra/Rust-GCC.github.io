## Overview

Thanks again to [Open Source Security, inc](https://opensrcsec.com/) and
[Embecosm](https://www.embecosm.com/) for their ongoing support for this
project.

### Milestone Progress

This month saw a jump in productivity as we went back to a more regular
schedule, after presenting the project's progress at several in-person
conferences in September.

We made great strides on multiple parts of the compiler, with Philip
spending a lot of time improving our type-system and working on geting
closures to work, while Arthur worked on the early name resolving of
macros and on handling more intrinsics.

We had also received a lot of review comments on our v2 version of the
upstream patches, which consumed a lot of our time. We now have a
workflow in place which should help address subsequent reviewsl We now
have a workflow in place which should help address subsequent reviews.
The v3 of the patches, which simply contains these fixes but no new
content, has been sent. More patches will follow to update the compiler
to its current state.

The compilation of libcore is currently blocked by two issues: Macro
importing and exporting, as well as closures. We are working hard on
getting these features in the compiler as soon as possible.

We are planning to spend time on these two features as well as look at
the `#[derive]` builtin macros in order to get closer and closer to
compiling `libcore 1.49` properly.

## Completed Activities

-   AST: dump structs, unions and enums
    [PR1572](https://github.com/rust-gcc/gccrs/pull/1572)
-   Implement data prefetch intrinsics
    [PR1565](https://github.com/rust-gcc/gccrs/pull/1565)
-   builtins: Move implementation into source file
    [PR1564](https://github.com/rust-gcc/gccrs/pull/1564)
-   ast: dump assignment and if expressions
    [PR1563](https://github.com/rust-gcc/gccrs/pull/1563)
-   Support looking up super trait items during path resolution
    [PR1562](https://github.com/rust-gcc/gccrs/pull/1562)
-   Fix -Wunused using \`rust-lang.cc\` hack
    [PR1560](https://github.com/rust-gcc/gccrs/pull/1560)
-   Fix include structure
    [PR1559](https://github.com/rust-gcc/gccrs/pull/1559)
-   testing: try loop in const function
    [PR1554](https://github.com/rust-gcc/gccrs/pull/1554)
-   Dump item visibility
    [PR1547](https://github.com/rust-gcc/gccrs/pull/1547)
-   Reintroduce targetrustm hooks without the maze of macro definitions
    in target headers
    [PR1543](https://github.com/rust-gcc/gccrs/pull/1543)
-   ast: dump TypeAlias
    [PR1593](https://github.com/rust-gcc/gccrs/pull/1593)
-   AST: more dump improvements
    [PR1590](https://github.com/rust-gcc/gccrs/pull/1590)
-   Method resolution must support multiple candidates
    [PR1587](https://github.com/rust-gcc/gccrs/pull/1587)
-   Add missing lang item mappings
    [PR1584](https://github.com/rust-gcc/gccrs/pull/1584)
-   Support type resolution on super traits on dyn objects
    [PR1583](https://github.com/rust-gcc/gccrs/pull/1583)
-   Add early name resolver
    [PR1580](https://github.com/rust-gcc/gccrs/pull/1580)
-   fix ICE on missing closing paren
    [PR1574](https://github.com/rust-gcc/gccrs/pull/1574)
-   Apply \#1560 master
    [PR1570](https://github.com/rust-gcc/gccrs/pull/1570)
-   make: Inherit CXXFLAGS, guard against non g++ compilers for warnings
    [PR1556](https://github.com/rust-gcc/gccrs/pull/1556)
-   Dump module items
    [PR1548](https://github.com/rust-gcc/gccrs/pull/1548)
-   Initial support for closures
    [PR1608](https://github.com/rust-gcc/gccrs/pull/1608)
-   Improve AST Fragment class
    [PR1607](https://github.com/rust-gcc/gccrs/pull/1607)
-   \[33/37\] lang-specs: Rename language spec @rs -\> @rust
    [PR1605](https://github.com/rust-gcc/gccrs/pull/1605)
-   Add check for recursive trait cycles
    [PR1602](https://github.com/rust-gcc/gccrs/pull/1602)
-   \[25/37\] rust-privacy-reporter: Add copyright header
    [PR1599](https://github.com/rust-gcc/gccrs/pull/1599)
-   \[10/37\] rust-cfg-parser: Add copyright header
    [PR1598](https://github.com/rust-gcc/gccrs/pull/1598)
-   ast: Module: unloaded module and inner attributes
    [PR1597](https://github.com/rust-gcc/gccrs/pull/1597)
-   Add more implementations for TARGET<sub>RUSTOSINFO</sub>
    [PR1596](https://github.com/rust-gcc/gccrs/pull/1596)
-   Support outer attribute handling on trait items just like normal
    items [PR1595](https://github.com/rust-gcc/gccrs/pull/1595)
-   Refactor TraitResolver to not require a visitor
    [PR1594](https://github.com/rust-gcc/gccrs/pull/1594)
-   Dump macro declarations properly
    [PR1549](https://github.com/rust-gcc/gccrs/pull/1549)
-   intrinsics: Use lambdas for wrapping\_\<op\> intrinsics
    [PR1621](https://github.com/rust-gcc/gccrs/pull/1621)
-   Intrinsics unchecked ops
    [PR1620](https://github.com/rust-gcc/gccrs/pull/1620)
-   parser: Fix ICE in closure parsing
    [PR1619](https://github.com/rust-gcc/gccrs/pull/1619)
-   Add missing copyright headers
    [PR1618](https://github.com/rust-gcc/gccrs/pull/1618)
-   Apply \#1605 on master (fix lang spec)
    [PR1617](https://github.com/rust-gcc/gccrs/pull/1617)
-   Apply 1559 master (remove system includes)
    [PR1616](https://github.com/rust-gcc/gccrs/pull/1616)
-   intrinsics: Add early implementation for atomic<sub>storeseqcst,
    relaxed, release</sub>
    [PR1615](https://github.com/rust-gcc/gccrs/pull/1615)
-   intrinsics: Add rust<sub>sorry</sub> wrapper for unimplemented
    intrinsics [PR1614](https://github.com/rust-gcc/gccrs/pull/1614)
-   builtins: Rename all bang macro handlers
    [PR1613](https://github.com/rust-gcc/gccrs/pull/1613)
-   Apply \#1556 on master
    [PR1585](https://github.com/rust-gcc/gccrs/pull/1585)

### Contributors this month

-   [Iain Buclaw](https://github.com/ibuclaw)
-   [David Faust](https://github.com/dafaust)
-   [Faisal Abas](https://github.com/abbasfaisal)
-   [Marc Poulhiès](https://github.com/dkm)
-   [Jakub Dupak](https://github.com/jdupak)

### Overall Task Status

| Category    | Last Month | This Month | Delta |
|-------------|------------|------------|-------|
| TODO        | 168        | 180        | +12   |
| In Progress | 28         | 31         | +3    |
| Completed   | 466        | 482        | +16   |

### Test Case

| TestCases | Last Month | This Month | Delta |
|-----------|------------|------------|-------|
| Passing   | 6794       | 6948       | +154  |
| Failed    | \-         | \-         | \-    |
| XFAIL     | 52         | 52         | \-    |
| XPASS     | \-         | \-         | \-    |

### Bugs

| Category    | Last Month | This Month | Delta |
|-------------|------------|------------|-------|
| TODO        | 51         | 56         | +5    |
| In Progress | 14         | 16         | +2    |
| Completed   | 210        | 214        | +4    |

### Milestones Progress

We have added milestones to better reflect the GCC merging cycle. More
milestones will be put together as more themes of work are discovered
along the year. We have closed out the `Const Generics` milestone, as it
is in a sufficiently complete state for `libcore-1.49` compilation.
Nonetheless, some const generics features are missing, and have been
added to a separate `Const Generics 2` project.

Note that the intrinsics milestone percentage on github is not
representative: It shows a 66% completion rate, but does not take into
account the tracking issues with dozens of unresolved items. Thus the
percentage is computed using the sum of issues and tracked items done
divided by the sums of issues and tracked items overall.

| Milestone                         | Last Week | This Week | Delta | Start Date     | Completion Date | Target        |
|-----------------------------------|-----------|-----------|-------|----------------|-----------------|---------------|
| Data Structures 1 - Core          | 100%      | 100%      | \-    | 30th Nov 2020  | 27th Jan 2021   | 29th Jan 2021 |
| Control Flow 1 - Core             | 100%      | 100%      | \-    | 28th Jan 2021  | 10th Feb 2021   | 26th Feb 2021 |
| Data Structures 2 - Generics      | 100%      | 100%      | \-    | 11th Feb 2021  | 14th May 2021   | 28th May 2021 |
| Data Structures 3 - Traits        | 100%      | 100%      | \-    | 20th May 2021  | 17th Sept 2021  | 27th Aug 2021 |
| Control Flow 2 - Pattern Matching | 100%      | 100%      | \-    | 20th Sept 2021 | 9th Dec 2021    | 29th Nov 2021 |
| Macros and cfg expansion          | 100%      | 100%      | \-    | 1st Dec 2021   | 31st Mar 2022   | 28th Mar 2022 |
| Imports and Visibility            | 100%      | 100%      | \-    | 29th Mar 2022  | 13th Jul 2022   | 27th May 2022 |
| Const Generics                    | 76%       | 100%      | +24%  | 30th May 2022  | 10th Oct 2022   | 17th Oct 2022 |
| Intrinsics and builtins           | 15%       | 18%       | +3%   | 6th Sept 2022  | \-              | 14th Nov 2022 |
| Initial upstream patches          | 0%        | 83%       | +83%  | 10th Oct 2022  | \-              | 13th Nov 2022 |
| Final set of upstream patches     | 0%        | 6%        | +6%   | 16th Nov 2022  | \-              | 30th Apr 2023 |
| Borrow checking                   | 0%        | 0%        | \-    | TBD            | \-              | TBD           |
| Const Generics 2                  | 0%        | 0%        | \-    | TBD            | \-              | TBD           |

### Risks

| Risk                           | Impact (1-3) | Likelihood (0-10) | Risk (I \* L) | Mitigation                                     |
|--------------------------------|--------------|-------------------|---------------|------------------------------------------------|
| Missing GCC 13 upstream window | 2            | 3                 | 6             | Merge in GCC 14 and be proactive about reviews |

### Testing project

| Testsuite                           | Compiler            | Last month | This month | Success delta |
|-------------------------------------|---------------------|------------|------------|---------------|
| rustc testsuite                     | gccrs -fsyntax-only | 82.1%      | 82.2%      | +0.1%         |
| gccrs testsuite                     | rustc stable        | 64.5%      | 64.2%      | -0.1%         |
| rustc testsuite passing tests       | gccrs               | 12.6%      | 12.3%      | -0.3%         |
| rustc testsuite (no<sub>std</sub>)  | gccrs               | 28.0%      | 27.6%      | -0.4%         |
| rustc testsuite (no<sub>core</sub>) | gccrs               | 83.3%      | 33.3%      | -50.0%        |
| blake3                              | gccrs               | 25.0%      | 25.5%      | \-            |
| libcore                             | gccrs               | 0%         | 0%         | \-            |

## Planned Activities

-   Finish closure support
-   Finish builtin macro name resolution support
-   Implement remaining intrinsics
-   Finish patch upstreaming

## Detailed changelog

### Macro expansion and name resolution

If you are not familiar with the concept of name resolution, I would
recommend starting by reading parts of the macro expansion and name
resolution chapters of the Rust compiler development guide:

1.  [Name
    Resolution](https://rustc-dev-guide.rust-lang.org/name-resolution.html)
2.  [Macro Name
    Resolution](https://rustc-dev-guide.rust-lang.org/macro-expansion.html#name-resolution)

Macros needing to be name resolved is one of the reasons why name
resolution happens at the AST level: Because macros expand to new
fragments of AST, and need to be expanded before further compiler
passes, we need to be able to refer a macro invocation to its
definition.

This includes resolving "simple" examples such as the following:

``` rust
macro_rules! a { () => () };

a!();

macro_rules! a { (now_with_more_tokens) => () };

a!(now_with_more_tokens);
```

or more complex ones involving imports:

``` rust
use lazy_static::lazy_static as the_famous_lazy_macro;

the_famous_lazy_macro! {
    static ref A: i32 = 15;
}
```

However, it does not make sense to perform a "full" name resolution at
this point: macro expansion will generate new tokens, which could then
benefit from a later resolution. Furthermore, the macro lexical scope is
quite simple compared to the type scope of name scope and has slightly
different rules. This explains why name resolution is "split in two" in
`rustc`: One part takes care of resolving macro invocations and imports,
and the other takes care of resolving types, variables, function calls…

From this point onward, we will refer to the `Early Name Resolution` as
the pass responsible for resolving imports and macro invocations, and to
`Name Resolution` as the later pass.

Up until the month of October, our macro expander performed macro name
resolution whenever a macro invocation required expansion. This worked
fine in practice, even for complex cases, but made it difficult to
expand with proper name resolution rules or imports. Adding
functionality such as `#[macro_export]` and `#[macro_import]` on top of
it would prove to be too difficult, so we chose to split up the name
resolution pass away from the expansion pass.

1.  A new expansion system

    To take care of macro and import name resolution, we have
    implemented a new `EarlyNameResolver` visitor which takes care of
    tying a macro invocation to its rules definition. The previous
    system worked recursively and expanded as many macros as it could in
    one place, but it was difficult to integrate the `EarlyNameResolver`
    within that system, which was starting to be hard to maintain and
    very complex.

    We have thus switched over to a fixed-point algorithm for resolving
    and expanding macros: we run the early name resolver, run the macro
    expander, check if anything has changed, and do it again.

    Let's look at an example of how the two systems differ, given this
    piece of code, and assuming that all these macro invocations expand
    to their input.

    ``` rust
    fn main() {
        foo!(bar!(baz!(let v = 15)));

        a!(b!(a_fn_call()));
    }
    ```

    1.  Previous system

    ``` rust
    fn main() {
        // recursively expand this invocation for as long as possible
        foo!(bar!(baz!(let v = 15)));

        a!(b!(a_fn_call()));
    }

    // into...

    fn main() {
        bar!(baz!(let v = 15));

        a!(b!(a_fn_call()));
    }

    // into...

    fn main() {
        baz!(let v = 15);

        a!(b!(a_fn_call()));
    }

    // into...

    fn main() {
        let v = 15;

        a!(b!(a_fn_call()));
    }

    // into...

    fn main() {
        let v = 15;

        // now this invocation
        a!(b!(a_fn_call()));
    }

    // into...

    fn main() {
        let v = 15;

        b!(a_fn_call());
    }

    // into...


    fn main() {
        let v = 15;

        a_fn_call();
    }

    // done!
    ```

    1.  Fixed-point fashion

    ``` rust
    fn main() {
        // expand each invocation *once* as we go through the crate

        foo!(bar!(baz!(let v = 15)));

        a!(b!(a_fn_call()));
    }

    // into...

    fn main() {
        bar!(baz!(let v = 15));

        b!(a_fn_call());
    }

    // into...

    fn main() {
        baz!(let v = 15);

        a_fn_call();
    }

    // into...

    fn main() {
        let v = 15;

        a_fn_call();
    }

    // done!
    ```

    The code responsible for performing this dance looks a bit like the
    following.

    ``` cpp
    auto enr = EarlyNameResolver();
    auto expander = MacroExpander();

    do {
        enr.go(crate);
        expander.go(crate);
    } while (expander.has_changed() && !recursion_limit_reached());
    ```

    It's a really simple and robust system, which helps clean up the
    code a lot.

2.  The problem

    Sadly, this system is not without flaw. As you may know, not all
    Rust macros can be expanded lazily!

    ``` rust
    macro_rules! gives_literal { () => ("literal!") }

    macro_rules! fake_concat {
        ($a:literal, $b:literal) => { concat!($a, $b); }
    }

    fn main() {
        let a = concat!("a ", gives_literal!()); // builtin macro, this is fine
        let b = fake_concat!("a ", gives_literal!()); // error!
    }
    ```

    …and this is the one remaining feature that the fixed-point system
    has to be able to deal with before we integrate it into the
    compiler, hopefully soon!

### Mapping intrinsics to GCC builtins

`gccrs` differs between two kinds of intrinsics:

1.  Those who map directly to GCC builtins, such as `sqrtf32` which can
    be replaced with a call to `__builtin_sqrtf`
2.  Those who require the creation of a function block and which might
    take generic arguments

A nice and short example is the handling of the `copy_nonoverlapping`
intrinsic, whose declaration is as follows:

``` rust
pub fn copy_nonoverlapping<T>(src: *const T, dst: *mut T, count: usize);
```

[The documentation for that
intrinsic](https://doc.rust-lang.org/core/intrinsics/fn.copy_nonoverlapping.html)
informs us that it is equivalent to a `memcpy` in C, with the argument
order swapped. Furthermore, the `count` parameter refers to the number
of values to copy, not the amount of bytes. We can thus make use of
GCC's `__builtin_memcpy` to create the following function block:

``` rust
pub fn copy_nonoverlapping<T>(src: *const T, dst: *mut T, count: usize) {
    __builtin_memcpy(dst, src, count * size_of::<T>());
}
```

We do similar things for a lot of Rust intrinsics and have recently
encountered some fun limitations.

1.  data prefetch intrinsics

    Two data prefetch intrinsics exist in Rust,
    `core::intrinsics::prefetch_read_data` and
    `core::intrinsics::prefetch_write_data`. These functions are generic
    over a type parameter `T`, and take as argument a pointer to that
    type `T`. An extra argument is the `locality`, which refers to a
    value between 0 and 3 indicating how local the data should be kept
    cache-wise.

    This maps quite nicely to GCC's `__builtin_prefetch`, whose
    "declaration" would look like the following:

    ``` c
    void __builtin_prefetch(const void *addr, int rw, int locality);
    ```

    The function blocks seem quite easy to create:

    ``` rust
    pub fn prefetch_read_data<T>(data: *const T, locality: i32) {
        __builtin_prefetch(data, 0 /* read */, locality);
    }

    pub fn prefetch_write_data<T>(data: *const T, locality: i32) {
        __builtin_prefetch(data, 1 /* write */, locality);
    }
    ```

    but an error arises when trying to compile them. For its locality
    argument, `__builtin_prefetch` expects a compile time constant,
    which it cannot reliably get from the function's argument. This
    causes a verification pass in our gimplification (a lowering pass in
    GCC's middle-end) to throw an error and fail the compilation.

    Interestingly, a similar limitation is present with `rustc` and
    `LLVM`, [but will appear further down the compilation
    pipeline](https://play.rust-lang.org/?version=nightly&mode=debug&edition=2021&gist=8012b1bf794c73b4038f62d4922179aa).

    This is no-doubt due to our lack of proper constant folding: GCC is
    able to tell that a call to `prefetch_read_data(addr, 3)` is valid
    and contains a compile-time constant, but we simply do not yet give
    it the possiblity. Thanks to this year GSOC's student [Faisal
    Abbas](https://github.com/abbasfaisal), we should be able to hook
    into that constant evaluator and try to extract a constant value if
    possible.

    If intrinsics piqued your interest, feel free to come on our Zulip
    channel and discuss the work left to be done. There are plenty to
    implement and we'd love the extra help!
