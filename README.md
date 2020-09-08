Florida COVID-19 Data
================
2020-09-08 12:13:58

## Today

| When        | Day        | Positive | New Positive Since | Deaths | New Deaths Since | Total     |
| :---------- | :--------- | :------- | :----------------- | :----- | :--------------- | :-------- |
| Today       | 2020-09-08 | 650,092  | 0                  | 12,067 | 0                | 4,816,873 |
| Yesterday   | 2020-09-07 | 648,269  | 1,823              | 12,023 | 44               | 4,801,684 |
| Last Week   | 2020-09-01 | 631,040  | 19,052             | 11,521 | 546              | 4,675,866 |
| 2 Weeks Ago | 2020-08-25 | 605,502  | 44,590             | 10,717 | 1,350            | 4,466,524 |

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

| County       | Current COVID Hospitalizations | Change Since Yesterday                  | Available Hospital Beds                      | Available ICU Beds                         |
| :----------- | -----------------------------: | :-------------------------------------- | :------------------------------------------- | :----------------------------------------- |
| All          |                           3163 | <span style="color: #EC4E20">↑ 6</span> | 17552<span style="color: #aaa">/42658</span> | 1544<span style="color: #aaa">/4410</span> |
| Miami-Dade   |                            535 | <span style="color: #EC4E20">↑ 6</span> | 2564<span style="color: #aaa">/5866</span>   | 190<span style="color: #aaa">/741</span>   |
| Broward      |                            345 |                                         | 1189<span style="color: #aaa">/3925</span>   | 100<span style="color: #aaa">/363</span>   |
| Duval        |                            199 |                                         | 1236<span style="color: #aaa">/2551</span>   | 154<span style="color: #aaa">/283</span>   |
| Hillsborough |                            174 |                                         | 833<span style="color: #aaa">/2858</span>    | 82<span style="color: #aaa">/284</span>    |
| Palm Beach   |                            171 |                                         | 1510<span style="color: #aaa">/2544</span>   | 146<span style="color: #aaa">/251</span>   |
| Orange       |                            149 |                                         | 1251<span style="color: #aaa">/3084</span>   | 119<span style="color: #aaa">/253</span>   |
| Pinellas     |                            131 |                                         | 1041<span style="color: #aaa">/2093</span>   | 79<span style="color: #aaa">/219</span>    |
| Gadsden      |                            124 |                                         | 208<span style="color: #aaa">/745</span>     | 0<span style="color: #aaa">/0</span>       |
| Polk         |                            110 |                                         | 451<span style="color: #aaa">/1158</span>    | 32<span style="color: #aaa">/104</span>    |
| Lee          |                             97 |                                         | 522<span style="color: #aaa">/1335</span>    | 28<span style="color: #aaa">/112</span>    |

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
