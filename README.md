Florida COVID-19 Data
================
2020-10-02 19:08:25

## Today

| When        | Day        | Positive | New Positive Since | Deaths | New Deaths Since | Total     |
| :---------- | :--------- | :------- | :----------------- | :----- | :--------------- | :-------- |
| Today       | 2020-10-02 | 711,804  | 0                  | 14,730 | 0                | 5,351,521 |
| Yesterday   | 2020-10-01 | 709,144  | 2,660              | 14,619 | 111              | 5,325,835 |
| Last Week   | 2020-09-25 | 695,887  | 15,917             | 14,083 | 647              | 5,205,994 |
| 2 Weeks Ago | 2020-09-18 | 677,660  | 34,144             | 13,387 | 1,343            | 5,038,261 |

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
| All          |                           2056 | <span style="color: #6BAA75">↓ -24</span> | 15326<span style="color: #aaa">/46056</span> | 1388<span style="color: #aaa">/4631</span> |
| Miami-Dade   |                            277 | <span style="color: #6BAA75">↓ -3</span>  | 2342<span style="color: #aaa">/6231</span>   | 192<span style="color: #aaa">/752</span>   |
| Broward      |                            204 | <span style="color: #EC4E20">↑ 2</span>   | 1045<span style="color: #aaa">/4130</span>   | 124<span style="color: #aaa">/315</span>   |
| Hillsborough |                            144 | <span style="color: #6BAA75">↓ -2</span>  | 565<span style="color: #aaa">/3230</span>    | 22<span style="color: #aaa">/353</span>    |
| Duval        |                            126 | <span style="color: #6BAA75">↓ -2</span>  | 987<span style="color: #aaa">/2791</span>    | 110<span style="color: #aaa">/329</span>   |
| Orange       |                            111 | <span style="color: #6BAA75">↓ -9</span>  | 1108<span style="color: #aaa">/3322</span>   | 150<span style="color: #aaa">/254</span>   |
| Palm Beach   |                            105 | <span style="color: #6BAA75">↓ -5</span>  | 1282<span style="color: #aaa">/2738</span>   | 137<span style="color: #aaa">/265</span>   |
| Pinellas     |                            101 | <span style="color: #EC4E20">↑ 13</span>  | 1203<span style="color: #aaa">/2496</span>   | 77<span style="color: #aaa">/220</span>    |
| Polk         |                             79 | <span style="color: #6BAA75">↓ -12</span> | 333<span style="color: #aaa">/1313</span>    | 17<span style="color: #aaa">/153</span>    |
| Brevard      |                             76 |                                           | 424<span style="color: #aaa">/1173</span>    | 25<span style="color: #aaa">/142</span>    |
| Osceola      |                             72 | <span style="color: #6BAA75">↓ -1</span>  | 256<span style="color: #aaa">/887</span>     | 29<span style="color: #aaa">/100</span>    |

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
