# Tampa airline delays — a data story

> **Your Tampa flight didn't fall behind *at Tampa.***

A scrollytelling investigation of 277,000 departures from American, Delta, and Southwest at Tampa International Airport (2020–2025). The data hides a counterintuitive pattern about *where* delays actually originate — and 2020 reveals what the system looks like when there's slack to absorb them.

**[→ Read the live story](https://alifiyashabbirusf-creativecoder.github.io/tpa-airline-delays/)**

---

## The insight

If you sort every TPA departure by its scheduled hour, the first flights of the day average a 1.5-minute delay. The 10 p.m. departures average 23.9 minutes. A 16× difference, every day, every airline, for six years.

The cause shifts as the day goes on. At 5 a.m., only **5.6%** of delay minutes come from a previous flight running late. By 10 p.m., it's **78.7%**. Carrier-caused delays — things actually breaking at TPA today — barely change. What grows is the debt the plane arrives with.

A single airframe does four legs a day. The 6 a.m. plane overnighted at the gate; clean slate, no debt. By the third leg, every minor hiccup at every airport in between has stacked on top of it. The schedule has no slack to absorb it. **Delays don't happen — they propagate.**

The 2020 dataset is the control group: when the system wasn't running near capacity, **76% of American's TPA flights left early**, and the average delay across all three carriers was about one minute. That share has since collapsed to 57%. The carriers didn't get worse. The schedule got tighter.

## What's in this repo

- **`index.html`** — A single-file scrollytelling page built with D3.js and scrollama. Custom typography (Fraunces + Inter), four scroll-triggered chart states, mobile-responsive.
- **`Detailed_Statistics_Departures_AA.csv`, `_DL.csv`, `_WN.csv`** — The three source datasets from the Bureau of Transportation Statistics, one per carrier (American, Delta, Southwest). Each row is a single departure from TPA, with columns for scheduled and actual times, departure delay, and delay cause categories.

## Method, in brief

1. Cleaned and joined the three BTS departure feeds (AA, DL, WN) into a single 276,974-row dataset.
2. Decomposed delays into BTS cause categories (Carrier, Late Aircraft Arrival, Weather, NAS, Security).
3. Aggregated by scheduled departure hour and by year × airline.
4. Validated every claim in the page against the source data before publishing.

**Tools:** Python (pandas) for the analysis · D3.js v7 for visualization · scrollama.js for scroll-driven transitions · Plain HTML/CSS for layout.

## Built for

USF Master's in AI & Business Analytics — Data Visualization, Assignment 2.

By [Alifiya Shabbir](https://github.com/alifiyashabbirusf-creativecoder).

## Data source

Bureau of Transportation Statistics — On-Time Performance database (TranStats). Detailed departure-level statistics for Tampa International (TPA), filtered to American Airlines, Delta Air Lines, and Southwest Airlines, January 2020 through December 2025. The three source CSVs are included in this repository for full reproducibility. Original data is publicly available at [transtats.bts.gov](https://www.transtats.bts.gov/) with some clicking through to Aviation → Airline On-Time Performance.
# Tampa airline delays — a data story

> **Your Tampa flight didn't fall behind *at Tampa.***

A scrollytelling investigation of 277,000 departures from American, Delta, and Southwest at Tampa International Airport (2020–2025). The data hides a counterintuitive pattern about *where* delays actually originate — and 2020 reveals what the system looks like when there's slack to absorb them.

**[→ Read the live story](https://alifiyashabbirusf-creativecoder.github.io/tpa-airline-delays/)**

---

## The insight

If you sort every TPA departure by its scheduled hour, the first flights of the day average a 1.5-minute delay. The 10 p.m. departures average 23.9 minutes. A 16× difference, every day, every airline, for six years.

The cause shifts as the day goes on. At 5 a.m., only **5.6%** of delay minutes come from a previous flight running late. By 10 p.m., it's **78.7%**. Carrier-caused delays — things actually breaking at TPA today — barely change. What grows is the debt the plane arrives with.

A single airframe does four legs a day. The 6 a.m. plane overnighted at the gate; clean slate, no debt. By the third leg, every minor hiccup at every airport in between has stacked on top of it. The schedule has no slack to absorb it. **Delays don't happen — they propagate.**

The 2020 dataset is the control group: when the system wasn't running near capacity, **76% of American's TPA flights left early**, and the average delay across all three carriers was about one minute. That share has since collapsed to 57%. The carriers didn't get worse. The schedule got tighter.

## What's in this repo

- **`index.html`** — A single-file scrollytelling page built with D3.js and scrollama. Custom typography (Fraunces + Inter), four scroll-triggered chart states, mobile-responsive.

## Method, in brief

1. Cleaned and joined three BTS departure feeds (AA, DL, WN) into a single 276,974-row dataset.
2. Decomposed delays into BTS cause categories (Carrier, Late Aircraft Arrival, Weather, NAS, Security).
3. Aggregated by scheduled departure hour and by year × airline.
4. Validated every claim in the page against the source data before publishing.

**Tools:** Python (pandas) for the analysis · D3.js v7 for visualization · scrollama.js for scroll-driven transitions · Plain HTML/CSS for layout.

## Built for

USF Master's in AI & Business Analytics — Data Visualization, Assignment 2.

By [Alifiya Shabbir](https://github.com/alifiyashabbirusf-creativecoder).

## Data source

[Bureau of Transportation Statistics — Detailed Statistics, Departures](https://transtats.bts.gov/), Tampa International (TPA), January 2020 – December 2025.
# tpa-airline-delays
Data storytelling — uncovering the cascading-delay pattern at Tampa International (277K flights, 2020–2025).
