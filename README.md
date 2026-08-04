# LEDE 2026 Final project

**Data gathering**

<p>Data used for this project are publicly available, published by Serbian Interior Affairs Ministry at Serbian Government open data portal, here https://data.gov.rs/sr/datasets/podatsi-o-saobratshajnim-nezgodama-po-politsijskim-upravama-i-opshtinama/. Available data are until June 30.</p>

**Data preparation for work**

<p>All data are separated per year, meaning that every year is a different data sheet. As there were no .csv version of those (at least I did not see them) I downloaded .xlsx versions. For every year, I downloaded data sheet, uploaded it on Google Sheets, removed categories I did not plan to work with, translated the rest and combine it all in one huge data sheet. Than, I downloaded that data sheet as a .csv file, so I can work with it in Jupyter notebook.</p>

**Data cleaning**

<p>Besides the cleaning work I did manually while translating and merging all data, now I used pandas to add some new categories that I wanted to work with. The original data sheet had only Date & Time category. With pandas I was able to extract more categories from it:
Date: separate dates in Month/Day/Year format
Time: separate time slots
Date in month: meaning Month/Day format of date, to see are there some dates that are repeating throughout years on which accidents are happening more often
Month: Months by name
Weekday: Days in week by name</p>

**Data analyze**

<p>Now I could compare different datasets in pandas and to check things like when (which date or month) the majority of accidents happened, when the majority of death cases happened and so on. These analysis can be seen in the notebook attached in this repo.</p>

**Visualisation**

<p>I used Datawrapper, with API keys we got, so it take the data directly from my notebook. I removed that part from the notebook attached here.</p>

**Data problems**

<p>Available data are separated in different categories and each of them has its own subcategories, but in some cases it is not all clear what those mean in practice. For example, police divide damage in traffic accident into subcategories death, injuries and material damage, and it is not clear how they categorized cases in which two things happened at once. Also, datasets lack more in-depth information about causes of TAs, so that part would have to be investigated in a separate project.</p>




