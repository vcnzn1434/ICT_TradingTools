# ICT Drawing Tools

vcnzn.com

A professional suite of **drawing tools** and **indicators** for [NinjaTrader 8](https://ninjatrader.com), built for ICT / Smart Money Concepts traders. Fast, configurable chart annotation with built-in risk analysis, alerts, and cross-chart synchronization.

---

## Table of Contents

- [Installation](#installation)
- [License Activation](#license-activation)
- [Tools](#tools)
- [Feature Matrix](#feature-matrix)
- [FPS Counter](#fps-counter)
- [Export Drawings](#export-drawings)
- [Alerts & Push Notifications](#alerts--push-notifications)
- [Updating](#updating)
- [FAQ](#faq)
- [Support](#support)
- [Our Mission](#our-mission)
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
4. The drawing tools appear in the **Drawing Tools** toolbar. Repeater V3 and FPS Counter appear under **Indicators**.
5. **Activate your license** — right-click any chart → **License Manager** → enter your license key (from your Whop Software purchase) → **Activate**.

That's it. One file, no dependencies.

---

## License Activation

### How to activate

1. Right-click on any chart in NinjaTrader.
2. Select **License Manager** from the context menu.
3. Enter your license key (from your Whop Software purchase).
4. Click **Activate**.
5. You'll see **✓ Licensed** when successful.

### How licensing works

- Your license is validated against our server on activation.
- Re-validation happens automatically every 4 hours in the background.
- If you lose internet, a **7-day offline grace period** keeps everything working.
- After 7 days offline, you'll need to reconnect to revalidate.
- Your license is tied to your machine — use the **Reset** button on your Whop product page to transfer to a new computer.

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

### FPS Counter (Free Indicator)

A lightweight, passive performance monitor that displays chart rendering frame rate and tick throughput.

- **No license required** — works for everyone
- **Zero forced redraws** — purely passive, counts natural chart repaints
- **Render FPS** — measures how many times per second the chart actually redraws
- **Tick Rate (TPS)** — measures incoming ticks per second during live market
- **FPS vs TPS comparison** — if FPS drops below TPS, your chart is struggling to keep up with incoming data
- Configurable corner position (top-left, top-right, bottom-left, bottom-right)
- Customizable text color, background color, and font size
- Idle detection — FPS decays to 0 when chart is not redrawing
- Monospace Consolas font in a rounded pill overlay

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

## FPS Counter

The FPS Counter is a free, zero-overhead diagnostic indicator that passively measures your chart's rendering performance.

### What it shows

| Metric | Meaning |
|--------|---------|
| **FPS** (Frames Per Second) | How many times per second the chart is actually redrawing |
| **TPS** (Ticks Per Second) | How many market ticks are arriving per second (live market only) |

### How to interpret

- **FPS ≈ TPS** — Your chart is rendering comfortably, keeping up with every tick.
- **FPS < TPS** — The chart can't render fast enough; NinjaTrader is coalescing/dropping frames. Consider reducing visible drawings or switching to a simpler chart type.
- **FPS = 0** — Normal when the market is closed and you're not interacting with the chart. The chart only redraws when there's a reason to.
- **High FPS during scrolling/zooming** — Reflects how fast the chart redraws during user interaction.

### Settings

| Property | Default | Description |
|----------|---------|-------------|
| Text Color | White | Display text color |
| Background Color | Semi-transparent dark | Pill background |
| Font Size | 12 | Consolas bold monospace |
| Position | Top Right | Corner placement |
| Show Tick Rate | On | Display TPS alongside FPS during live market |

### Notes

- No license required.
- Adds no forced redraws — purely counts existing `OnRender` calls.
- Negligible rendering cost (one small text overlay per frame).
- TPS is only shown during live/realtime market data.

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

1. Download the latest **ICT_DrawingTools.dll** from your Whop Files page.
2. Close NinjaTrader 8.
3. Replace the existing DLL in `Documents\NinjaTrader 8\bin\Custom\`.
4. Launch NinjaTrader 8.

Your license stays active — no re-activation needed after updates.

---

## FAQ

**Q: How many machines can I use my license on?**
A: One machine per license. You can transfer it yourself via Whop (see below).

**Q: What happens if my subscription expires?**
A: The drawing tools stop rendering on your charts. Your existing drawings are preserved and will reappear when you resubscribe.

**Q: Does Repeater V3 require a license?**
A: No. Repeater V3 is free and works without activation.

**Q: Does FPS Counter require a license?**
A: No. FPS Counter is free and works without activation.

**Q: FPS Counter shows 0 when the market is closed. Is it broken?**
A: No. It only counts actual chart redraws. When no data is arriving and you're not interacting with the chart, the chart doesn't redraw, so FPS is correctly 0.

**Q: Can I use this with NinjaTrader's Sim (demo) account?**
A: Yes. The tools work on all chart types — live, sim, and replay.

**Q: I switched computers. How do I transfer my license?**
A: Go to your Whop product page and click the **Reset** button on your Software license. This clears the machine binding. Then install the DLL on your new computer and activate with the same license key. No need to contact support.

**Q: The tools don't appear after installing. What do I do?**
A: Make sure the DLL is in the correct folder (`Documents\NinjaTrader 8\bin\Custom\`), not a subfolder. Restart NinjaTrader completely (close all windows, not just the chart).

---

## Support

For bugs, issues, or feature requests:

- Visit your **Whop product page** for community access and direct support
- Include your **Machine ID** (found in License Manager) when reporting issues

> **Note:** For machine transfers, use the **Reset** button on your Whop Software license — no need to contact support.

---

## Our Mission

In markets that move with depth and structure — fractal in nature, reflecting the order of His Word — we center our trading on the True Living God, the One who declares the end from the beginning.

In every session, we pray:

> *Lord, discipline our hearts and minds so we may reflect who You are shaping us to become.*

Because markets require more than skill — they require Godly attributes. Guide us and allow us this:

- **Forgiveness** — Let yesterday's mistakes stay in yesterday.
- **Patience** — Wait with intention. Act with discipline.
- **Wisdom** — Discern the ever-changing conditions with clarity.

*In Jesus' name, Amen.*

---

## Legal

Copyright (c) 2026 VCNZN. All rights reserved.

This software is proprietary and confidential. Unauthorized copying, modification, distribution, or reverse engineering is strictly prohibited. Licensed exclusively under a paid subscription. See [LICENSE](LICENSE) for full terms.

**Trading Disclaimer:** This software is a charting tool only and does not constitute financial advice. Trading futures, options, and other financial instruments involves substantial risk of loss. You are solely responsible for your own trading decisions and any resulting profits or losses. Past performance is not indicative of future results. These tools were built and tested on NQ (Nasdaq 100 E-mini futures) — while they should work on other instruments, behavior on other markets has not been extensively verified.

RepeaterV3 is based on the free RepeaterV2 community indicator and does not require a license.

FPS Counter is a free utility indicator and does not require a license.



