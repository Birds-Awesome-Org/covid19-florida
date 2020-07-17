Florida COVID-19 Data
================
2020-07-17 19:05:45

## Today

| When        | Day        | Positive | New Positive Since | Deaths | New Deaths Since | Total     |
| :---------- | :--------- | :------- | :----------------- | :----- | :--------------- | :-------- |
| Today       | 2020-07-17 | 327,241  | 0                  | 4,912  | 0                | 2,880,768 |
| Yesterday   | 2020-07-16 | 315,775  | 11,466             | 4,782  | 130              | 2,815,618 |
| Last Week   | 2020-07-10 | 244,151  | 83,090             | 4,203  | 709              | 2,421,627 |
| 2 Weeks Ago | 2020-07-03 | 178,594  | 148,647            | 3,785  | 1,127            | 2,081,360 |

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

| County       | Current COVID Hospitalizations | Change Since Yesterday                     | Available Hospital Beds                      | Available ICU Beds                        |
| :----------- | -----------------------------: | :----------------------------------------- | :------------------------------------------- | :---------------------------------------- |
| All          |                           8961 | <span style="color: #6BAA75">↓ -134</span> | 13228<span style="color: #aaa">/47302</span> | 993<span style="color: #aaa">/5163</span> |
| Miami-Dade   |                           1904 | <span style="color: #EC4E20">↑ 1</span>    | 1686<span style="color: #aaa">/6970</span>   | 132<span style="color: #aaa">/852</span>  |
| Broward      |                           1199 | <span style="color: #6BAA75">↓ -2</span>   | 945<span style="color: #aaa">/4444</span>    | 65<span style="color: #aaa">/445</span>   |
| Palm Beach   |                            633 | <span style="color: #6BAA75">↓ -37</span>  | 1077<span style="color: #aaa">/3110</span>   | 96<span style="color: #aaa">/326</span>   |
| Orange       |                            625 | <span style="color: #EC4E20">↑ 19</span>   | 974<span style="color: #aaa">/3447</span>    | 67<span style="color: #aaa">/310</span>   |
| Duval        |                            489 | <span style="color: #6BAA75">↓ -32</span>  | 907<span style="color: #aaa">/3030</span>    | 96<span style="color: #aaa">/344</span>   |
| Hillsborough |                            465 | <span style="color: #6BAA75">↓ -77</span>  | 663<span style="color: #aaa">/3328</span>    | 35<span style="color: #aaa">/355</span>   |
| Pinellas     |                            428 | <span style="color: #6BAA75">↓ -6</span>   | 516<span style="color: #aaa">/2385</span>    | 41<span style="color: #aaa">/251</span>   |
| Polk         |                            299 | <span style="color: #EC4E20">↑ 2</span>    | 260<span style="color: #aaa">/1381</span>    | 11<span style="color: #aaa">/147</span>   |
| Lee          |                            258 | <span style="color: #EC4E20">↑ 10</span>   | 270<span style="color: #aaa">/1518</span>    | 15<span style="color: #aaa">/124</span>   |
| Collier      |                            195 | <span style="color: #6BAA75">↓ -1</span>   | 178<span style="color: #aaa">/739</span>     | 25<span style="color: #aaa">/56</span>    |

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
