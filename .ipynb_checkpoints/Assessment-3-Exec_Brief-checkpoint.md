# Front Matter: CASA0013: Foundations of Spatial Data Science

## Title of Briefing: Drivers behind the geographic concentration on Airbnb listings across London

### Student ID: 21203086 

### Word Count: 1490

# Executive Briefing

## Table of contents

Executive Summary

Background

Data Analysis

Conclusion

Bibliography

Appendices


## Executive summary


Do certain areas of London trigger the geographic concentration of Airbnb listings across London?

This report seeks to describe and analyse the spread of Airbnb listings in London by identifying common components characterising areas displaying a high concentration of listings. First, visualisations seek to quantify the current picture of Airbnb listings across the city, followed by a categorisation of the Greater London Wards by their concentration of listings (low, medium, high). A subsequent geodemographic classification of the areas attempts to identify patterns explaining the presence or absence of listings. Finally, this paper discusses how these results and similar approaches can inform policies that will regulate Airbnb listings in a targeted manner.

Key findings:

* Airbnb listings numbers, albeit high, have significantly dropped during the Covid 19 pandemic
* As expected, the highest concentration of Airbnb listings is noted in central London areas, but Airbnb listings scatter even to the city’s fringes.
* In a more detailed geodemographic profiling of London areas, the most affected areas are central, affluent with a young population and predominantly white while the least are rural, older and no flats.


## Background

What started as an alternative way of holidays, sharing, and experiencing the local in an authentic and original way, has turned into a booming economy with questionable effects. Airbnb listings have all over the world been professionalised and intensified and are now cluttering cities while the housing crisis remains a major problem.  The fundamental right to a roof is challenged as housing prices rise rapidly across cities, especially in the years after the financial crisis of 2008 (Gleeson, 2021). The notorious housing problem of London (Travers, Sims and Bosetti, 2016) has strongly contributed to spatial inequality and transformed the urban landscape (Shabrina, Arcaute and Batty, 2019) by pushing residents out of inner London to more affordable regions. 

While many factors generate the complicated matter of the housing crisis, research to date shows that Airbnb and similar platforms contribute to rising rent prices (Barron, Kung and Proserpio, no date; Horn and Merante, 2017) and remove available housing from the market by injecting short term rentals in residential areas (Shabrina, Arcaute and Batty, 2022). 

Many have called for policies to control unregulated platforms like Airbnb, but communities, researchers and local authorities have struggled to grasp and interpret the sudden growth and unprecedented model of the sharing economies (Horn and Merante, 2017). This paper argues that in order to successfully and appropriately regulate Airbnb in a city like London, the phenomenon and its complexity need first to be fully understood and studied. Therefore, this analysis will first present the current status of Airbnb listings across London and identify the most affected areas before attempting a more in-depth analysis.

Drawing from the most recent available data on the Inside Airbnb website (October 2021), London currently has a total of just over 67,900 listings. Roughly 20% (13,600 listings) have had a review in the past year, which is used as an indicator for currently active listings. These numbers seem to be in stark contrast with pre-pandemic figures: 80,770 listings in May 2019 (Temperton, 2020). While it is difficult to confirm the accuracy of these numbers since they do not derive from official Airbnb data, it is evident that the Covid 19 pandemic has strongly affected the sharing economy.


<figure>
<img src="Active_Airbnb_map_comparison_dots2.png" alt="Trulli" style="width:100%">
<figcaption align = "centre"><b>Fig.1 - Comparison maps: Airbnb listings in London in 2021 (Data: Inside Airbnb) </b></figcaption>
</figure>

The maps in Figure 1 illustrate the magnitude of the Airbnb listings count across the area of London. Even the outer Boroughs seem to host a considerable number of listings. While the currently active listings (last posted review within the past year) are significantly less, the emerging pattern remains the same: a very high concentration of listings in the centre spread outwards in smaller intensity. More specifically, looking at the density of Airbnb listings across London Boroughs, Figure 2 confirms that inner London Boroughs concentrate most of the listings: Westminster, Kensington and Chelsea, and Tower Hamlets are the three most affected areas, closely followed by Hackney, Islington, and Camden.

<figure>
<img src="Barplot_Listings_Density_per_Borough.png" alt="Trulli" style="width:50%">
<figcaption align = "centre"><b>Fig.2 - Barplot: Airbnb listings Density per London Borough(2021) (Data: Inside Airbnb) </b></figcaption>
</figure>

## Data Analysis

This analysis will use the listings density (active and inactive) as the measure of spatial penetration of Airbnb listings in London. However, the London Boroughs are relatively large spatial units that do not capture more fine-grained variation across the city's urban fabric. Therefore, the analysis will be based on smaller spatial units, the Greater London Wards. 

<figure>
<img src="Log Airbnb_density.png" alt="Trulli" style="width:100%">
<figcaption align = "centre"><b>Fig.3 - Airbnb listings density(log) in London in 2021 (Data: Inside Airbnb) </b></figcaption>
</figure>

Plotting the Log transformed listings density across the London Wards (Figure 3) reveals:

* High concentration of listings in the central north and west parts of London
* Medium concentration of listings in the immediately surrounding areas and mostly within the inner London division with a light but a noticeable shift towards the west. 
* Low concentration of listings in Outer London.  

While the concentration of listings in central London is certainly expected and explained by the attractiveness of these areas to tourists, in terms of proximity to major sights of the city, the rather surprising expansion of listings towards even the outer areas of the city have been noted and studied in previous research. (Quattrone et al., 2016; Shabrina, Arcaute and Batty, 2019) 

In the attempt to better understand where and why listings are concentrating, this analysis employs a form of statistical clustering known as K-Means to group the London Wards based on the concentration of Airbnb listings and variables deriving from the London Wards Profiles from the London Datastore that provides key summary measures on a multitude of categories such as population, diversity, and housing. 


| name | description | category | source |
| ----------- | ----------- | ----------- | ----------- |
| Median age |Median Age (2013)| demographic | London Wards Profiles |
| Population density | Population density (2013) | geodemographic | London Wards Profiles |
| BAME percentage | Percentage of BAME (2011) | demographic | London Wards Profiles |
| Median income | Median Household income estimate (2012/13) | economic | London Wards Profiles |
| Flat percentage | Percentage of Flat, maisonette or apartment (2011) | housing | London Wards Profiles |
| Higher Education percentage | Percentage with Level 4 qualifications and above (2011) | socialdemographic | London Wards Profiles |
| Transport | Average Public Transport Accessibility score (2014) | location/attactiveness | London Wards Profiles |
| Listings Density | Airbnb listings density per area (2021) | Airbnb | Inside Airbnb |

<b> Fig.4 - Table listing the variables used </b>

<figure>
<img src="Variables_maps.png" alt="Trulli" style="width:100%">
<figcaption align = "centre"><b>Fig.5 - Distribution of variables across London (Data: London Ward Profiles, Inside Airbnb) </b></figcaption>
</figure>

The selection of the variables as listed in Figure 4, whilst not exhaustive, aims to capture a range of geodemographic, social, and economic characteristics of the subregions following similar studies (Quattrone et al., 2016, 2018).

The distribution of the data is heavily skewed in some instances and with different ranges and units (Appendix A), which requires standardisation so that none of the variables dominates the classification process. The number of clusters is set to 4 based on the results from the Elbow and Silhouette plot (Appendix B)

Evaluating the distribution of each variable per cluster (Appendix C) in conjunction with the geographic distribution of the clusters across London (Figure 8), the resulting clusters can be interpreted as (LOW, MEDIUM, HIGH indicate the concentration of listings):

**Cluster 1:  LOW - suburban middle class**

These are suburban areas, in the outer edges of London, where population density is low, and few houses are flats and transport connections are bad. The population is older, predominantly white, with average income and low higher education levels.

**Cluster 2:  HIGH - densely populated diverse inner London**

Mostly inner London areas with good transport links, with some exceptions. These areas have a high population density together with a high concentration of flats. Characterised by younger, diverse population with an average income and average higher education levels. 

**Cluster 3: MEDIUM - affluent and attractive city areas**

Almost entirely inner London areas with relatively good transport links. Medium population density levels as well as medium flat concentration. The population age is average, predominantly white with high income and high education levels. 

**Cluster 4: LOW - deprived outer areas**

Areas just outside inner London, with exceptions, that have bad transport links. Medium population density levels and few flats. The population here is mostly Black, Asian and Minority Ethnic with low income and education levels.


<figure>
<img src="Cluster_map.png" alt="Trulli" style="width:100%">
<figcaption align = "centre"><b>Fig.5 - Distribution of variables across London (Data: London Ward Profiles, Inside Airbnb) </b></figcaption>
</figure>

## Conclusion

The classification of London wards suggests that Airbnb listings are concentrated not only in central areas with good transport links but also in areas with young, white, well-off residents and where flats are more frequent than other types of housings. These findings align with Quattrone et al. regression and prediction models, which identify central areas with young and talented people most prone to high Airbnb listings concentration.  (Quattrone et al., 2018)

This rather simple and generic classification of the London areas can form the basis for a much more detailed and complicated analysis, implementing different methods such as a multiple linear regression while testing for spatial autocorrelation. Using a more extensive set of variables and perhaps even smaller spatial units might refine the results and produce new insights.

While the results strongly depend on the researcher’s choices, methods, and assumptions, it is essential to note that the data themselves have significant limitations: the London Profiles data extracted from the 2011 census is now outdated, while the Inside Airbnb data has questionable accuracy, and any interpretation needs to bear in mind the still ongoing Covid 19 pandemic.

The findings indicate that the policies and regulations imposed on the sharing economy need to take into account the variations in listings concentration and neighbourhood characteristics which will help protect the most susceptible areas. Creating incentives for either hosts to register their short-term lets on a government/local authority platform or Airbnb to share their data so that an accurate and valid database can be created informing the much-needed further research on this topic. 


# Bibliography

Barron, K., Kung, E. and Proserpio, D. (no date) The Effect of Home-Sharing on House Prices and Rents: Evidence from Airbnb. Available at: https://ssrn.com/abstract=3006832.

Gleeson, J. (2021) GLA Housing and Land Housing in London 2021. Available at: www.london.gov.uk.

Horn, K. and Merante, M. (2017) “Is home sharing driving up rents? Evidence from Airbnb in Boston,” Journal of Housing Economics, 38, pp. 14–24. [doi:10.1016/j.jhe.2017.08.002.](https://www.sciencedirect.com/science/article/abs/pii/S1051137717300876)

Inside Airbnb,2021. Available at: http://insideairbnb.com/get-the-data.html (Accessed: 22 December 2021).

London Datastore, 2021, Ward Profiles and Atlas. Available at: https://data.london.gov.uk/dataset/ward-profiles-and-atlas (Accessed: 22 December 2021).

Quattrone, G. et al. (2016) “Who benefits from the ‘sharing’ economy of airbnb?,” in 25th International World Wide Web Conference, WWW 2016. International World Wide Web Conferences Steering Committee, pp. 1385–1393. [doi:10.1145/2872427.2874815.](https://www.researchgate.net/publication/301874810_Who_Benefits_from_the_Sharing_Economy_of_Airbnb)

Quattrone, G. et al. (2018) “Analyzing and predicting the spatial penetration of Airbnb in U.S. cities,” EPJ Data Science, 7(1). [doi:10.1140/epjds/s13688-018-0156-6.](https://epjdatascience.springeropen.com/articles/10.1140/epjds/s13688-018-0156-6)

Shabrina, Z., Arcaute, E. and Batty, M. (2019) “Airbnb’s disruption of the housing structure in London.” Available at: http://arxiv.org/abs/1903.11205.

Shabrina, Z., Arcaute, E. and Batty, M. (2022) “Airbnb and its potential impact on the London housing market,” Urban Studies, 59(1), pp. 197–221. [doi:10.1177/0042098020970865.](https://journals.sagepub.com/doi/full/10.1177/0042098020970865)

Travers, T., Sims, S. and Bosetti, N. (no date) HOUSING AND INEQUALITY IN LONDON. Available at: www.centreforlondon.org.

Temperton, J. (2020) Airbnb has devoured London – and here’s the data that proves it. Available at: https://www.wired.co.uk/article/airbnb-london-short-term-rentals (Accessed: 04 January 2022).


# Appendices

### Appendix A

<figure>
<img src="Variables_distribution_hist.png" alt="Trulli" style="width:80%">
<figcaption align = "centre"><b> Histograms </b></figcaption>
</figure>

### Appendix B

<figure>
<img src="Silhouette_elbow_plot.png" alt="Trulli" style="width:80%">
<figcaption align = "centre"><b> Silhouette and Elbow plot </b></figcaption>
</figure>

### Appendix C

<figure>
<img src="Variable_distribution_clusters.png" alt="Trulli" style="width:80%">
<figcaption align = "centre"><b> Variable distribuτιion per cluster </b></figcaption>
</figure>


```python

```


```python

```


```python

```


```python

```


```python

```
