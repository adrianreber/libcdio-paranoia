10.2+2.0.2
----------
2024-05-07

- A 6-year-old bug, seen primarily by Whipper users, concerning
  adjusting of CD-drives that have large sample offsets, or negative
  offsets has been fixed.  Fix is from and thanks are due to
  buddyabaddon.
  https://github.com/rocky/libcdio-paranoia/issues/14 and
  https://github.com/rocky/libcdio-paranoia/pull/38
- Code has moved from savannah.gnu.org to github. CircleCI
  testing is now incorporated into builds.
- Add test on LSN on span check errors, and give a better
  message when there is a problem. https://github.com/rocky/libcdio-paranoia/pull/39
- Require libcdio at least 2.0.0
- Remove dead code after exit. https://github.com/rocky/libcdio-paranoia/pull/32
- Fix manpage for Japanese. https://github.com/rocky/libcdio-paranoia/pull/27
- Add notes for using gmake for building on FreeBSD. https://github.com/rocky/libcdio-paranoia/pull/26


10.2+2.0.1
----------
2019-09-16

- cdda toc routines now included (fixes #21)
- "make distcheck" broken in 2.0.0 works properly again
- Remove some gcc/clang warnings


10.2+2.0.0
----------
2019-01-26

  This work was done by Edd Barrett and Thomas Schmitt
- OpenBSD tolerance
- typos in manual page and README
- Do not attempt to call a NULL callback (issue #15) from mskamp
- Switch to semantic versioning number in libcdio portion and match
  up with libcdio version

10.2+0.94+2
-----------
2017-08-22

- Add `--force-overread`
  Force overreading into the lead-out portion of the disc. This option
  is only applicable when using the `-O` option with a positive sample
  offset value. Many drives are not capable of reading into this
  portion of the disc and attempting to do so on those drives will
  produce read errors and possibly hard lockups

10.2+0.94+1
-----------
2017-03-25

- Fix problem where end of span seems to default to last track. Savannah bug 43444
- Fix NULL pointer dereference that occurs when byte swapping is
  needed. MR #4
- Re-silence recently added gcc -Wunused-result warnings
- Use `@LIBS@` figured out by autoconf when linking (for `-lrt` on Linux).
- Incorrect track was getting used in matching. See
  Savannah bug 49831 and MR #7, #8 and #10

10.2+0.93+1
-----------
2014-09-29

- Add `cdio_cddap_free_messages` function
- Start using Coverty Static analysis
- Update OS versions we recognize
- Upgrade libcdio-paranoia to paranoia version 10.2
- Bug fixes on MS Windows and other bug fixes
- Redo license so everything is GPL3

10.2+0.90
---------
2012-12-24

Split off from libcdio to allow more flexible licensing and to be compatible
with cdparanoia-III-10.2's license. And also, libcdio is just too large.
