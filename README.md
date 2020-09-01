Florida COVID-19 Data
================
2020-09-01 07:13:10

## Today

| When           | Day        | Positive | New Positive Since | Deaths | New Deaths Since | Total     |
| :------------- | :--------- | :------- | :----------------- | :----- | :--------------- | :-------- |
| Yesterday      | 2020-08-31 | 623,471  | 0                  | 11,331 | 0                | 4,615,539 |
| The Day Before | 2020-08-30 | 621,586  | 1,885              | 11,263 | 68               | 4,599,608 |
| Last Week      | 2020-08-25 | 605,502  | 17,969             | 10,717 | 614              | 4,466,524 |
| 2 Weeks Ago    | 2020-08-18 | 579,932  | 43,539             | 9,893  | 1,438            | 4,279,040 |

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

| County       | Current COVID Hospitalizations | Change Since Yesterday | Available Hospital Beds                      | Available ICU Beds                         |
| :----------- | -----------------------------: | :--------------------- | :------------------------------------------- | :----------------------------------------- |
| All          |                           3736 |                        | 16546<span style="color: #aaa">/43856</span> | 1477<span style="color: #aaa">/4519</span> |
| Miami-Dade   |                            682 |                        | 2543<span style="color: #aaa">/6016</span>   | 184<span style="color: #aaa">/751</span>   |
| Broward      |                            427 |                        | 1152<span style="color: #aaa">/3973</span>   | 106<span style="color: #aaa">/373</span>   |
| Duval        |                            230 |                        | 1089<span style="color: #aaa">/2655</span>   | 136<span style="color: #aaa">/305</span>   |
| Hillsborough |                            186 |                        | 765<span style="color: #aaa">/3008</span>    | 71<span style="color: #aaa">/298</span>    |
| Orange       |                            184 |                        | 1143<span style="color: #aaa">/3265</span>   | 118<span style="color: #aaa">/254</span>   |
| Palm Beach   |                            178 |                        | 1386<span style="color: #aaa">/2593</span>   | 145<span style="color: #aaa">/255</span>   |
| Pinellas     |                            142 |                        | 1018<span style="color: #aaa">/2113</span>   | 92<span style="color: #aaa">/217</span>    |
| Polk         |                            139 |                        | 400<span style="color: #aaa">/1212</span>    | 21<span style="color: #aaa">/115</span>    |
| Gadsden      |                            133 |                        | 199<span style="color: #aaa">/754</span>     | 0<span style="color: #aaa">/0</span>       |
| Lee          |                            117 |                        | 483<span style="color: #aaa">/1366</span>    | 24<span style="color: #aaa">/116</span>    |

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
