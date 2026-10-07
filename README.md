# CI2026_lab2

## Problem
Given N objects (0..N-1) and N subsets, where subset `s` has `s+1` random
elements and a random cost `10*random() + (s + random())^2`, pick a collection
of subsets that covers all N objects at minimum total cost.
I solve it for every N from 1 to 100.

## Approach
Hill climbing, with fitness = minus the total cost of the selected subsets.

1. **Start:** all subsets selected. This is always a valid cover.
2. **Tweak:** pick 1 subset (50%) or 2 subsets (50%) at random and toggle
   each one (add it if absent, remove it if present).
3. **Accept** the new solution only if it is still a valid cover
   (every object covered) and its cost is strictly lower.
4. Repeat for 20,000 steps per N. The seed is fixed (`seed(42)`) so results
   are reproducible.

## Results


| N | cost | selected sets |
|---|------|---------------|
| 10 | (paste from results.csv) | |
| 50 | (paste from results.csv) | |
| 100 | (paste from results.csv) | |

## Observations


## How to run
`pip install matplotlib` then `python lab2.py`
