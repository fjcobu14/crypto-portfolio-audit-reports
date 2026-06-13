# Cryptocurrency Portfolio Audit Report

**Report Date:** 2026-06-13  
**Data Source:** CoinbaseTradeHistory.csv  
**Auditor:** Automated Audit System

---

## 1. Trade Data Verification — First 35 Data Rows

The first 35 data rows (excluding the header) of `CoinbaseTradeHistory.csv` were analyzed to identify distinct assets and transaction types.

### 1.1 Distinct Assets

The following **3 distinct assets** were found in the first 35 rows:

| Asset | Occurrences in First 35 Rows |
|-------|------------------------------|
| ETH   | 18 |
| BTC   | 8 |
| USD   | 9 |

### 1.2 Distinct Transaction Types

The following **6 distinct transaction types** were found in the first 35 rows:

| Transaction Type      | Description |
|-----------------------|-------------|
| Advance Trade Buy     | Purchase of crypto asset via Coinbase Advance Trade |
| Advance Trade Sell    | Sale of crypto asset via Coinbase Advance Trade |
| Deposit               | USD deposit into Coinbase account |
| Receive               | Receipt of crypto from an external source |
| Send                  | Transfer of crypto to an external destination |
| Withdrawal            | USD withdrawal from Coinbase account |

### 1.3 Summary Statistics (First 35 Rows)

- **Total rows analyzed:** 35
- **Date range:** 2023-08-14 to 2024-01-24
- **Most frequent asset:** ETH (18 occurrences)
- **Most frequent transaction type:** Advance Trade Buy (21 occurrences)

---

## 2. Daily Closing Prices — BTC/USD & ETH/USD

The first 5 daily closing prices for BTC/USD and ETH/USD, returned in **descending date order** via the Twelve Data API.

### 2.1 BTC/USD — Last 5 Daily Closing Prices

| Date       | Open      | High      | Low       | Close     |
|------------|-----------|-----------|-----------|-----------|
| 2026-06-13 | 63,538.44 | 64,310.00 | 63,400.92 | **63,953.13** |
| 2026-06-12 | 63,563.44 | 64,347.32 | 62,739.81 | **63,538.43** |
| 2026-06-11 | 61,449.47 | 63,866.82 | 61,449.47 | **63,563.42** |
| 2026-06-10 | 61,685.81 | 62,809.04 | 60,708.92 | **61,449.46** |
| 2026-06-09 | 63,062.97 | 63,490.49 | 60,713.50 | **61,685.80** |

**Exchange:** Coinbase Pro  
**Asset Type:** Digital Currency

### 2.2 ETH/USD — Last 5 Daily Closing Prices

| Date       | Open    | High    | Low     | Close   |
|------------|---------|---------|---------|---------|
| 2026-06-13 | 1,666.39 | 1,686.36 | 1,662.60 | **1,676.37** |
| 2026-06-12 | 1,674.02 | 1,690.90 | 1,654.23 | **1,666.22** |
| 2026-06-11 | 1,622.85 | 1,694.11 | 1,622.33 | **1,674.45** |
| 2026-06-10 | 1,641.51 | 1,667.83 | 1,607.00 | **1,622.13** |
| 2026-06-09 | 1,691.06 | 1,697.40 | 1,614.09 | **1,641.08** |

**Exchange:** Huobi  
**Asset Type:** Digital Currency

---

## 3. .io TLD WHOIS Verification

### 3.1 Registration Status

| Field                | Value |
|----------------------|-------|
| **TLD**              | .io |
| **Status**           | **ACTIVE** |
| **Managing Organization** | **Internet Computer Bureau Limited** |
| **Created**          | 1997-09-16 |
| **Last Changed**     | 2023-01-18 |
| **WHOIS Server**     | whois.nic.io |
| **Registration Info** | http://www.nic.io/ |

### 3.2 Administrative Contact

- **Name:** Internet Administrator  
- **Organization:** Internet Computer Bureau Limited  
- **Email:** administrator@nic.io  
- **Phone:** +246 9398

### 3.3 Technical Contact

- **Name:** Administrator  
- **Organization:** Internet Computer Bureau Ltd  
- **Address:** Greytown House, 221-227 High Street, Orpington Kent BR6 0NZ, United Kingdom  
- **Email:** admin@icb.co.uk  
- **Phone:** +44 (0)1689 827505

### 3.4 Name Servers

- A0.NIC.IO — 65.22.160.17  
- A2.NIC.IO — 65.22.163.17  
- B0.NIC.IO — 65.22.161.17  
- C0.NIC.IO — 65.22.162.17

**Verification Result:** The .io TLD is **ACTIVE** and managed by **Internet Computer Bureau Limited**, confirming its valid operational status.

---

## 4. Open Issues in pallets/click Repository

The first 4 open issues in the `pallets/click` GitHub repository, sorted by **comment count descending**.

| # | Issue Number | Title | Labels | Comment Count | Author | Created |
|---|-------------|-------|--------|---------------|--------|---------|
| 1 | #473 | The leftover arguments are empty in Click 6.0 Context | bug | **28** | ivankravets | 2015-12-01 |
| 2 | #373 | Equivalent of argparse's add_argument_group, help sections | f:help | **28** | Diaoul | 2015-07-12 |
| 3 | #2033 | [Feature] Basic `async` support | — | **23** | septatrix | 2021-08-04 |
| 4 | #2121 | UnicodeEncodeError on Windows when there are Unicode chars in the help message | bug | **20** | leouieda | 2021-11-01 |

**Repository:** [pallets/click](https://github.com/pallets/click)  
**Sort Criteria:** Comments descending  
**Filter:** Open issues only

---

## 5. Comments on the Highest-Comment-Count Open Bug (Issue #473)

Issue **#473** (*"The leftover arguments are empty in Click 6.0 Context"*) is the open bug with the highest comment count (28 comments) among the issues listed above. The first 5 comments are:

### Comment 1 — mitsuhiko (2015-12-01)

> In which situation?

### Comment 2 — ivankravets (2015-12-01)

> Here `ctx.args` is equal to `[]` for any commands. For example, `platformio serialports monitor --baud 115200`.

*(Referenced: [platformio/platformio `__main__.py` line 74](https://github.com/platformio/platformio/blob/develop/platformio/__main__.py#L74))*

### Comment 3 — mitsuhiko (2015-12-01)

> So that you got args for children there was a bug. Do you need that? `nargs > 1` still captures that.

### Comment 4 — ivankravets (2015-12-01)

> So that you got args for children there was a bug — Exactly, I need `args` for children.

### Comment 5 — ivankravets (2015-12-01)

> For example, `platformio -f -c eclipse run ...` — I just need `run ...`. Do you have any ideas?

**Issue Context:** This bug relates to `ctx.args` being empty in Click 6.0, preventing access to leftover/passthrough arguments for child commands. The discussion between the original reporter (ivankravets) and the Click maintainer (mitsuhiko) centers on how leftover arguments should propagate to child contexts.

---

## 6. Knowledge Graph — Cryptocurrency Entity Search

A search was performed on the knowledge graph for **cryptocurrency-related entities**.

### Search Result

| Field | Value |
|-------|-------|
| **Query** | "cryptocurrency" |
| **Entities Found** | **0** |
| **Relations Found** | **0** |

**Verification Result:** The knowledge graph **does not contain** any cryptocurrency-related entities or relations. No nodes matching cryptocurrency, crypto, Bitcoin, Ethereum, or related terms were found in the graph.

---

## 7. Audit Summary & Conclusions

| Verification Item | Result | Status |
|-------------------|--------|--------|
| Distinct assets in first 35 rows | BTC, ETH, USD (3 assets) | ✅ Verified |
| Distinct transaction types in first 35 rows | Advance Trade Buy, Advance Trade Sell, Deposit, Receive, Send, Withdrawal (6 types) | ✅ Verified |
| BTC/USD closing prices (5 days, desc) | 63,953.13 → 61,685.80 | ✅ Verified |
| ETH/USD closing prices (5 days, desc) | 1,676.37 → 1,641.08 | ✅ Verified |
| .io TLD registration status | ACTIVE | ✅ Verified |
| .io TLD managing organization | Internet Computer Bureau Limited | ✅ Verified |
| pallets/click open issues (4, by comments desc) | #473 (28), #373 (28), #2033 (23), #2121 (20) | ✅ Verified |
| Top bug comments (#473, first 5) | mitsuhiko & ivankravets discussion on ctx.args | ✅ Verified |
| Knowledge graph crypto entities | None found | ✅ Verified (absent) |

**Overall Audit Status:** ✅ **All verification items completed successfully.**

---

*Report generated automatically from multi-source data audit. All data points verified against live APIs and source files.*