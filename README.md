Florida COVID-19 Data
================
2020-10-01 07:06:54

## Today

| When           | Day        | Positive | New Positive Since | Deaths | New Deaths Since | Total     |
| :------------- | :--------- | :------- | :----------------- | :----- | :--------------- | :-------- |
| Yesterday      | 2020-09-30 | 706,516  | 0                  | 14,488 | 0                | 5,301,184 |
| The Day Before | 2020-09-29 | 704,568  | 1,948              | 14,313 | 175              | 5,290,116 |
| Last Week      | 2020-09-24 | 693,040  | 13,476             | 13,961 | 527              | 5,179,499 |
| 2 Weeks Ago    | 2020-09-17 | 674,456  | 32,060             | 13,247 | 1,241            | 5,010,973 |

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
| All          |                           2097 | <span style="color: #6BAA75">↓ -1</span> | 14377<span style="color: #aaa">/46465</span> | 1338<span style="color: #aaa">/4665</span> |
| Miami-Dade   |                            269 |                                          | 2271<span style="color: #aaa">/6325</span>   | 207<span style="color: #aaa">/738</span>   |
| Broward      |                            186 |                                          | 1057<span style="color: #aaa">/4163</span>   | 119<span style="color: #aaa">/326</span>   |
| Hillsborough |                            147 |                                          | 547<span style="color: #aaa">/3259</span>    | 45<span style="color: #aaa">/327</span>    |
| Duval        |                            130 |                                          | 803<span style="color: #aaa">/2828</span>    | 104<span style="color: #aaa">/330</span>   |
| Orange       |                            112 |                                          | 1037<span style="color: #aaa">/3332</span>   | 130<span style="color: #aaa">/274</span>   |
| Palm Beach   |                            111 |                                          | 1328<span style="color: #aaa">/2722</span>   | 137<span style="color: #aaa">/280</span>   |
| Pinellas     |                             91 |                                          | 922<span style="color: #aaa">/2331</span>    | 57<span style="color: #aaa">/234</span>    |
| Polk         |                             87 |                                          | 337<span style="color: #aaa">/1312</span>    | 16<span style="color: #aaa">/128</span>    |
| Brevard      |                             71 |                                          | 396<span style="color: #aaa">/1213</span>    | 37<span style="color: #aaa">/128</span>    |
| Osceola      |                             70 | <span style="color: #6BAA75">↓ -1</span> | 269<span style="color: #aaa">/887</span>     | 31<span style="color: #aaa">/92</span>     |

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
