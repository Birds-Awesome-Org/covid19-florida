Florida COVID-19 Data
================
2020-10-28 12:09:41

## Today

| When        | Day        | Positive | New Positive Since | Deaths | New Deaths Since | Total     |
| :---------- | :--------- | :------- | :----------------- | :----- | :--------------- | :-------- |
| Today       | 2020-10-28 | 790,426  | 0                  | 16,775 | 0                | 6,053,154 |
| Yesterday   | 2020-10-27 | 786,311  | 4,115              | 16,709 | 66               | 6,014,492 |
| Last Week   | 2020-10-21 | 762,533  | 27,893             | 16,413 | 362              | 5,779,019 |
| 2 Weeks Ago | 2020-10-14 | 741,632  | 48,794             | 15,788 | 987              | 5,615,247 |

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
| All          |                           2337 | <span style="color: #6BAA75">↓ -3</span>  | 14422<span style="color: #aaa">/46924</span> | 1439<span style="color: #aaa">/4662</span> |
| Miami-Dade   |                            319 | <span style="color: #6BAA75">↓ -12</span> | 2328<span style="color: #aaa">/6339</span>   | 196<span style="color: #aaa">/744</span>   |
| Broward      |                            206 | <span style="color: #6BAA75">↓ -3</span>  | 938<span style="color: #aaa">/4265</span>    | 92<span style="color: #aaa">/372</span>    |
| Hillsborough |                            157 | <span style="color: #EC4E20">↑ 2</span>   | 734<span style="color: #aaa">/3371</span>    | 41<span style="color: #aaa">/362</span>    |
| Palm Beach   |                            140 | <span style="color: #EC4E20">↑ 8</span>   | 1240<span style="color: #aaa">/2796</span>   | 153<span style="color: #aaa">/236</span>   |
| Orange       |                            136 | <span style="color: #6BAA75">↓ -6</span>  | 1081<span style="color: #aaa">/3370</span>   | 139<span style="color: #aaa">/265</span>   |
| Duval        |                            133 | <span style="color: #EC4E20">↑ 16</span>  | 897<span style="color: #aaa">/2835</span>    | 108<span style="color: #aaa">/329</span>   |
| Pinellas     |                            127 | <span style="color: #6BAA75">↓ -4</span>  | 857<span style="color: #aaa">/2278</span>    | 66<span style="color: #aaa">/236</span>    |
| Polk         |                             89 | <span style="color: #EC4E20">↑ 11</span>  | 360<span style="color: #aaa">/1331</span>    | 60<span style="color: #aaa">/122</span>    |
| Osceola      |                             83 | <span style="color: #EC4E20">↑ 1</span>   | 271<span style="color: #aaa">/895</span>     | 39<span style="color: #aaa">/84</span>     |
| Alachua      |                             71 | <span style="color: #EC4E20">↑ 8</span>   | 270<span style="color: #aaa">/1468</span>    | 48<span style="color: #aaa">/260</span>    |

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
