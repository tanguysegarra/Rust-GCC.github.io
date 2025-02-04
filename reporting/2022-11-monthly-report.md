## Overview

Thanks again to [Open Source Security, inc](https://opensrcsec.com/) and
[Embecosm](https://www.embecosm.com/) for their ongoing support for this
project.

### Milestone Progress

Most of the work this month was focused on fixing the reviews we
received on the patches. We spent quite a lot of time organizing them
differently, making the fixes, and then applying those fixes to the
proper patches. The v4 of the patchset will be sent on the mailing list
soon.

The compilation of libcore is still blocked by the same two issues:
Macro importing and exporting, as well as closures. With the work on
patches, we are finding very little time to add new features to the
compiler but will get back to it as soon as possible.

We are still planning to complete these two issues as well as look at
the `#[derive]` builtin macros.

We are also preparing abstracts in the hope of giving two talks at
[FOSDEM](https://fosdem.org/2023/) in February. You should also expect a
blog-post from us on the [Rust Foundation's
website](https://foundation.rust-lang.org/) in the coming weeks.

As a side-note, Arthur will be on vacation the second half of December,
starting on the 19th.

### Community call

We will be having our monthly community call on the 12th of December at
10h00 UTC.

-   Date/Time: 12th December 2022 at: 10h00 UTC
-   Mailing list: <https://gcc.gnu.org/mailman/listinfo/gcc-rust>
-   Zulip: <https://gcc-rust.zulipchat.com/>
-   IRC: irc.oftc.net \#gccrust
-   Video Link: <https://meet.jit.si/gccrs-community-call-december>

Agenda: <https://hackmd.io/@Rust-GCC/Syy1hUDvi>

You can subscribe to our newly-created Google calendar to get updates
and the dates of events the team will attend.

-   Calendar ID:
    7060a0923ffebd3cb52b1afef35a28ff7b64f05962c9af84c23b1847f1f5f894@group.calendar.google.com
-   [Google calendar
    link](https://calendar.google.com/calendar/embed?src=7060a0923ffebd3cb52b1afef35a28ff7b64f05962c9af84c23b1847f1f5f894%40group.calendar.google.com&ctz=Europe%2FParis)
-   [iCal
    link](https://calendar.google.com/calendar/ical/7060a0923ffebd3cb52b1afef35a28ff7b64f05962c9af84c23b1847f1f5f894%40group.calendar.google.com/public/basic.ics)

## Completed Activities

-   Fix regressions in 32 bit mode and gcc4.8 builds
    [PR1676](https://github.com/rust-gcc/gccrs/pull/1676)
-   just for fun [PR1672](https://github.com/rust-gcc/gccrs/pull/1672)
-   'rust-warn += -Wno-unused-parameter'
    [PR1670](https://github.com/rust-gcc/gccrs/pull/1670)
-   builtins: Remove unused parameter
    [PR1668](https://github.com/rust-gcc/gccrs/pull/1668)
-   8e52e414f40b: Fix merge issue
    [PR1664](https://github.com/rust-gcc/gccrs/pull/1664)
-   dwarf2out.c: Don't emit DW<sub>LANGRustold</sub>
    [PR1663](https://github.com/rust-gcc/gccrs/pull/1663)
-   48fa248760da: Simplify get<sub>nthcallarg</sub>
    [PR1662](https://github.com/rust-gcc/gccrs/pull/1662)
-   58e75f65e56d: Remove HOST<sub>WIDEINT</sub> struct member
    [PR1661](https://github.com/rust-gcc/gccrs/pull/1661)
-   Use \`wide<sub>inttotree</sub>\` instead of
    \`double<sub>inttotree</sub>\`
    [PR1660](https://github.com/rust-gcc/gccrs/pull/1660)
-   8e52e414f40b: Use build<sub>intcstu</sub> for size expressions
    [PR1659](https://github.com/rust-gcc/gccrs/pull/1659)
-   ci: Remove warning checks on gcc-patch-dev
    [PR1657](https://github.com/rust-gcc/gccrs/pull/1657)
-   No fold after convert to
    [PR1656](https://github.com/rust-gcc/gccrs/pull/1656)
-   gcc-patch-dev: Add CI to patch branch
    [PR1655](https://github.com/rust-gcc/gccrs/pull/1655)
-   Release \`mpz<sub>t</sub>\` values properly
    [PR1653](https://github.com/rust-gcc/gccrs/pull/1653)
-   AST dump types [PR1652](https://github.com/rust-gcc/gccrs/pull/1652)
-   Improve dump lex
    [PR1651](https://github.com/rust-gcc/gccrs/pull/1651)
-   dwarf2out.c: Don't emit DW<sub>LANGRustold</sub>
    [PR1649](https://github.com/rust-gcc/gccrs/pull/1649)
-   Add location to AST::Visibility
    [PR1636](https://github.com/rust-gcc/gccrs/pull/1636)
-   rust: Remove unused variables and fix dangling ref…
    [PR1635](https://github.com/rust-gcc/gccrs/pull/1635)
-   Implement PhantomData
    [PR1633](https://github.com/rust-gcc/gccrs/pull/1633)
-   Fix mac-os regression in apply generic arguments t…
    [PR1632](https://github.com/rust-gcc/gccrs/pull/1632)
-   Ast dump where clause
    [PR1631](https://github.com/rust-gcc/gccrs/pull/1631)
-   Cleanup builtin handling
    [PR1630](https://github.com/rust-gcc/gccrs/pull/1630)
-   typecheck: Fix overzealous \`delete\` call
    [PR1628](https://github.com/rust-gcc/gccrs/pull/1628)
-   Ast dump unit struct
    [PR1625](https://github.com/rust-gcc/gccrs/pull/1625)
-   Ast dump refactor
    [PR1624](https://github.com/rust-gcc/gccrs/pull/1624)
-   Initial state capture for closures
    [PR1611](https://github.com/rust-gcc/gccrs/pull/1611)

### Contributors this month

-   [Marc Poulhiès](https://github.com/dkm)
-   [Jakub Dupak](https://github.com/jdupak)
-   [tamaron](https://github.com/tamaroning)
-   [Dave Evans](https://github.com/dme2)
-   [Thomas Schwinge](https://github.com/tschwinge)

### Overall Task Status

| Category    | Last Month | This Month | Delta |
|-------------|------------|------------|-------|
| TODO        | 180        | 183        | +3    |
| In Progress | 31         | 31         | \-    |
| Completed   | 482        | 499        | +17   |

### Test Case

| TestCases | Last Month | This Month | Delta |
|-----------|------------|------------|-------|
| Passing   | 6948       | 6976       | +28   |
| Failed    | \-         | \-         | \-    |
| XFAIL     | 52         | 52         | \-    |
| XPASS     | \-         | \-         | \-    |

### Bugs

| Category    | Last Month | This Month | Delta |
|-------------|------------|------------|-------|
| TODO        | 56         | 55         | -1    |
| In Progress | 16         | 16         | \-    |
| Completed   | 214        | 218        | +4    |

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
| Const Generics                    | 100%      | 100%      | \-    | 30th May 2022  | 10th Oct 2022   | 17th Oct 2022 |
| Initial upstream patches          | 83%       | 100%      | +17%  | 10th Oct 2022  | 13th Nov 2022   | 13th Nov 2022 |
| Upstream initial patchset         | 0%        | 78%       | +78%  | 13th Nov 2022  | \-              | 19th Dec 2022 |
| Final set of upstream patches     | 6%        | 20%       | +14%  | 16th Nov 2022  | \-              | 30th Apr 2023 |
| Intrinsics and builtins           | 18%       | 18%       | \-    | 6th Sept 2022  | \-              | TBD           |
| Borrow checking                   | 0%        | 0%        | \-    | TBD            | \-              | TBD           |
| Const Generics 2                  | 0%        | 0%        | \-    | TBD            | \-              | TBD           |
| Rust-for-Linux compilation        | 0%        | 0%        | \-    | TBD            | \-              | TBD           |

### Risks

| Risk                           | Impact (1-3) | Likelihood (0-10) | Risk (I \* L) | Mitigation                                     |
|--------------------------------|--------------|-------------------|---------------|------------------------------------------------|
| Missing GCC 13 upstream window | 2            | 3                 | 6             | Merge in GCC 14 and be proactive about reviews |

### Testing project

| Testsuite                           | Compiler            | Last month | This month | Success delta |
|-------------------------------------|---------------------|------------|------------|---------------|
| rustc testsuite                     | gccrs -fsyntax-only | 82.2%      | 82.2%      | \-            |
| gccrs testsuite                     | rustc stable        | 64.2%      | 64.1%      | -0.1%         |
| rustc testsuite passing tests       | gccrs               | 12.3%      | 12.3%      | \-            |
| rustc testsuite (no<sub>std</sub>)  | gccrs               | 27.6%      | 27.6%      | \-            |
| rustc testsuite (no<sub>core</sub>) | gccrs               | 33.3%      | 33.3%      | \-            |
| blake3                              | gccrs               | 25.5%      | 25.5%      | \-            |
| libcore                             | gccrs               | 0%         | 0%         | \-            |

## Planned Activities

-   Finish closure support
-   Finish builtin macro name resolution support
-   Implement remaining intrinsics
-   Finish patch upstreaming

## Detailed changelog
