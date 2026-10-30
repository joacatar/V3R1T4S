# Pull request to dronperminov/FastMatrixMultiplication

Not opened. `cursor[bot]` received `403` on `POST /repos/dronperminov/FastMatrixMultiplication/forks` and `Permission denied` on push.

After Joao forks the repository:

```
git clone --depth 1 https://github.com/joacatar/FastMatrixMultiplication.git
cp 4x6x10_m175_cr637_cn2004_ZT_reduced.json 8x8x8_m343_cr1332_cn7482_ZT_reduced.json \
  schemes/results/addition_reduced_ZT/
git switch -c adds-kron-8x8x8-4x6x10
git add schemes/results/addition_reduced_ZT/4x6x10_m175_cr637_cn2004_ZT_reduced.json \
        schemes/results/addition_reduced_ZT/8x8x8_m343_cr1332_cn7482_ZT_reduced.json
git commit -m "Add 1332- and 637-addition evaluations of 8x8x8:343 and 4x6x10:175"
git push -u origin adds-kron-8x8x8-4x6x10
gh pr create --repo dronperminov/FastMatrixMultiplication --title "$(head -1 TITLE.txt)" --body-file BODY.md
```

## Title

Add 1332-addition and 637-addition evaluations of the 8x8x8:343 and 4x6x10:175 ternary schemes

## Body

Adds two reduced evaluations of existing best ternary ranks. Ranks are unchanged. No optimality and no runtime speedup is claimed.

| Format | Rank | Previous reduced additions | This evaluation | U / V / W | Naive |
| --- | ---: | ---: | ---: | --- | ---: |
| 8x8x8 | 343 | 1410 (`8x8x8_m343_cr1410_cn4434_ZT_reduced.json`) | 1332 | 351 / 351 / 630 | 7482 |
| 4x6x10 | 175 | 677 (`4x6x10_m175_cr677_cn1878_ZT_reduced.json`) | 637 | 129 / 207 / 301 | 2004 |

Construction: Kronecker composition of the straight-line programs, Winograd `2x2x2_m7_cr15` (4+4+7 additions) with `4x4x4_m49_cr156` and with `2x3x5_m25_cr69` (`cn111`, 15+21+33). Block additions cost `n2*m2`, `m2*p2` and `n2*p2` respectively, which gives `7*156 + 15*16 = 1332` and `7*69 + 4*6 + 4*15 + 7*10 = 637`.

Validation on master as of 2026-10-30:

- `Scheme.load(path, validate=True)` accepts both files (full Brent identity over Z).
- The same reduced-addition counter used in this repository, `sum(max(0, len(form)-1))` over fresh and final forms, returns the splits above, and returns 1410 and 677 on the current files.
- 6x12x14 is not included. The live best rank is 645 over Q (`fmm_sota.json`) and 654 over ZT/Z (`docs/ranks.md`). An open pull request already proposes a ZT rank-654 scheme.

Credits: A. I. Perminov (the reduced format, the counting convention, and the 1410 and 677 evaluations); Winograd's `<2,2,2>:7`. The inner schemes are the published `cr156` and `cr69` files in this repository.
