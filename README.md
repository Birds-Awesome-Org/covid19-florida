Florida COVID-19 Data
================
2020-10-19 12:09:31

## Today

| When        | Day        | Positive | New Positive Since | Deaths | New Deaths Since | Total     |
| :---------- | :--------- | :------- | :----------------- | :----- | :--------------- | :-------- |
| Today       | 2020-10-19 | 756,727  | 0                  | 16,222 | 0                | 5,739,283 |
| Yesterday   | 2020-10-18 | 755,020  | 1,707              | 16,168 | 54               | 5,722,392 |
| Last Week   | 2020-10-12 | 736,024  | 20,703             | 15,599 | 623              | 5,567,283 |
| 2 Weeks Ago | 2020-10-05 | 717,874  | 38,853             | 14,886 | 1,336            | 5,412,683 |

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
| All          |                           2052 | <span style="color: #EC4E20">↑ 47</span>  | 17102<span style="color: #aaa">/44149</span> | 1594<span style="color: #aaa">/4405</span> |
| Miami-Dade   |                            264 | <span style="color: #EC4E20">↑ 8</span>   | 2539<span style="color: #aaa">/6043</span>   | 223<span style="color: #aaa">/723</span>   |
| Broward      |                            188 | <span style="color: #EC4E20">↑ 12</span>  | 1167<span style="color: #aaa">/4079</span>   | 99<span style="color: #aaa">/340</span>    |
| Hillsborough |                            139 | <span style="color: #EC4E20">↑ 4</span>   | 644<span style="color: #aaa">/3100</span>    | 56<span style="color: #aaa">/311</span>    |
| Orange       |                            122 | <span style="color: #6BAA75">↓ -14</span> | 1729<span style="color: #aaa">/3189</span>   | 152<span style="color: #aaa">/252</span>   |
| Duval        |                            118 | <span style="color: #EC4E20">↑ 2</span>   | 1096<span style="color: #aaa">/2671</span>   | 103<span style="color: #aaa">/318</span>   |
| Pinellas     |                            116 | <span style="color: #EC4E20">↑ 6</span>   | 1024<span style="color: #aaa">/2222</span>   | 73<span style="color: #aaa">/222</span>    |
| Palm Beach   |                             99 | <span style="color: #EC4E20">↑ 2</span>   | 1458<span style="color: #aaa">/2528</span>   | 159<span style="color: #aaa">/238</span>   |
| Osceola      |                             79 | <span style="color: #EC4E20">↑ 5</span>   | 311<span style="color: #aaa">/850</span>     | 38<span style="color: #aaa">/89</span>     |
| Polk         |                             76 | <span style="color: #EC4E20">↑ 3</span>   | 372<span style="color: #aaa">/1237</span>    | 43<span style="color: #aaa">/115</span>    |
| Brevard      |                             66 | <span style="color: #6BAA75">↓ -5</span>  | 463<span style="color: #aaa">/1140</span>    | 49<span style="color: #aaa">/117</span>    |

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
