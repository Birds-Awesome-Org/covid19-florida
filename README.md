Florida COVID-19 Data
================
2020-09-03 19:15:54

## Today

| When        | Day        | Positive | New Positive Since | Deaths | New Deaths Since | Total     |
| :---------- | :--------- | :------- | :----------------- | :----- | :--------------- | :-------- |
| Today       | 2020-09-03 | 637,013  | 0                  | 11,800 | 0                | 4,717,696 |
| Yesterday   | 2020-09-02 | 633,442  | 3,571              | 11,651 | 149              | 4,693,802 |
| Last Week   | 2020-08-27 | 611,991  | 25,022             | 11,011 | 789              | 4,517,364 |
| 2 Weeks Ago | 2020-08-20 | 588,602  | 48,411             | 10,186 | 1,614            | 4,335,752 |

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
| All          |                           3439 | <span style="color: #6BAA75">↓ -86</span> | 14823<span style="color: #aaa">/45935</span> | 1244<span style="color: #aaa">/4777</span> |
| Miami-Dade   |                            631 | <span style="color: #EC4E20">↑ 20</span>  | 2275<span style="color: #aaa">/6288</span>   | 136<span style="color: #aaa">/796</span>   |
| Broward      |                            400 | <span style="color: #6BAA75">↓ -17</span> | 1092<span style="color: #aaa">/4140</span>   | 93<span style="color: #aaa">/392</span>    |
| Duval        |                            215 | <span style="color: #6BAA75">↓ -3</span>  | 933<span style="color: #aaa">/2848</span>    | 130<span style="color: #aaa">/316</span>   |
| Palm Beach   |                            214 | <span style="color: #EC4E20">↑ 3</span>   | 1239<span style="color: #aaa">/2787</span>   | 120<span style="color: #aaa">/271</span>   |
| Hillsborough |                            156 | <span style="color: #6BAA75">↓ -6</span>  | 679<span style="color: #aaa">/3050</span>    | 44<span style="color: #aaa">/340</span>    |
| Orange       |                            148 | <span style="color: #6BAA75">↓ -13</span> | 1068<span style="color: #aaa">/3320</span>   | 111<span style="color: #aaa">/261</span>   |
| Pinellas     |                            134 | <span style="color: #6BAA75">↓ -3</span>  | 813<span style="color: #aaa">/2226</span>    | 40<span style="color: #aaa">/262</span>    |
| Polk         |                            126 | <span style="color: #6BAA75">↓ -7</span>  | 319<span style="color: #aaa">/1268</span>    | 20<span style="color: #aaa">/119</span>    |
| Gadsden      |                            121 |                                           | 202<span style="color: #aaa">/751</span>     | 0<span style="color: #aaa">/0</span>       |
| Lee          |                             97 | <span style="color: #6BAA75">↓ -36</span> | 359<span style="color: #aaa">/1492</span>    | 23<span style="color: #aaa">/116</span>    |

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
