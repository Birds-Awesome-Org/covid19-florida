Florida COVID-19 Data
================
2020-08-07 15:22:32

## Today

| When           | Day        | Positive | New Positive Since | Deaths | New Deaths Since | Total     |
| :------------- | :--------- | :------- | :----------------- | :----- | :--------------- | :-------- |
| Yesterday      | 2020-08-06 | 510,389  | 0                  | 7,871  | 0                | 3,857,336 |
| The Day Before | 2020-08-05 | 502,739  | 7,650              | 7,751  | 120              | 3,814,884 |
| Last Week      | 2020-07-31 | 470,386  | 40,003             | 6,966  | 905              | 3,628,088 |
| 2 Weeks Ago    | 2020-07-24 | 402,312  | 108,077            | 5,768  | 2,103            | 3,276,636 |

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
| All          |                           7145 | <span style="color: #6BAA75">↓ -314</span> | 13897<span style="color: #aaa">/46009</span> | 1081<span style="color: #aaa">/5109</span> |
| Miami-Dade   |                           1600 | <span style="color: #6BAA75">↓ -22</span>  | 1697<span style="color: #aaa">/6763</span>   | 113<span style="color: #aaa">/887</span>   |
| Broward      |                           1021 | <span style="color: #6BAA75">↓ -19</span>  | 945<span style="color: #aaa">/4292</span>    | 62<span style="color: #aaa">/466</span>    |
| Palm Beach   |                            436 | <span style="color: #6BAA75">↓ -18</span>  | 1408<span style="color: #aaa">/2800</span>   | 108<span style="color: #aaa">/309</span>   |
| Hillsborough |                            383 | <span style="color: #6BAA75">↓ -14</span>  | 533<span style="color: #aaa">/3308</span>    | 33<span style="color: #aaa">/366</span>    |
| Duval        |                            372 | <span style="color: #6BAA75">↓ -35</span>  | 928<span style="color: #aaa">/2833</span>    | 94<span style="color: #aaa">/347</span>    |
| Orange       |                            350 | <span style="color: #6BAA75">↓ -33</span>  | 970<span style="color: #aaa">/3434</span>    | 92<span style="color: #aaa">/280</span>    |
| Pinellas     |                            279 | <span style="color: #6BAA75">↓ -14</span>  | 626<span style="color: #aaa">/2256</span>    | 53<span style="color: #aaa">/234</span>    |
| Polk         |                            251 | <span style="color: #6BAA75">↓ -18</span>  | 308<span style="color: #aaa">/1318</span>    | 6<span style="color: #aaa">/152</span>     |
| Lee          |                            206 | <span style="color: #EC4E20">↑ 3</span>    | 280<span style="color: #aaa">/1503</span>    | 34<span style="color: #aaa">/107</span>    |
| Escambia     |                            164 | <span style="color: #6BAA75">↓ -10</span>  | 401<span style="color: #aaa">/1094</span>    | 6<span style="color: #aaa">/141</span>     |

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
