Florida COVID-19 Data
================
2020-08-24 19:11:23

## Today

| When        | Day        | Positive | New Positive Since | Deaths | New Deaths Since | Total     |
| :---------- | :--------- | :------- | :----------------- | :----- | :--------------- | :-------- |
| Today       | 2020-08-24 | 602,829  | 0                  | 10,534 | 0                | 4,447,156 |
| Yesterday   | 2020-08-23 | 600,571  | 2,258              | 10,462 | 72               | 4,428,633 |
| Last Week   | 2020-08-17 | 576,094  | 26,735             | 9,674  | 860              | 4,252,876 |
| 2 Weeks Ago | 2020-08-10 | 536,961  | 65,868             | 8,408  | 2,126            | 4,013,857 |

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

| County       | Current COVID Hospitalizations | Change Since Yesterday                    | Available Hospital Beds                      | Available ICU Beds                         |
| :----------- | -----------------------------: | :---------------------------------------- | :------------------------------------------- | :----------------------------------------- |
| All          |                           4646 | <span style="color: #6BAA75">↓ -98</span> | 15920<span style="color: #aaa">/44310</span> | 1338<span style="color: #aaa">/4720</span> |
| Miami-Dade   |                            902 | <span style="color: #EC4E20">↑ 9</span>   | 2058<span style="color: #aaa">/6452</span>   | 164<span style="color: #aaa">/818</span>   |
| Broward      |                            599 | <span style="color: #6BAA75">↓ -38</span> | 1124<span style="color: #aaa">/4022</span>   | 98<span style="color: #aaa">/409</span>    |
| Duval        |                            258 | <span style="color: #6BAA75">↓ -12</span> | 1032<span style="color: #aaa">/2694</span>   | 103<span style="color: #aaa">/331</span>   |
| Hillsborough |                            242 | <span style="color: #EC4E20">↑ 1</span>   | 756<span style="color: #aaa">/2982</span>    | 62<span style="color: #aaa">/306</span>    |
| Palm Beach   |                            237 | <span style="color: #6BAA75">↓ -32</span> | 1416<span style="color: #aaa">/2613</span>   | 133<span style="color: #aaa">/274</span>   |
| Orange       |                            236 | <span style="color: #6BAA75">↓ -12</span> | 1090<span style="color: #aaa">/3237</span>   | 105<span style="color: #aaa">/266</span>   |
| Polk         |                            178 | <span style="color: #EC4E20">↑ 15</span>  | 356<span style="color: #aaa">/1253</span>    | 12<span style="color: #aaa">/134</span>    |
| Pinellas     |                            151 | <span style="color: #6BAA75">↓ -5</span>  | 842<span style="color: #aaa">/2018</span>    | 57<span style="color: #aaa">/228</span>    |
| Lee          |                            134 | <span style="color: #6BAA75">↓ -14</span> | 488<span style="color: #aaa">/1383</span>    | 41<span style="color: #aaa">/97</span>     |
| Alachua      |                            121 | <span style="color: #EC4E20">↑ 5</span>   | 290<span style="color: #aaa">/1421</span>    | 30<span style="color: #aaa">/278</span>    |

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
