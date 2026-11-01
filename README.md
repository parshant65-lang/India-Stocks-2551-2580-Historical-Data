# India-Stocks-2551-2580-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2551 to 2580)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2551-2580-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2551 to 2580)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2551 | `VISHAL` | Vishal Fabrics Limited | `VISHAL.NS` |
| 2552 | `VISHNU` | Vishnu Chemicals Limited | `VISHNU.NS` |
| 2553 | `VISHWARAJ` | Vishwaraj Sugar Industries Limited | `VISHWARAJ.NS` |
| 2554 | `VITAL` | Vital Chemtech Limited | `VITAL.NS` |
| 2555 | `VIVIANA` | Viviana Power Tech Limited | `VIVIANA.NS` |
| 2556 | `VIVIDHA` | Visagar Polytex Limited | `VIVIDHA.NS` |
| 2557 | `VIVIMEDLAB` | Vivimed Labs Limited | `VIVIMEDLAB.NS` |
| 2558 | `VIVOBIOT` | Vivo Bio Tech Limited | `VIVOBIOT.NS` |
| 2559 | `VIYASH` | Viyash Scientific Limited | `VIYASH.NS` |
| 2560 | `VLEGOV` | VL E-Governance & IT Solutions Limited | `VLEGOV.NS` |
| 2561 | `VLSFINANCE` | VLS Finance Limited | `VLSFINANCE.NS` |
| 2562 | `VMART` | V-Mart Retail Limited | `VMART.NS` |
| 2563 | `VMSTMT` | VMS TMT Limited | `VMSTMT.NS` |
| 2564 | `VNL` | Vishal Nirmiti Limited | `VNL.NS` |
| 2565 | `VOEPL` | Virtuoso Optoelectronics Limited | `VOEPL.NS` |
| 2566 | `VOITHPAPR` | Voith Paper Fabrics India Limited | `VOITHPAPR.NS` |
| 2567 | `VOLTAMP` | Voltamp Transformers Limited | `VOLTAMP.NS` |
| 2568 | `VPRPL` | Vishnu Prakash R Punglia Limited | `VPRPL.NS` |
| 2569 | `VRAJ` | Vraj Iron and Steel Limited | `VRAJ.NS` |
| 2570 | `VRLLOG` | VRL Logistics Limited | `VRLLOG.NS` |
| 2571 | `VSSL` | Vardhman Special Steels Limited | `VSSL.NS` |
| 2572 | `VSTIND` | VST Industries Limited | `VSTIND.NS` |
| 2573 | `VSTL` | Vibhor Steel Tubes Limited | `VSTL.NS` |
| 2574 | `VSTTILLERS` | V.S.T Tillers Tractors Limited | `VSTTILLERS.NS` |
| 2575 | `VTMLTD` | VTM Limited | `VTMLTD.NS` |
| 2576 | `WAAREEINDO` | Indosolar Limited | `WAAREEINDO.NS` |
| 2577 | `WAAREERTL` | Waaree Renewable Technologies Limited | `WAAREERTL.NS` |
| 2578 | `WABAG` | VA Tech Wabag Limited | `WABAG.NS` |
| 2579 | `WAKEFIT` | Wakefit Innovations Limited | `WAKEFIT.NS` |
| 2580 | `WALCHANNAG` | Walchandnagar Industries Limited | `WALCHANNAG.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream VISHAL 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2551-2580-Historical-Data/main/VISHAL/1m/2026/10/VISHAL_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
