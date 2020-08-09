Florida COVID-19 Data
================
2020-08-09 19:07:47

## Today

| When        | Day        | Positive | New Positive Since | Deaths | New Deaths Since | Total     |
| :---------- | :--------- | :------- | :----------------- | :----- | :--------------- | :-------- |
| Today       | 2020-08-09 | 532,806  | 0                  | 8,315  | 0                | 3,985,663 |
| Yesterday   | 2020-08-08 | 526,577  | 6,229              | 8,238  | 77               | 3,945,872 |
| Last Week   | 2020-08-02 | 487,132  | 45,674             | 7,206  | 1,109            | 3,720,997 |
| 2 Weeks Ago | 2020-07-26 | 423,855  | 108,951            | 5,972  | 2,343            | 3,386,503 |

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

| County       | Current COVID Hospitalizations | Change Since Yesterday                     | Available Hospital Beds                      | Available ICU Beds                         |
| :----------- | -----------------------------: | :----------------------------------------- | :------------------------------------------- | :----------------------------------------- |
| All          |                           6848 | <span style="color: #6BAA75">↓ -268</span> | 15714<span style="color: #aaa">/43890</span> | 1230<span style="color: #aaa">/4928</span> |
| Miami-Dade   |                           1503 | <span style="color: #6BAA75">↓ -84</span>  | 1891<span style="color: #aaa">/6584</span>   | 136<span style="color: #aaa">/848</span>   |
| Broward      |                            909 | <span style="color: #6BAA75">↓ -113</span> | 1068<span style="color: #aaa">/4122</span>   | 67<span style="color: #aaa">/440</span>    |
| Palm Beach   |                            428 | <span style="color: #EC4E20">↑ 6</span>    | 1487<span style="color: #aaa">/2686</span>   | 126<span style="color: #aaa">/290</span>   |
| Duval        |                            385 | <span style="color: #EC4E20">↑ 14</span>   | 1028<span style="color: #aaa">/2712</span>   | 101<span style="color: #aaa">/340</span>   |
| Hillsborough |                            352 | <span style="color: #6BAA75">↓ -31</span>  | 758<span style="color: #aaa">/3100</span>    | 79<span style="color: #aaa">/337</span>    |
| Orange       |                            336 | <span style="color: #6BAA75">↓ -27</span>  | 1071<span style="color: #aaa">/3285</span>   | 87<span style="color: #aaa">/285</span>    |
| Pinellas     |                            259 | <span style="color: #6BAA75">↓ -17</span>  | 713<span style="color: #aaa">/2166</span>    | 64<span style="color: #aaa">/223</span>    |
| Polk         |                            233 | <span style="color: #EC4E20">↑ 2</span>    | 406<span style="color: #aaa">/1223</span>    | 25<span style="color: #aaa">/143</span>    |
| Lee          |                            187 | <span style="color: #6BAA75">↓ -14</span>  | 397<span style="color: #aaa">/1392</span>    | 40<span style="color: #aaa">/101</span>    |
| Escambia     |                            167 | <span style="color: #EC4E20">↑ 2</span>    | 494<span style="color: #aaa">/1001</span>    | 17<span style="color: #aaa">/130</span>    |

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
