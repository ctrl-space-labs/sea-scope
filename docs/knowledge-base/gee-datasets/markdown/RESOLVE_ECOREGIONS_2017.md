



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

RESOLVE Ecoregions 2017


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
=========================================================================================================================








Dataset Availability
2017\-04\-05T00:00:00Z–2017\-04\-05T00:00:00Z
Dataset Provider


[RESOLVE Biodiversity and Wildlife Solutions](https://ecoregions.appspot.com/)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("RESOLVE/ECOREGIONS/2017")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/RESOLVE/RESOLVE_ECOREGIONS_2017)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("RESOLVE/ECOREGIONS/2017_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/RESOLVE/RESOLVE_ECOREGIONS_2017_FeatureView)





Tags


[biodiversity](/earth-engine/datasets/tags/biodiversity)
[conservation](/earth-engine/datasets/tags/conservation)
[ecoregions](/earth-engine/datasets/tags/ecoregions)
[ecosystems](/earth-engine/datasets/tags/ecosystems)
[global](/earth-engine/datasets/tags/global)
[table](/earth-engine/datasets/tags/table)
habitats
protection
resolve








#### Description



The RESOLVE Ecoregions dataset, updated in 2017, offers a depiction of the 846 terrestrial
ecoregions that represent our living planet. View the stylized map at
[https://ecoregions2017\.appspot.com/](https://ecoregions2017.appspot.com/) or in
[Earth Engine](https://code.earthengine.google.com/b961ab2adfcb03c920aab63d86c49eb2).


Ecoregions, in the simplest definition, are ecosystems of regional extent.
Specifically, ecoregions represent distinct assemblages of biodiversity\-all
taxa, not just vegetation\-whose boundaries include the space required to
sustain ecological processes. Ecoregions provide a useful basemap for
conservation planning in particular because they draw on natural, rather
than political, boundaries, define distinct biogeographic assemblages and
ecological habitats within biomes, and assist in representation of Earth's
biodiversity.


This dataset is based on recent advances in biogeography \- the science
concerning the distribution of plants and animals. The original ecoregions
dataset has been widely used since its introduction in 2001, underpinning the
most recent analyses of the effects of global climate change on nature by
ecologists to the distribution of the world's beetles to modern conservation
planning.


The 846 terrestrial ecoregions are grouped into 14 biomes and 8 realms. Six
of these biomes are forest biomes and remaining eight are non\-forest biomes.
For the forest biomes, the geographic boundaries of the ecoregions
(Dinerstein et al., 2017\) and protected areas (UNEP\-WCMC 2016\) were
intersected with the Global Forest Change data (Hansen et al. 2013\) for the
years 2000 to 2015, to calculate percent of habitat in protected areas and
percent of remaining habitat outside protected areas. Likewise, the
boundaries of the non\-forest ecoregions and protected areas (UNEP\-WCMC 2016\)
were intersected with Anthropogenic Biomes data (Anthromes v2\) for the year
2000 (Ellis et al., 2010\) to identify remaining habitats inside and outside
the protected areas. Each ecoregion has a unique ID, area (sq. degrees), and NNH
(Nature Needs Half) categories 1\-4\. NNH categories are based on percent of
habitat in protected areas and percent of remaining habitat outside
protected areas.


1. Half Protected: More than 50% of the total ecoregion area is already
protected.
2. Nature Could Reach Half: Less than 50% of the total ecoregion area is
protected but the amount of remaining unprotected natural habitat could
bring protection to over 50% if new conservation areas are added to the
system.
3. Nature Could Recover: The amount of protected and unprotected natural
habitat remaining is less than 50% but more than 20%. Ecoregions in this
category would require restoration to reach Half Protected.
4. Nature Imperiled: The amount of protected and unprotected natural habitat
remaining is less than or equal to 20%. Achieving half protected is not
possible in the short term and efforts should focus on conserving
remaining, native habitat fragments.


The updated Ecoregions 2017 is the most\-up\-to\-date (as of February 2018\) dataset on remaining
habitat in each terrestrial ecoregion. It was released to chart progress towards
achieving the visionary goal of [Nature Needs Half](https://natureneedshalf.org/), to protect half of all
the land on Earth to save a living terrestrial biosphere.


Note \- a number of ecoregions are very complex polygons with over a million
vertices, such as Rock \& Ice. These ecoregions were split when necessary,
with attributes like Eco\_ID being preserved. If you'd like to see all
ecoregions that have been split, please [run this script](https://code.earthengine.google.com/7a437c78fc8cb46ec586bb4e2c10e526).





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| BIOME\_NAME | STRING | Biome name |
| BIOME\_NUM | DOUBLE | Biome number |
| COLOR | STRING | Color |
| COLOR\_BIO | STRING | Biome color |
| COLOR\_NNH | STRING | NNH color |
| ECO\_ID | DOUBLE | Ecoregion unique ID |
| ECO\_NAME | STRING | Ecoregion name |
| LICENSE | STRING | CC\-BY 4\.0 |
| NNH | DOUBLE | NNH category (1\-4\) based on percent of habitat in protected areas and percent of remaining habitat outside protected areas |
| NNH\_NAME | STRING | Half Protected, Nature Could Reach Half, Nature Could Recover, or Nature Imperiled |
| OBJECTID | DOUBLE | Object id |
| REALM | STRING | Realm name |
| SHAPE\_AREA | DOUBLE | Area of ecoregion polygon in square degrees |
| SHAPE\_LENG | DOUBLE | Length of ecoregion polygon in degrees |




### Terms of Use


**Terms of Use**


[CC\-BY\-4\.0](https://spdx.org/licenses/CC-BY-4.0.html)




### Citations



Citations:
* [Bioscience, An Ecoregions\-Based Approach to Protecting Half the
Terrestrial Realm](https://academic.oup.com/bioscience/article/67/6/534/3102935)
[doi:10\.1093/biosci/bix014](https://doi.org/10.1093/biosci/bix014)





### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varecoRegions=ee.FeatureCollection('RESOLVE/ECOREGIONS/2017');

// patch updated colors
varcolorUpdates=[
{ECO_ID:204,COLOR:'#B3493B'},
{ECO_ID:245,COLOR:'#267400'},
{ECO_ID:259,COLOR:'#004600'},
{ECO_ID:286,COLOR:'#82F178'},
{ECO_ID:316,COLOR:'#E600AA'},
{ECO_ID:453,COLOR:'#5AA500'},
{ECO_ID:317,COLOR:'#FDA87F'},
{ECO_ID:763,COLOR:'#A93800'},
];

// loop over all other features and create a new style property for styling
// later on
varecoRegions=ecoRegions.map(function(f){
varcolor=f.get('COLOR');
returnf.set({style:{color:color,width:0}});
});

// make styled features for the regions we need to update colors for,
// then strip them from the main asset and merge in the new feature
for(vari=0;i < colorUpdates.length;i++){
colorUpdates[i].layer=ecoRegions
.filterMetadata('ECO_ID','equals',colorUpdates[i].ECO_ID)
.map(function(f){
returnf.set({style:{color:colorUpdates[i].COLOR,width:0}});
});

ecoRegions=ecoRegions
.filterMetadata('ECO_ID','not_equals',colorUpdates[i].ECO_ID)
.merge(colorUpdates[i].layer);
}

// use style property to color shapes
varimageRGB=ecoRegions.style({styleProperty:'style'});

Map.setCenter(16,49,4);
Map.addLayer(imageRGB,{},'RESOLVE/ECOREGIONS/2017');
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/RESOLVE/RESOLVE_ECOREGIONS_2017)
### Visualize as a FeatureView



 A `FeatureView` is a view\-only, accelerated representation of a
 `FeatureCollection`. For more details, visit the
 [`FeatureView` documentation.](/earth-engine/guides/featureview_overview) 



**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
varfvLayer=ui.Map.FeatureViewLayer('RESOLVE/ECOREGIONS/2017_FeatureView');

varvisParams={
opacity:1,
polygonFillColor:{
property:'NNH_NAME',
categories:[
['Half Protected','blue'],
['Nature Could Reach Half Protected','green'],
['Nature Could Recover','yellow'],
['Nature Imperiled','orange']
],
defaultValue:'lightgrey'
}
};

fvLayer.setVisParams(visParams);
fvLayer.setName('Ecoregions (Nature Needs Half category)');

Map.setCenter(16,49,4);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/RESOLVE/RESOLVE_ECOREGIONS_2017_FeatureView)


[RESOLVE Ecoregions 2017](/earth-engine/datasets/catalog/RESOLVE_ECOREGIONS_2017)

The RESOLVE Ecoregions dataset, updated in 2017, offers a depiction of the 846 terrestrial ecoregions that represent our living planet. View the stylized map at https://ecoregions2017\.appspot.com/ or in Earth Engine. Ecoregions, in the simplest definition, are ecosystems of regional extent. Specifically, ecoregions represent distinct assemblages of biodiversity\-all taxa, not just …

 RESOLVE/ECOREGIONS/2017,
 biodiversity,conservation,ecoregions,ecosystems,global,table

2017\-04\-05T00:00:00Z/2017\-04\-05T00:00:00Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








