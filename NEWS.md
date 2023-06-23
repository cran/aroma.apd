# Version 0.7.0 (2023-06-21)

## Miscellaneous

 * Importing `throw()` from **R.oo** instead of **R.methodsS3**.


# Version 0.6.1 (2022-07-17)

## Miscellaneous

 * Fix unnecessary escape of underscores (`_`) in Rd files.


# Version 0.6.0 (2015-02-24)

## Miscellaneous

 * Added package tests (from examples).

 * Importing suggested functions using `::`.

 * Declaring all S3 methods.

 * Bumped package dependencies.


# Version 0.5.0 (2014-02-25)

## Miscellaneous

 * Bumped up package requirements.


# Version 0.4.1 (2014-01-05)

## New features

 * Now `celToApd()` throws a more informative error message if it
   fails to located an APD map file.

 * Now the `aroma.apd` `Package` object is also available when the
   package is only loaded (but not attached).

 * Now `writeApd()` is atomic, which is achieved by first writing to a
   temporary file which is then renamed upon completion.

## Bug fixes

 * `celToApd()` assumed that **affxparser** was already attached.

## Miscellaneous

 * Removed unnecessary import statements from NAMESPACE.

 * Some of the examples assumed that the suggested **affxparser** was
   installed and attached.

 * Bumped up package version requirements.


# Version 0.4.0 (2013-09-21)

## Bug fixes

 * `cdfToApdMap()` did not validate and assign argument `verbose`.

 * Forgot to import `trim()` from **R.oo**.

## Miscellaneous

 * Removed fallback attachments of **R.utils** and **R.huge** as these
   are no longer needed with **R.oo** (>= 1.15.1).

 * Package no longer utilizes `import()`, only `importFrom()`:s.

 * Now only using `Authors@R` in DESCRIPTION, which is possible since
   R (>= 2.14.0).

 * Dropped obsolete R (< 2.0.0) code that was never used.



# Version 0.3.0 (2013-08-02)

## Significant changes

 * Package no longer attaches/loads **R.utils** and **R.huge** (only
   imports them).  However, they will be attached dynamically, when
   certain methods are called.

 * Utilizing new `startupMessage()` of **R.oo**.

## Bug fixes

 * Several functions incorrectly assumed that the **affxparser**
   package had been attached ("loaded").  Although this is almost
   always the case, because this package is only used by
   **aroma.affymetrix**, which loads **affxparser**, this was an
   incorrect assumption.


# Version 0.2.5 (2013-05-25)

## Miscellaneous

 * Minor speedup by replacing `rm()` calls with NULL assignments.


# Version 0.2.4 (2013-05-22)

## Miscellaneous

 * CRAN POLICY: Now all Rd ` \usage{}` lines are at most 90 characters
   long.


# Version 0.2.3 (2012-06-30)

## Miscellaneous

 * Updated package dependencies.


# Version 0.2.2 (2012-04-04)

 * Now package only imports **R.methodsS3**.


# Version 0.2.1 (2012-04-01)

## Miscellaneous

 * Now package no longer gives an `R CMD check` NOTE that
   `.onAttach()` tries to load the **affxparser** package.


# Version 0.2.0 (2011-07-23)

## Miscellaneous

 * Now the package depends on **R.huge** v0.3.0, which now also has a
   namespace.


# Version 0.1.9 (2011-02-20)

## New features

 * Now this package will try to install **affxparser**, if missing and
   in interactive mode.


# Version 0.1.8 (2011-01-31)

## New features

 * Using `packageStartupMessage()` instead of `cat()`.


# Version 0.1.7 (2009-10-16)

## Bug fixes

 * Fixed a few broken Rd links to the **affxparser** package.


# Version 0.1.6 (2009-06-11)

## Miscellaneous

 * Made it explicit in the title and the description that this package
   should now be considered deprecated.


# Version 0.1.5 (2009-05-16)

## New features

 * Updated `{read|update|write}Apd()` to coerce argument `writeMap` to
   integer indices.  `readApd()` also coerce argument `indices` to the
   same.  Before it used to coerce to doubles, if using **R.utils**
   v1.1.4 or before.  These updates should make no difference to
   anyone.  The main purpose is just to use `Arguments$getIndices()`
   instead of `Arguments$getNumerics()` where ever possible.

## Bug fixes

 * Fixed a syntax error in one Rdoc comment.

## Miscellaneous

 * Renamed the file HISTORY (this one) to NEWS.


# Version 0.1.4 (2007-05-24)

## New features

 * Added a namespace to the package.


# Version 0.1.3 (2006-06-19)

## Bug fixes

 * Forgot to use `autoload("setMethodS3", package="R.oo")`, etc.
   Package would not install on Linux.


# Version 0.1.2 (2006-03-18)

## New features

 * Added `updateApdUnits()`.

 * Now all probe indices are not longer zero-based but one-based.
   However, there is still an option to change this to zero-based
   indices again by using argument `indexOffset = 0`.  This option
   might be remove in the future, because zero-based indices are
   really confusing in R.


# Version 0.1.1 (2006-03-14)

## New features

 * There is now a quite large set of methods to process APD files.

 * All of the methods to re-arrange CDF structures and to create
   cell-index maps have been moved to the **affxparser** package.


# Version 0.1.0 (2006-02-23)

 * Created.
