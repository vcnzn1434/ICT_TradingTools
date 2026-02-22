# ICT Drawing Tools

A professional suite of **drawing tools** and **indicators** for [NinjaTrader 8](https://ninjatrader.com), built for ICT / Smart Money Concepts traders. Fast, configurable chart annotation with built-in risk analysis, alerts, and cross-chart synchronization.

---

## Table of Contents

- [Installation](#installation)
- [License Activation](#license-activation)
- [Tools](#tools)
- [Feature Matrix](#feature-matrix)
- [Export Drawings](#export-drawings)
- [Alerts & Push Notifications](#alerts--push-notifications)
- [Updating](#updating)
- [FAQ](#faq)
- [Support](#support)
- [Legal](#legal)

---

## Installation

1. **Close** NinjaTrader 8 completely.
2. **If upgrading from a source-code (.cs) version**, remove any previous ICT Drawing Tools `.cs` files from `Documents\NinjaTrader 8\bin\Custom\` and its subfolders (`DrawingTools\`, `AddOns\`, etc.). Keeping old `.cs` files alongside the DLL will cause duplicate type errors.
3. Copy **`ICT_DrawingTools.dll`** into your NinjaTrader custom folder:
   ```
   Documents\NinjaTrader 8\bin\Custom\
   ```
   > **Tip:** Press `Win + R`, type `%USERPROFILE%\Documents\NinjaTrader 8\bin\Custom` and hit Enter to open the folder directly.
4. **Launch** NinjaTrader 8.
4. The drawing tools appear in the **Drawing Tools** toolbar. Repeater V3 appears under **Indicators**.
5. **Activate your license** — right-click any chart → **License Manager** → enter your license key → **Activate**.

That's it. One file, no dependencies.

---

## License Activation

### How to activate

1. Right-click on any chart in NinjaTrader.
2. Select **License Manager** from the context menu.
3. Enter your license key (from your Whop purchase).
4. Click **Activate**.
5. You'll see **✓ Licensed** when successful.

### How licensing works

- Your license is validated against our server on activation.
- Re-validation happens automatically every 4 hours in the background.
- If you lose internet, a **7-day offline grace period** keeps everything working.
- After 7 days offline, you'll need to reconnect to revalidate.
- Your license is tied to your machine — contact support if you switch computers.

### Status indicators

| Status | Meaning |
|--------|---------|
| ✓ Licensed | Active subscription — all tools unlocked |
| ⚠ Grace Period | Currently offline — days remaining shown |
| ✕ Expired | Subscription ended or grace period exceeded |
| ✕ Invalid Key | Key not recognized — check for typos |
| Not Activated | No key entered yet |

### Deactivating

Click **Deactivate** in the License Manager window to remove the stored key from your machine. This does **not** cancel your subscription — manage billing through Whop.

---

## Tools

### FVG Tool — Fair Value Gap

Detects and draws Fair Value Gap and Volume Imbalance zones with optional chaining into combined zones.

- **Auto-detection** of Bullish / Bearish FVGs from your click position
- **8 interval presets** — each with independent colors and opacity
- **Volume Imbalance** detection with FVG+VI chaining into mixed zones
- **Risk display** — currency, points, ticks, or percentage from zone edge
- **Price display** — Full price, last 2/3/4 digits, or ticks-from-current
- **Gap size** — points, ticks, percentage, or currency
- **Midpoint & quadrant lines** for precise levels within the zone
- **Extension modes** — auto-extend, extend to session end, or extend to clicked session end
- **Alerts** — NinjaTrader sound + Pushover push notifications

### OrderBlock Tool

Draws Order Block zones with full annotation and analysis features.

- Midpoint and quadrant level splits
- Price, size, and risk text displays
- Auto-extend, session-end extend, and cut-extend modes
- Alerts with Pushover support

### RejectionBlock Tool

Draws Rejection Block (wick rejection) zones with the same feature set as the OrderBlock Tool.

### ORG Tool — Opening Range / Gap

Draws zones between two time-price reference points for opening range and gap analysis.

- Auto-detection of Opening Range Gaps
- Midpoint, quadrant, and price displays
- Risk and gap size display
- Full extension and alert support

### Zone Tool

A fast, general-purpose rectangle/zone drawing tool with two-click placement.

- Simple two-click zone drawing
- Configurable fill and border appearance
- Midpoint & quadrant lines
- Price, zone size, and risk displays
- Auto-extend, session-end extend, cut-extend modes
- Alerts with Pushover support
- Full right-click context menu

### Line Tool

Draws horizontal lines from candle levels with rich labeling.

- Price label with configurable format and placement
- Custom text labels
- Ticks-away display from current price
- Auto-extend, session-end extend, cut-extend
- Alerts with Pushover support

### Price & Time Marker

Places directional arrow markers at specific bar locations.

- Captures OHLC and time data from the bar
- Configurable display of Open, High, Low, Close, Time
- Multiple placement positions

### Position Tool

A comprehensive position sizing and risk/reward visualizer.

- Entry, stop loss, and up to 6 take-profit targets
- Risk amount, percentage, and R:R calculations
- Visual projection lines to each target
- Smooth anti-aliased connecting line between entry, stop, and targets
- Saveable risk presets with confirmation on delete
- Predefined risk value presets for fast setup
- One-click order placement (entry, stop, targets)
- Break-even and flatten from context menu

### Text Annotation Tool

Inline text labels and callout annotations with leader lines.

- Rich formatting — bold, italic, font family and size
- Background fill and border options
- 8 text alignment positions
- Callout mode with connection point and leader line

### Repeater V3 (Free Indicator)

Auto-draws time/price regions on a repeating schedule. Based on the community RepeaterV2 with a dynamic rectangle outline opacity fix.

- **No license required** — works for everyone
- Session-based scheduling
- Repeating time-window regions
- Works on all intraday intervals
- **User-configurable event tags** — assign a custom tag name to each event (up to 10)
- **Export support** — indicator-generated drawings are included in the Export Drawings CSV with clean tag names

### Chart Screenshot

One-click chart screenshots saved to a configurable folder.

- Keyboard shortcut support (Ctrl+Shift+S)
- Toolbar camera icon — click to capture
- Toolbar folder icon — click to choose save folder
- Configurable save folder (defaults to `Pictures\Screenshots`)
- Audible confirmation sound on capture
- Auto-copies screenshot to clipboard
- High-DPI and multi-monitor aware

---

## Feature Matrix

| Feature | FVG | OB | RB | ORG | Zone | Line | Marker | Position | Text |
|---------|:---:|:--:|:--:|:---:|:----:|:----:|:------:|:--------:|:----:|
| Auto-extend | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | — | — |
| Session-end extend | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | — | — |
| Cut extend | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | — | — |
| Midpoint line | ✓ | ✓ | ✓ | ✓ | ✓ | — | — | — | — |
| Quadrant lines | ✓ | ✓ | ✓ | ✓ | ✓ | — | — | — | — |
| Price labels | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — |
| Risk display | ✓ | ✓ | ✓ | ✓ | ✓ | — | — | ✓ | — |
| Text templates | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | — | — |
| Alerts | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | — | — |
| Pushover | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | — | — |
| Right-click menu | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |

---

## Export Drawings

Export all visible drawings on a chart to a structured CSV file for journaling, review, or external analysis.

### How to export

1. Right-click anywhere on a chart.
2. Click **Export Drawings for Date**.
3. A CSV file is saved automatically to:
   ```
   Documents\NinjaTrader 8\DrawingExport\
   ```

The export uses the date at your click position — all drawings whose time range overlaps that date are included. Only drawings that are **visible on the current chart** are exported (scrolled-off drawings are excluded).

### What gets exported

The export captures every ICT Drawing Tool plus indicator-generated drawings (e.g., Repeater V3 rectangles). Each row is one drawing with these columns:

| Column | Description |
|--------|-------------|
| ToolType | Drawing tool name (FVGTool, OrderBlockTool, ZoneTool, etc.) |
| Direction | Bullish / Bearish / Long / Short (where applicable) |
| Interval | Chart interval the drawing was created on (e.g., 1 Min, 5 Min) |
| StartTime | Left edge timestamp |
| EndTime | Right edge timestamp |
| TopPrice | Upper price boundary |
| BottomPrice | Lower price boundary |
| Price | Single-price value (lines, markers, position entry) |
| Midpoint | Midpoint price (if midpoint is enabled) |
| Q1_25pct | Lower quadrant price (if quadrants are enabled) |
| Q3_75pct | Upper quadrant price (if quadrants are enabled) |
| MidpointEnabled | Whether midpoint line is on |
| QuadrantsEnabled | Whether quadrant lines are on |
| Label | Text label / annotation on the drawing |
| Tag | Drawing tag identifier |
| CandleOpen/High/Low/Close | OHLC data (Price & Time Marker only) |

**Position Tool** rows include additional dynamic columns: EntryPrice, StopPrice, RiskMethod, RiskValue, TargetMethod, per-target prices/R:R/scale-out percentages, BestRR, Account, and order types.

**Third-party / native NinjaTrader drawings** (rectangles, lines, regions) are captured using a generic fallback that reads all anchors and whitelisted trading-relevant properties automatically.

### File naming

Files are named with the format:
```
Export_<Instrument>_<Date>_<Time>.csv
```
For example: `Export_ES_2026-02-22_143052.csv`

### Notes

- Requires an active license.
- Indicator-generated drawing tags are cleaned automatically (trailing event/bar suffixes are stripped).
- Columns are dynamic — only columns with data appear in the output. Position-specific fields won't clutter exports that contain only zone tools.
- Auto-extending zones are always included if their start time is on or before the target date.

---

## Alerts & Push Notifications

All zone and line tools include alerts powered by a shared alert engine:

1. **NinjaTrader sound alerts** — plays a .wav file through NinjaTrader's built-in alert system.
2. **Pushover notifications** — sends push notifications to your phone via [Pushover](https://pushover.net) with 23 configurable sounds.
3. **Template tokens** — customize alert messages with `@INSTRUMENT`, `@INTERVAL`, `@DIRECTION`, `@PRICE`, and more.
4. **Rearm on re-entry** — optionally re-triggers when price leaves and re-enters a zone.

**Pushover setup:** Enter your Pushover **User Key** and **API Token** in the tool's Alert property group. Get these from [pushover.net](https://pushover.net) (separate service, not included).

---

## Updating

1. Download the latest **ICT_DrawingTools.dll** from your Whop purchase page.
2. Close NinjaTrader 8.
3. Replace the existing DLL in `Documents\NinjaTrader 8\bin\Custom\`.
4. Launch NinjaTrader 8.

Your license stays active — no re-activation needed after updates.

---

## FAQ

**Q: How many machines can I use my license on?**
A: One machine per license. Contact support if you need to transfer to a new computer.

**Q: What happens if my subscription expires?**
A: The drawing tools stop rendering on your charts. Your existing drawings are preserved and will reappear when you resubscribe.

**Q: Does Repeater V3 require a license?**
A: No. Repeater V3 is free and works without activation.

**Q: Can I use this with NinjaTrader's Sim (demo) account?**
A: Yes. The tools work on all chart types — live, sim, and replay.

**Q: I switched computers. How do I transfer my license?**
A: Deactivate on your old machine first (License Manager → Deactivate), then activate on the new one. If you no longer have access to the old machine, contact support.

**Q: The tools don't appear after installing. What do I do?**
A: Make sure the DLL is in the correct folder (`Documents\NinjaTrader 8\bin\Custom\`), not a subfolder. Restart NinjaTrader completely (close all windows, not just the chart).

---

## Support

For help, questions, or feature requests:

- Visit your **Whop purchase page** for community access and direct support
- Include your **Machine ID** (found in License Manager) when contacting support

---

## Legal

Copyright (c) 2026 VCNZN. All rights reserved.

This software is proprietary and confidential. Unauthorized copying, modification, distribution, or reverse engineering is strictly prohibited. Licensed exclusively under a paid subscription. See [LICENSE](LICENSE) for full terms.

**Trading Disclaimer:** This software is a charting tool only and does not constitute financial advice. Trading futures, options, and other financial instruments involves substantial risk of loss. You are solely responsible for your own trading decisions and any resulting profits or losses. Past performance is not indicative of future results.

RepeaterV3 is based on the free RepeaterV2 community indicator and does not require a license.
