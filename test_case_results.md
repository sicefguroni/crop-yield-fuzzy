# Fuzzy Logic Test Case Results

This file mirrors the 20 test cases used in `fuzzy-logic.ipynb` and records the current model outputs.

## Accuracy Summary

- Matched cases: 17/20
- Mismatched cases: 3/20
- Accuracy: 85.0%

## Test Case Matrix

| Case | Category | Rainfall | Temperature | Soil Moisture | Soil Nutrients | Expected Yield | Predicted Yield | Predicted Value (tons/hectare) | Top Rule | Rule Strength | Status |
| --- | --- | ---: | ---: | ---: | ---: | --- | --- | ---: | ---: | ---: | --- |
| 1 | Happy Path | 100 | 28 | 65 | 60 | High | High | 3.99 | 68 | 0.40 | Match |
| 2 | Happy Path | 120 | 26 | 70 | 58 | High | High | 3.97 | 71 | 0.40 | Match |
| 3 | Happy Path | 150 | 27 | 68 | 62 | High | Very High | 4.31 | 71 | 0.36 | Mismatch |
| 4 | Happy Path | 180 | 25 | 72 | 55 | High | High | 3.69 | 71 | 0.44 | Match |
| 5 | Happy Path | 200 | 29 | 66 | 88 | Very High | Very High | 4.10 | 69 | 0.36 | Match |
| 6 | Happy Path | 220 | 24 | 75 | 90 | Very High | Very High | 4.14 | 72 | 0.50 | Match |
| 7 | Happy Path | 250 | 26 | 70 | 85 | Very High | Very High | 4.42 | 72 | 0.40 | Match |
| 8 | Edge Cases | 0 | 45 | 5 | 20 | Very Low | Very Low | 0.55 | 19 | 0.60 | Match |
| 9 | Edge Cases | 10 | 43 | 8 | 22 | Very Low | Very Low | 0.56 | 19 | 0.56 | Match |
| 10 | Edge Cases | 5 | 44 | 6 | 18 | Very Low | Very Low | 0.54 | 19 | 0.64 | Match |
| 11 | Edge Cases | 300 | 25 | 100 | 25 | Very Low | Very Low | 0.58 | 70 | 0.50 | Match |
| 12 | Edge Cases | 280 | 24 | 98 | 40 | Low | Medium | 2.73 | 71 | 0.60 | Mismatch |
| 13 | Edge Cases | 320 | 26 | 100 | 15 | Very Low | Very Low | 0.53 | 70 | 0.70 | Match |
| 14 | Edge Cases | 15 | 42 | 10 | 20 | Very Low | Very Low | 0.55 | 19 | 0.60 | Match |
| 15 | Stress Test | 150 | 40 | 80 | 65 | Medium | Medium | 3.00 | 80 | 0.40 | Match |
| 16 | Stress Test | 160 | 39 | 78 | 60 | Medium | Medium | 3.00 | 80 | 0.56 | Match |
| 17 | Stress Test | 140 | 41 | 82 | 68 | Medium | Medium | 3.00 | 81 | 0.36 | Match |
| 18 | Stress Test | 170 | 38 | 75 | 55 | Medium | Medium | 3.00 | 80 | 0.50 | Match |
| 19 | Stress Test | 130 | 42 | 85 | 35 | Low | Medium | 2.64 | 80 | 0.40 | Mismatch |
| 20 | Stress Test | 155 | 37 | 77 | 62 | Medium | Medium | 3.00 | 80 | 0.52 | Match |

## Current Mismatches

- Case 3: expected `High`, predicted `Very High`
- Case 12: expected `Low`, predicted `Medium`
- Case 19: expected `Low`, predicted `Medium`

## Notes

- The values in this file reflect the current notebook execution state.
- If the rule base or membership ranges change, rerun the notebook and update this file to keep it aligned.
