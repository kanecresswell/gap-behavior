# gap-behavior

🧠 Behavioral Gap Classification & Session Flow Analysis
This repository contains a modular Jupyter workflow for classifying trading sessions based on gap behavior, session structure, and closing position relative to prior range. It builds a three-stage behavioral funnel to empirically map market rhythm and flow tendencies.

📦 What This Pipeline Does
1. Session Filtering & Aggregation
Filters raw tick-level data to valid trading sessions (07:00–15:59).

Aggregates into 2-minute OHLCV buckets for structural clarity.

2. Session-Level Summary
Computes daily high/low/close and compares to prior session range.

Tags each session as:

Inside (0) or Outside (1) previous day's range.

Overlapping (0) or Non-overlapping (1) range structure.

3. Gap Classification
Extracts 07:00 and 09:30 open prices.

Classifies each session into one of four gap types:

0: No Gap

1: Morning Gap

2: Overnight & Morning Gap

3: Fake Gap

4: Catch-All (fallback)

4. Behavioral Flow Mapping
Combines gap type, session classification, and close behavior into 3-stage flows.

Computes joint probabilities for each flow.

Visualizes flow distributions with bar charts and pie grids.

5. Flow Scoring & Exploration
Calculates conditional probabilities and flow ratios.

Enables empirical validation of behavioral setups across regimes.

📊 Visual Outputs
Gap type distributions

Session classification probabilities

Conditional bar charts: Close vs Prev Range | Gap Type

2×2 pie grid: Session × Close behavior for each Gap Type

🔧 Modular Extensions (Planned)
Regime memory tracking

Flow scoring engine

Dash-based interactive dashboard

Behavioral overlay tagging for rhythm segmentation

🧠 Why This Matters
This framework is designed for traders and researchers seeking structural clarity and behavioral transparency. It supports rhythm engine development, regime tagging, and expectation-driven market analysis.
