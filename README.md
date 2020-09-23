Florida COVID-19 Data
================
2020-09-23 12:14:15

## Today

| When        | Day        | Positive | New Positive Since | Deaths | New Deaths Since | Total     |
| :---------- | :--------- | :------- | :----------------- | :----- | :--------------- | :-------- |
| Today       | 2020-09-23 | 690,499  | 0                  | 13,782 | 0                | 5,155,980 |
| Yesterday   | 2020-09-22 | 687,909  | 2,590              | 13,579 | 203              | 5,132,342 |
| Last Week   | 2020-09-16 | 671,201  | 19,298             | 13,100 | 682              | 4,984,023 |
| 2 Weeks Ago | 2020-09-09 | 652,148  | 38,351             | 12,269 | 1,513            | 4,831,248 |

Parsed from the [Florida’s COVID-19 Data and Surveillance
Dashboard](https://fdoh.maps.arcgis.com/apps/opsdashboard/index.html#/8d0de33f260d444c852a615dc7837c86).

Prior to 2020-04-25, Florida DOH published updated data twice per day.
Starting 2020-04-25, Florida DOH updates once per day at approximately
11am. Since 2020-05-06, the updates are occasionally later in the day.
In the following charts, for a given day, I use the last value reported
prior to 8am of the subsequent day. I take snapshots of the various FL
DOH data sources at 7am, noon and 7pm daily.

## Confirmed Cases

![](plots/covid-19-florida-daily-test-changes.png)

![](plots/covid-19-florida-deaths-by-day.png)

![](plots/covid-19-florida-county-top-6.png)

<div class="columns">

<div class="column is-full-mobile">

![](plots/covid-19-florida-testing.png)

</div>

<div class="column is-full-mobile">

![](plots/covid-19-florida-total-positive.png)

</div>

</div>

## Hospital and ICU Utilization

| County       | Current COVID Hospitalizations | Change Since Yesterday                   | Available Hospital Beds                      | Available ICU Beds                         |
| :----------- | -----------------------------: | :--------------------------------------- | :------------------------------------------- | :----------------------------------------- |
| All          |                           2339 | <span style="color: #EC4E20">↑ 20</span> | 14861<span style="color: #aaa">/46178</span> | 1367<span style="color: #aaa">/4656</span> |
| Miami-Dade   |                            314 | <span style="color: #6BAA75">↓ -1</span> | 2458<span style="color: #aaa">/6167</span>   | 184<span style="color: #aaa">/750</span>   |
| Broward      |                            242 |                                          | 1112<span style="color: #aaa">/4074</span>   | 115<span style="color: #aaa">/350</span>   |
| Hillsborough |                            150 | <span style="color: #EC4E20">↑ 7</span>  | 543<span style="color: #aaa">/3238</span>    | 39<span style="color: #aaa">/335</span>    |
| Palm Beach   |                            147 | <span style="color: #6BAA75">↓ -2</span> | 1270<span style="color: #aaa">/2755</span>   | 146<span style="color: #aaa">/251</span>   |
| Duval        |                            136 | <span style="color: #6BAA75">↓ -2</span> | 871<span style="color: #aaa">/2878</span>    | 123<span style="color: #aaa">/314</span>   |
| Polk         |                            117 |                                          | 320<span style="color: #aaa">/1332</span>    | 15<span style="color: #aaa">/131</span>    |
| Orange       |                            114 |                                          | 1116<span style="color: #aaa">/3287</span>   | 142<span style="color: #aaa">/262</span>   |
| Pinellas     |                            105 | <span style="color: #6BAA75">↓ -1</span> | 867<span style="color: #aaa">/2309</span>    | 60<span style="color: #aaa">/237</span>    |
| Alachua      |                             79 | <span style="color: #EC4E20">↑ 2</span>  | 235<span style="color: #aaa">/1459</span>    | 31<span style="color: #aaa">/277</span>    |
| Volusia      |                             63 |                                          | 398<span style="color: #aaa">/1162</span>    | 68<span style="color: #aaa">/179</span>    |

![](plots/covid-19-florida-icu-usage.png)

## Daily Testing

![](plots/covid-19-florida-tests-per-case.png)

<!-- ![](plots/covid-19-florida-change-new-cases.png) -->

![](plots/covid-19-florida-tests-percent-positive.png)

![](plots/covid-19-florida-test-and-case-growth.png)

## Cases and Deaths by Age

![](plots/covid-19-florida-weekly-events-by-age.png)

![](plots/covid-19-florida-age.png)

![](plots/covid-19-florida-age-deaths.png)

![](plots/covid-19-florida-age-sex.png)

## Sources

  - [Florida’s COVID-19 Data and Surveillance
    Dashboard](https://fdoh.maps.arcgis.com/apps/opsdashboard/index.html#/8d0de33f260d444c852a615dc7837c86)

  - [Florida Department of Health COVID-19 status
    page](http://www.floridahealth.gov/diseases-and-conditions/COVID-19/)

  - PDF Reports released daily on [Florida Disaster
    Covid-19](http://www.floridahealth.gov/diseases-and-conditions/COVID-19/)

The data structure and format of the released data changes frequently.
I’m keeping track of the impact of these changes in this repo in
[NEWS.md](NEWS.md).

## FL DOH Dashboard

One table is extracted from the [Florida’s COVID-19 Data and
Surveillance
Dashboard](https://fdoh.maps.arcgis.com/apps/opsdashboard/index.html#/8d0de33f260d444c852a615dc7837c86).

  - Current test counts:
    [data/covid-19-florida\_dash\_summary.csv](data/covid-19-florida_dash_summary.csv)

The `timestamp` column of indicates when the dashboard was polled for
changes.

Testing statistics prior to 2020-03-16 18:00:00 EDT were imported from
<https://covidtracking.com>.

![](screenshots/fodh_maps_arcgis_com__apps__opsdashboard.png)

## Snapshots and Data Capture

Initially this repo gathered data from the [Florida Department of Health
COVID-19 status
page](http://www.floridahealth.gov/diseases-and-conditions/COVID-19/).
This page has been [reformatted several
times](screenshots/floridahealth_gov__diseases-and-conditions__COVID-19.png)
and the data structure changes frequently, so currently I am collecting
snapshots of the webpage and not trying to parse these tables.

I am also capturing a snapshot (HTML) and screenshot of the [Florida’s
COVID-19 Data and Surveillance
Dashboard](https://fdoh.maps.arcgis.com/apps/opsdashboard/index.html#/8d0de33f260d444c852a615dc7837c86).
Data extracted from the dashboard are currently used for the current
test count summaries, available in
[covid-19-florida-tests.csv](covid-19-florida-tests.csv).

Prior to the afternoon of 2020-03-18, the dashboard reported
county-level case counts. Around 4pm on 2020-03-18, the dashboard layout
was modified, making these counts inaccessible. Similarly, prior to this
update I was relying on the reported “last update time” listed in the
dashboard, but since then I have been using the time at which the
dashboard was checked for any time stamps from this source.

On the same day that county-level data became inaccessible in the
dashboard, FL DOH started releasing PDF reports, which I have begun to
collect in [pdfs/](pdfs/). The name of the report contains a time stamp,
therefore I am periodically checking the FL DOH web page for the updated
link. I’ve been able to extract most of the data from the PDF tables.
Individual tables are stored in time stamped folders, using the time
stamp in the PDF file name. The unified data files are available in
[data/](data/) and prefixed with `covid-19-florida_pdf_`.
