# OEIS edits ready for a logged-in human

Fetched 2026-10-30T17:51:40Z. Each current b-file was the server's synthesized file (no later uploaded terms). This agent cannot log in to OEIS, so nothing was submitted.

Do this for each sequence below:

1. Sign in at https://oeis.org/.
2. Open the sequence and choose Edit.
3. Paste the comment into a `%C` line and the extension into a `%E` line. Keep the existing history.
4. Extend the DATA (`%S` / `%T` / `%U`) with the new terms when they still fit the usual line length. For A396618 the new terms are long; the b-file is the record.
5. On the edit screen, upload the matching `b*.txt` from this folder (Unix LF, last line ends with a newline). The first line is a `#` comment, which OEIS allows.
6. Preview, then submit. OEIS staff approve the edit; it is not live at upload time.

Not prepared, because `joacatar/Nocturno-research` returned HTTP 404 to this token and `STATE.md` could not be read:

- A390394 a(73)..a(103). Live synthesized b-file ends at a(72) = 53.
- A391592. Live synthesized b-file ends at a(54) = 37. The new terms are not in this fork.
- A364132 a(28). Live synthesized b-file ends at a(22) = 52.
- BND Text 2. No target in the V3R1T4S bank matches that name, and the manuscript text is not on this machine.

## A390087 and A390085

These are one computation. https://oeis.org/A390087 and https://oeis.org/A390085.

A390087 comment:

```
a(8) = 39 and a(9) = 48. Witness of length 16 for k = 39: 77, 75, 73, 71, 69, 67, -65, 63, -61, -59, -57, -55, -53, -51, -49, -45. Witness of length 18 for k = 48: 95, 93, 91, 89, 87, 85, 83, -81, 79, -77, -75, -73, -71, -69, -67, -65, -63, -61. Both are irreducible odd zero-sum sets (every nonempty proper subset has nonzero sum). Checked 2026-10-30.
```

A390087 extension:

```
a(8)-a(9) from Joao Tarira, Oct 30 2026
```

A390085 comment:

```
a(31) through a(38) = 7, a(39) through a(47) = 8, and a(48) = 9, from the same witnesses as A390087(8) and A390087(9) and from exhaustive searches that found no smaller index.
```

A390085 extension:

```
a(31)-a(48) from Joao Tarira, Oct 30 2026
```

The one-command checker in `known-knowns/A390087/2026-10-25-joao-tarira-66fe3ad6` on branch `claim/a390087` rechecks the witnesses. Equality for the indices in between rests on the saved exhaustive logs in that package.

## A395265

https://oeis.org/A395265

Comment:

```
a(20) = 56 and a(21) = 62. A 20-mark witness ending at 56 is 0, 1, 2, 3, 8, 11, 14, 16, 20, 24, 29, 31, 36, 40, 43, 46, 50, 54, 55, 56. A 21-mark witness ending at 62 is 0, 1, 2, 3, 8, 12, 17, 19, 23, 27, 30, 35, 37, 40, 43, 49, 52, 56, 60, 61, 62. Every positive difference occurs at most 5 times. Checked 2026-10-30. Minimality is the saved exhaustive search in the research record.
```

Extension:

```
a(20)-a(21) from Joao Tarira, Oct 30 2026
```

Open draft already on V3R1T4S, not an OEIS edit: https://github.com/elder-plinius/V3R1T4S/pull/772

## A396618

https://oeis.org/A396618

Comment:

```
a(22) = 6338072189, a(23) = 20042521382, a(24) = 63380064097, a(25) = 200424655855. Counts of n-digit squares whose proper decimal suffixes are not squares, with 0 counting as a square, matching the OEIS Mathematica program. Two independent counters agreed. Checked against a(1) through a(21) before the new terms were kept.
```

Extension:

```
a(22)-a(25) from Joao Tarira, Oct 30 2026
```

Open draft already on V3R1T4S, not an OEIS edit: https://github.com/elder-plinius/V3R1T4S/pull/760

A390087's open draft: https://github.com/elder-plinius/V3R1T4S/pull/771
