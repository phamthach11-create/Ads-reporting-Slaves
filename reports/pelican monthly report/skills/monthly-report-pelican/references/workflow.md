# Pelican monthly PPT workflow

## Source setup

- Use the prior month's Pelican PPTX as the template.
- Keep the visual design and edit inherited elements in place.
- Google Ads account: Larson Packaging Company.
- Default Google Ads filter: campaign name contains `Pelican`.
- Use enabled and paused campaigns when the report requires historical performance.
- Confirm the visible date range after every navigation because Google Ads may retain a stale URL parameter.

## Slide 1 — Reporting period

- Replace the prior month with the new report month.
- Preserve all design elements.

## Slide 2 — Account overview

- Use all campaigns containing `Pelican`.
- Show the latest month and compare with the immediately preceding month.
- Pull account metrics from Google Ads.
- Calculate account-level CPL as total cost divided by total leads.
- Reconcile totals before writing them to the slide.

## Slide 3 — Pelican performance analysis

- Query Google Ads Advisor with the performance prompt in `advisor-prompts.md`.
- Include only Pelican campaigns.
- Shorten the response and distribute ideas across the inherited analysis boxes.
- Retain verified numbers and remove unsupported or overly long commentary.

## Slide 4 — Keyword table

- Open Google Ads Search keywords.
- Filter campaign name contains `Pelican` and set the report month.
- Show at most 10 representative keywords.
- Prioritize every keyword with conversions, then high-spend non-converting keywords.
- Preserve the table structure and number formats.

## Slide 5 — Keyword analysis

- Query Ads Advisor with the keyword prompt in `advisor-prompts.md`.
- Structure the output around top keywords, search intent and competition, and engagement.
- Keep only claims supported by visible keyword or auction data.

## Slide 6 — GA4 acquisition

Use the GA4 property associated with Pelican/Larson Packaging.

### User acquisition chart

- Report: `User acquisition: First user primary channel group (Default Channel Group)`.
- Dimension: `First user source / medium`.
- Metric: `New users`.

### Traffic acquisition chart

- Report: `Traffic acquisition: Session primary channel group (Default Channel Group)`.
- Dimension: `Session source / medium`.
- Metric: `Sessions`.

### Grouping

- Aggregate duplicate source/medium values split across channel groups.
- Display Top 3 source/medium rows.
- Group rank 4 onward as `Other` using total minus Top 3.
- Update both native charts and write a short comparison of acquisition versus sessions.

## Slide 7 — Age and gender

- Google Ads path: `Overview`.
- Apply campaign name contains Pelican and the report month.
- Find the `Demographics` card and select `Gender & Age`.
- Capture only the card boundaries. Exclude filters, date controls, navigation, and adjacent cards.
- Query Ads Advisor with the demographic prompt.
- Analyze known age/gender segments and acknowledge `Unknown` separately.

## Slide 8 — Devices

- Google Ads path: `Overview`.
- Capture only the `Devices` card.
- The useful card metrics are Cost, Clicks, and the lead/conversion metric selected in the card.
- Query Ads Advisor with the device prompt.
- Compare mobile phones, computers, and tablets using clicks, cost, conversions, and CPL.
- Do not call mobile efficient merely because it has the most clicks.

## Slide 9 — Ad schedule

- Google Ads path: `Overview`.
- Capture only the `Day & hour` card with `Day & Hour` selected.
- Query Ads Advisor with the schedule prompt.
- Identify strongest days, strongest hours, weak periods, and a concise scheduling implication.

## Slide 10 — Matched locations

- Google Ads path: `Insights and reports → When and where ads showed → Matched locations`.
- Set level to `Regions`.
- Filter campaign name contains Pelican and set the report month.
- Read real table values for Location, Cost, Conversions, and Cost/conv.
- Update the inherited native chart; never insert a screenshot.
- Preserve the actual template's chart series. The September run verified three series: Cost, Conversions and Cost/conversion; do not remove one based on an older default.
- If using Cost/conv for grouped locations, recalculate as total grouped cost / total grouped conversions.
- Change a stale `last 3 months` title to the actual date range used.
- Analyze cost concentration, conversion volume, CPL, non-converting spend, and practical geographic implications.

## Slide 11 — Conclusion

- Synthesize only verified findings already present in the deck.
- State the strongest channel, keyword/device/time/location opportunities, and the most important efficiency risk.
- Do not introduce new metrics or speculative initiatives.

## Screenshot handling

- Take the screenshot from the live signed-in Google Ads tab.
- Crop to the exact white card boundary.
- Preserve the full card header, metric selector, visualization, footnote, and destination link.
- Use `contain` when the card and inherited image frame have different aspect ratios.
- Inspect the standalone crop before inserting it.

## QA checklist

- Report month is consistent on every slide.
- All Google Ads data is Pelican-only.
- Month-over-month comparisons use adjacent complete months.
- GA4 Top 3 + Other totals reconcile to the report total.
- Keyword table contains at most 10 rows.
- Overview screenshots contain only their individual cards.
- Slide 10 remains an editable native chart.
- Every analysis statement matches visible data.
- Speaker notes include source, date range, filters, and calculation notes.
- Final PPTX reopens successfully and edited slides have no clipping or overlap.

## Lessons from the September run

- Verify reporting month inside the deck: the August template was named July, but its cover and metric table were August.
- Include enabled and paused Pelican campaigns with historical data; do not use current status as a substitute for activity in the reporting month.
- Use only Pelican totals in every analysis; old template sections contained LPC/all-account metrics and rolling 30-day periods.
- Preserve real missing-source categories in GA4 rankings; do not replace them with last month's preferred sources.
- Reconcile regional metrics at the combined Pelican scope, not a single campaign scope. Device cards must use the intended conversion metric, not a narrower lead action without disclosure.
- PPTX export previously lost chart-workbook relationships. Verify all three editable charts retain valid embedded workbook links and that chart caches match workbook data after export.
- September structural checks passed, but visual rendering hung. That historical result does not establish visual approval: render and inspect the new deck before claiming visual checks pass.
