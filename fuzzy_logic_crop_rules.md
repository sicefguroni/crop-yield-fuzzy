# Fuzzy Logic Rules for Crop Yield Prediction

## Input Variables and Linguistic Terms

| Variable | Low | Medium | High |
|---|---|---|---|
| Rainfall | Low | Moderate | High |
| Temperature | Cold | Warm | Hot |
| Soil Moisture | Dry | Moist | Wet |
| Soil Nutrients | Poor | Fair | Rich |

## Output Variable
- **Yield**: Very Low, Low, Medium, High, Very High

---

## 81 IF-THEN Rules

Rules are organized by Rainfall level, then Temperature, then Soil Moisture, varying Soil Nutrients across each row.

### Rainfall: LOW

| # | Rainfall | Temperature | Soil Moisture | Soil Nutrients | Yield |
|---|---|---|---|---|---|
| 1 | Low | Cold | Dry | Poor | Very Low |
| 2 | Low | Cold | Dry | Fair | Very Low |
| 3 | Low | Cold | Dry | Rich | Low |
| 4 | Low | Cold | Moist | Poor | Very Low |
| 5 | Low | Cold | Moist | Fair | Low |
| 6 | Low | Cold | Moist | Rich | Low |
| 7 | Low | Cold | Wet | Poor | Low |
| 8 | Low | Cold | Wet | Fair | Low |
| 9 | Low | Cold | Wet | Rich | Medium |
| 10 | Low | Warm | Dry | Poor | Very Low |
| 11 | Low | Warm | Dry | Fair | Low |
| 12 | Low | Warm | Dry | Rich | Low |
| 13 | Low | Warm | Moist | Poor | Low |
| 14 | Low | Warm | Moist | Fair | Low |
| 15 | Low | Warm | Moist | Rich | Medium |
| 16 | Low | Warm | Wet | Poor | Low |
| 17 | Low | Warm | Wet | Fair | Medium |
| 18 | Low | Warm | Wet | Rich | Medium |
| 19 | Low | Hot | Dry | Poor | Very Low |
| 20 | Low | Hot | Dry | Fair | Very Low |
| 21 | Low | Hot | Dry | Rich | Low |
| 22 | Low | Hot | Moist | Poor | Very Low |
| 23 | Low | Hot | Moist | Fair | Low |
| 24 | Low | Hot | Moist | Rich | Low |
| 25 | Low | Hot | Wet | Poor | Low |
| 26 | Low | Hot | Wet | Fair | Low |
| 27 | Low | Hot | Wet | Rich | Medium |

---

### Rainfall: MODERATE

| # | Rainfall | Temperature | Soil Moisture | Soil Nutrients | Yield |
|---|---|---|---|---|---|
| 28 | Moderate | Cold | Dry | Poor | Low |
| 29 | Moderate | Cold | Dry | Fair | Low |
| 30 | Moderate | Cold | Dry | Rich | Medium |
| 31 | Moderate | Cold | Moist | Poor | Low |
| 32 | Moderate | Cold | Moist | Fair | Medium |
| 33 | Moderate | Cold | Moist | Rich | Medium |
| 34 | Moderate | Cold | Wet | Poor | Low |
| 35 | Moderate | Cold | Wet | Fair | Medium |
| 36 | Moderate | Cold | Wet | Rich | Medium |
| 37 | Moderate | Warm | Dry | Poor | Low |
| 38 | Moderate | Warm | Dry | Fair | Medium |
| 39 | Moderate | Warm | Dry | Rich | Medium |
| 40 | Moderate | Warm | Moist | Poor | Medium |
| 41 | Moderate | Warm | Moist | Fair | Medium |
| 42 | Moderate | Warm | Moist | Rich | High |
| 43 | Moderate | Warm | Wet | Poor | Medium |
| 44 | Moderate | Warm | Wet | Fair | High |
| 45 | Moderate | Warm | Wet | Rich | High |
| 46 | Moderate | Hot | Dry | Poor | Low |
| 47 | Moderate | Hot | Dry | Fair | Low |
| 48 | Moderate | Hot | Dry | Rich | Medium |
| 49 | Moderate | Hot | Moist | Poor | Low |
| 50 | Moderate | Hot | Moist | Fair | Medium |
| 51 | Moderate | Hot | Moist | Rich | Medium |
| 52 | Moderate | Hot | Wet | Poor | Medium |
| 53 | Moderate | Hot | Wet | Fair | Medium |
| 54 | Moderate | Hot | Wet | Rich | High |

---

### Rainfall: HIGH

| # | Rainfall | Temperature | Soil Moisture | Soil Nutrients | Yield |
|---|---|---|---|---|---|
| 55 | High | Cold | Dry | Poor | Low |
| 56 | High | Cold | Dry | Fair | Medium |
| 57 | High | Cold | Dry | Rich | Medium |
| 58 | High | Cold | Moist | Poor | Medium |
| 59 | High | Cold | Moist | Fair | Medium |
| 60 | High | Cold | Moist | Rich | High |
| 61 | High | Cold | Wet | Poor | Low |
| 62 | High | Cold | Wet | Fair | Medium |
| 63 | High | Cold | Wet | Rich | Medium |
| 64 | High | Warm | Dry | Poor | Medium |
| 65 | High | Warm | Dry | Fair | Medium |
| 66 | High | Warm | Dry | Rich | High |
| 67 | High | Warm | Moist | Poor | Medium |
| 68 | High | Warm | Moist | Fair | High |
| 69 | High | Warm | Moist | Rich | Very High |
| 70 | High | Warm | Wet | Poor | Medium |
| 71 | High | Warm | Wet | Fair | High |
| 72 | High | Warm | Wet | Rich | High |
| 73 | High | Hot | Dry | Poor | Low |
| 74 | High | Hot | Dry | Fair | Medium |
| 75 | High | Hot | Dry | Rich | Medium |
| 76 | High | Hot | Moist | Poor | Medium |
| 77 | High | Hot | Moist | Fair | Medium |
| 78 | High | Hot | Moist | Rich | High |
| 79 | High | Hot | Wet | Poor | Low |
| 80 | High | Hot | Wet | Fair | Medium |
| 81 | High | Hot | Wet | Rich | Medium |

---

## Key Logic Notes

- **Warm + Moist/Wet + Rich Nutrients** consistently yields High or Very High regardless of rainfall level.
- **Hot + Dry** conditions always reduce yield due to heat stress and water scarcity.
- **Cold + Wet** does not necessarily mean high yield; low temperature limits plant metabolism.
- **High Rainfall + Wet Soil** can reduce yield (waterlogging risk), hence some High Rainfall rules output Medium instead of High.
- The **only Very High yield** occurs under ideal conditions: High Rainfall + Warm + Moist + Rich Nutrients (Rule 69).
