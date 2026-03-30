# CEE Government Bond Yield Correlation

**Author:** Hermann Ossani  
**Data:** ECB Data Portal + FRED (St. Louis Fed)  
**Updated:** March 2026

---

## Overview
Analysis of 10-year government bond yield co-movement across
8 Central and Eastern European countries using two independent
data sources — the ECB and FRED.

**Countries:** Poland, Czech Rep., Hungary, Slovakia, Austria,
Bulgaria, Croatia, Romania  
**Benchmark:** Germany  
**Period:** 2005–present

---

## Files

| File | Description |
|---|---|
| `Correlation Bonds CEE ECB data.ipynb` | Main analysis — ECB Data Portal |
| `Correlation Bonds CEE FRED data.ipynb` | Same analysis — FRED (St. Louis Fed) |
| `Comparison ECB Data and FRED Data.ipynb` | Cross-source validation |

---

## Methodology
Correlations are computed on **monthly yield changes** (basis points),
not yield levels. Levels are non-stationary and produce misleading
correlations. Changes are stationary and capture genuine co-movement.

---

## Key Findings
## Key Findings

**Correlation structure**
- Austria show the strongest correlation with Germany —
  both are eurozone members with deeply integrated economies
- Bulgaria, Croatia, Romania and Hungary show the weakest correlations
  with Germany — these countries have independent monetary policy,
  local currency risk, and higher political risk premia
- Croatia joined the eurozone only in January 2023 — too recent
  to be visible as a structural shift in the sample period

**2022 spike**
- Correlations across all CEE countries rose sharply during the
  2022-2023 ECB rate hike cycle, as aggressive monetary tightening
  became the dominant driver of all European bond markets
- The Russia-Ukraine war (February 2022) likely amplified this effect —
  a common geopolitical shock hitting all CEE markets simultaneously,
  compressing idiosyncratic differences

**Data source comparison**
- FRED does not carry data for Bulgaria, Croatia and Romania —
  the cross-source comparison is restricted to the 6 available countries
- ECB and FRED correlations differ by less than 0.005 for all
  common country pairs — both sources are fully consistent
- ECB Data Portal is the preferred source for CEE analysis due to
  broader country coverage and no API key requirement
---

## Limitations
- **Correlation is not causation.** High correlation reflects shared
  exposure to ECB policy and global risk sentiment — not a direct
  causal link between markets.
- Non-euro countries (Poland, Czech Rep., Hungary) report yields
  in local currency — currency effects are embedded in the correlation.

---

## Libraries
```
pandas, numpy, matplotlib, seaborn, ecbdata, fredapi, scipy
```

## Data Sources
- **ECB Data Portal:** data-api.ecb.europa.eu — free, no API key required
- **FRED:** fred.stlouisfed.org — free, API key required