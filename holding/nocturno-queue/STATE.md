# Proposed addition to nocturno-research STATE.md

Not committed to `joacatar/Nocturno-research` (HTTP 404 with the agent token). Paste this under the queue.

Source: `elder-plinius/V3R1T4S` commit `f3b19b475065f35d0a7f93e8a6078c9b2f12566e` (2026-10-30), "Bank: 660 new known unknowns (1104 in 31 categories)". Picked for exact search in C or Python, OEIS-style checkers, and a laptop. Skipped disease, drug, and ML leaderboards, and skipped `subtraction-game-max-period-terms` because V3R1T4S issue #780 says several of those terms are already published.

| Priority | Bank id | Why it fits | Page |
| --- | --- | --- | --- |
| 1, started | `tiny-tag-busy-beaver-exact` | 2048 strings, exact simulator, published f(1)..f(10) reproduced | https://github.com/elder-plinius/V3R1T4S/blob/f3b19b475065f35d0a7f93e8a6078c9b2f12566e/known-unknowns/graphs-games-automata/tiny-tag-busy-beaver-exact.md |
| 2 | `rectangle-dissections-square-a182275-n13` | Next OEIS term, two independent transfer matrices, tractability 4.5 | https://github.com/elder-plinius/V3R1T4S/blob/f3b19b475065f35d0a7f93e8a6078c9b2f12566e/known-unknowns/recreational-math/rectangle-dissections-square-a182275-n13.md |
| 3 | `no-three-collinear-cube-a399138` | A larger witness is checked in seconds; lower bounds a(7)>=73 through a(11)>=164 | https://github.com/elder-plinius/V3R1T4S/blob/f3b19b475065f35d0a7f93e8a6078c9b2f12566e/known-unknowns/graphs-games-automata/no-three-collinear-cube-a399138.md |
| 4 | `benzel-stones-and-bones-next-terms` | Next term of A364416 or A364417 by a transfer matrix | https://github.com/elder-plinius/V3R1T4S/blob/f3b19b475065f35d0a7f93e8a6078c9b2f12566e/known-unknowns/graphs-games-automata/benzel-stones-and-bones-next-terms.md |
| 5 | `odd-graceful-trees-beyond-12` | Labeling search; a full win needs every tree through 22 vertices or a counterexample | https://github.com/elder-plinius/V3R1T4S/blob/f3b19b475065f35d0a7f93e8a6078c9b2f12566e/known-unknowns/graphs-games-automata/odd-graceful-trees-beyond-12.md |

## Started: tiny-tag-busy-beaver-exact

Status page re-read 2026-10-30: https://wiki.bbchallenge.org/wiki/Tiny_Tag still lists no exact value past n = 10. f(1)..f(10) = 1, 5, 9, 13, 15, 334, 404, 670, 12584, 2180995. An independent ring-buffer simulator reproduced those ten champions on the strings the page names.

Sweep of all 2048 length-11 strings, step cap 50,000,000 (2026-10-30):

- 1152 strings halt. The longest is 890606 steps, initial string `11110100100`.
- 896 strings are still running at 50,000,000 steps. The same 896 were already open at a cap of 2,000,000, so nothing else halted in between.
- This is a lower bound f(11) >= 890606. It is not a claim. The success rule needs a non-halting certificate for every one of the 896. Partial win p3 allows at most 20 holdouts.

No V3R1T4S pull request was opened. The kit requires a three-skeptic panel and an explicit yes for that pull request before a draft goes to `elder-plinius/V3R1T4S`.
