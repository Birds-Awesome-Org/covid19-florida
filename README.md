Florida COVID-19 Data
================
2020-09-26 19:13:37

## Today

| When        | Day        | Positive | New Positive Since | Deaths | New Deaths Since | Total     |
| :---------- | :--------- | :------- | :----------------- | :----- | :--------------- | :-------- |
| Today       | 2020-09-26 | 698,682  | 0                  | 14,190 | 0                | 5,235,007 |
| Yesterday   | 2020-09-25 | 695,887  | 2,795              | 14,083 | 107              | 5,205,994 |
| Last Week   | 2020-09-19 | 681,233  | 17,449             | 13,450 | 740              | 5,068,554 |
| 2 Weeks Ago | 2020-09-12 | 661,571  | 37,111             | 12,756 | 1,434            | 4,901,680 |

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
| All          |                           2099 | <span style="color: #6BAA75">↓ -22</span> | 16728<span style="color: #aaa">/44785</span> | 1417<span style="color: #aaa">/4715</span> |
| Miami-Dade   |                            268 | <span style="color: #6BAA75">↓ -7</span>  | 3490<span style="color: #aaa">/6057</span>   | 188<span style="color: #aaa">/746</span>   |
| Broward      |                            215 |                                           | 1141<span style="color: #aaa">/3994</span>   | 98<span style="color: #aaa">/368</span>    |
| Hillsborough |                            141 | <span style="color: #6BAA75">↓ -1</span>  | 568<span style="color: #aaa">/3162</span>    | 46<span style="color: #aaa">/334</span>    |
| Orange       |                            122 | <span style="color: #EC4E20">↑ 5</span>   | 1080<span style="color: #aaa">/3288</span>   | 135<span style="color: #aaa">/269</span>   |
| Duval        |                            120 | <span style="color: #6BAA75">↓ -6</span>  | 886<span style="color: #aaa">/2910</span>    | 128<span style="color: #aaa">/306</span>   |
| Palm Beach   |                            111 | <span style="color: #6BAA75">↓ -17</span> | 1400<span style="color: #aaa">/2620</span>   | 147<span style="color: #aaa">/253</span>   |
| Pinellas     |                             98 | <span style="color: #6BAA75">↓ -1</span>  | 932<span style="color: #aaa">/2192</span>    | 65<span style="color: #aaa">/217</span>    |
| Polk         |                             84 | <span style="color: #EC4E20">↑ 2</span>   | 400<span style="color: #aaa">/1228</span>    | 29<span style="color: #aaa">/115</span>    |
| Alachua      |                             70 | <span style="color: #6BAA75">↓ -4</span>  | 272<span style="color: #aaa">/1431</span>    | 34<span style="color: #aaa">/274</span>    |
| Osceola      |                             67 | <span style="color: #EC4E20">↑ 5</span>   | 281<span style="color: #aaa">/869</span>     | 35<span style="color: #aaa">/88</span>     |

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
