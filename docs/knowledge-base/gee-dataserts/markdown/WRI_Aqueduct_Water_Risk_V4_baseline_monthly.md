



* [Home](https://developers.google.com/)
* [Earth Engine Data Catalog](https://developers.google.com/earth-engine/datasets)
* [All datasets](https://developers.google.com/earth-engine/datasets/catalog)





 
 
 Send feedback
 
 

WRI Aqueduct Baseline Monthly Version 4\.0


 
 Stay organized with collections
 

 
 Save and categorize content based on your preferences.
============================================================================================================================================








Dataset Availability
2010\-01\-01T00:00:00Z–2080\-12\-31T23:59:59Z
Dataset Provider


[World Resources Institute](https://www.wri.org/data/aqueduct-global-maps-40-data)



Earth Engine Snippet

FeatureCollection
  


`ee.FeatureCollection("WRI/Aqueduct_Water_Risk/V4/baseline_monthly")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WRI/WRI_Aqueduct_Water_Risk_V4_baseline_monthly)



 
 
 
 FeatureView
   


`ui.Map.FeatureViewLayer("WRI/Aqueduct_Water_Risk/V4/baseline_monthly_FeatureView")` 
[open\_in\_new](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WRI/WRI_Aqueduct_Water_Risk_V4_baseline_monthly_FeatureView)





Tags


[aqueduct](/earth-engine/datasets/tags/aqueduct)
[flood](/earth-engine/datasets/tags/flood)
[monitoring](/earth-engine/datasets/tags/monitoring)
[surface\-ground\-water](/earth-engine/datasets/tags/surface-ground-water)
[table](/earth-engine/datasets/tags/table)
[wri](/earth-engine/datasets/tags/wri)








#### Description



Aqueduct 4\.0 is the latest iteration of WRI's water risk framework designed
to translate complex hydrological data into intuitive indicators of water
related risk. This dataset has curated 13 water risk indicators for
quantity, quality and reputational concerns into a comprehensive framework.
For 5 of the 13 indicators, a global hydrological model called PCR\-GLOBWB 2
has been used to generate novel datasets on sub\-basic water supply.
The PCR\-GLOBWB 2 model is also used to project future sub\-basin water
conditions using CMIP6 climate forcings. The projections center around
three periods (2030, 2050, and 2080\) under three future scenarios
(business\-as\-usual SSP 3 RCP 7\.0, optimistic SSP 1 RCP 2\.6, and
pessimistic SSP 5 RCP 8\.5\).


The water risk indicators have been aggregated by category (quantity,
quality, reputational, and overall) into composite risk scores using
sector\-specific weighting schemes. In addition, select sub\-basin scores have
been aggregated into country and provincial administrative boundaries using
a weighted average approach, where sub\-basins with more demand have a higher
influence over the final administrative score.


The WRI Aqueduct baseline monthly dataset provides monthly data on key water
risk indicators which includes indicators such as baseline water stress,
baseline water depletion and interannual variability.This monthly data
allows for a more detailed analysis of water risk dynamics throughout the
year, which is crucial for understanding seasonal water scarcity, planning
for water management interventions, and adapting to changing water
availability patterns.


This [technical note](https://www.wri.org/research/aqueduct-40-updated-decision-relevant-global-water-risk-indicators)
explains in detail the framework, methodology, and data used
in developing Aqueduct Floods.





### Table Schema


**Table Schema**




| Name | Type | Description |
| --- | --- | --- |
| fid\_1 | INT | Feature Id |
| pfaf\_id | INT | Six digit Pfafstetter code for the [hydrological basin](https://hydrosheds.org/page/hydrobasins) |
| bwd\_01\_cat | INT | Baseline water depletion category for January |
| bwd\_01\_label | STRING | Baseline water depletion label for January |
| bwd\_01\_raw | DOUBLE | Baseline water depletion raw value for January |
| bwd\_01\_score | DOUBLE | Baseline water depletion score for January |
| bwd\_02\_cat | INT | Baseline water depletion category for February |
| bwd\_02\_label | STRING | Baseline water depletion label for February |
| bwd\_02\_raw | DOUBLE | Baseline water depletion raw value for February |
| bwd\_02\_score | DOUBLE | Baseline water depletion score for February |
| bwd\_03\_cat | INT | Baseline water depletion category for March |
| bwd\_03\_label | STRING | Baseline water depletion label for March |
| bwd\_03\_raw | DOUBLE | Baseline water depletion raw value for March |
| bwd\_03\_score | DOUBLE | Baseline water depletion score for March |
| bwd\_04\_cat | INT | Baseline water depletion category for April |
| bwd\_04\_label | STRING | Baseline water depletion label for April |
| bwd\_04\_raw | DOUBLE | Baseline water depletion raw value for April |
| bwd\_04\_score | DOUBLE | Baseline water depletion score for April |
| bwd\_05\_cat | INT | Baseline water depletion category for May |
| bwd\_05\_label | STRING | Baseline water depletion label for May |
| bwd\_05\_raw | DOUBLE | Baseline water depletion raw value for May |
| bwd\_05\_score | DOUBLE | Baseline water depletion score for May |
| bwd\_06\_cat | INT | Baseline water depletion category for June |
| bwd\_06\_label | STRING | Baseline water depletion label for June |
| bwd\_06\_raw | DOUBLE | Baseline water depletion raw value for June |
| bwd\_06\_score | DOUBLE | Baseline water depletion score for June |
| bwd\_07\_cat | INT | Baseline water depletion category for July |
| bwd\_07\_label | STRING | Baseline water depletion label for July |
| bwd\_07\_raw | DOUBLE | Baseline water depletion raw value for July |
| bwd\_07\_score | DOUBLE | Baseline water depletion score for July |
| bwd\_08\_cat | INT | Baseline water depletion category for August |
| bwd\_08\_label | STRING | Baseline water depletion label for August |
| bwd\_08\_raw | DOUBLE | Baseline water depletion raw value for August |
| bwd\_08\_score | DOUBLE | Baseline water depletion score for August |
| bwd\_09\_cat | INT | Baseline water depletion category for September |
| bwd\_09\_label | STRING | Baseline water depletion label for September |
| bwd\_09\_raw | DOUBLE | Baseline water depletion raw value for September |
| bwd\_09\_score | DOUBLE | Baseline water depletion score for September |
| bwd\_10\_cat | INT | Baseline water depletion category for October |
| bwd\_10\_label | STRING | Baseline water depletion label for October |
| bwd\_10\_raw | DOUBLE | Baseline water depletion raw value for October |
| bwd\_10\_score | DOUBLE | Baseline water depletion score for October |
| bwd\_11\_cat | INT | Baseline water depletion category for November |
| bwd\_11\_label | STRING | Baseline water depletion label for November |
| bwd\_11\_raw | DOUBLE | Baseline water depletion raw value for November |
| bwd\_11\_score | DOUBLE | Baseline water depletion score for November |
| bwd\_12\_cat | INT | Baseline water depletion category for December |
| bwd\_12\_label | STRING | Baseline water depletion label for December |
| bwd\_12\_raw | DOUBLE | Baseline water depletion raw value for December |
| bwd\_12\_score | DOUBLE | Baseline water depletion score for December |
| bws\_01\_cat | INT | Baseline water stress category for January |
| bws\_01\_label | STRING | Baseline water stress label for January |
| bws\_01\_raw | DOUBLE | Baseline water stress raw value for January |
| bws\_01\_score | DOUBLE | Baseline water stress score for January |
| bws\_02\_cat | INT | Baseline water stress category for February |
| bws\_02\_label | STRING | Baseline water stress label for February |
| bws\_02\_raw | DOUBLE | Baseline water stress raw value for February |
| bws\_02\_score | DOUBLE | Baseline water stress score for February |
| bws\_03\_cat | INT | Baseline water stress category for March |
| bws\_03\_label | STRING | Baseline water stress label for March |
| bws\_03\_raw | DOUBLE | Baseline water stress raw value for March |
| bws\_03\_score | DOUBLE | Baseline water stress score for March |
| bws\_04\_cat | INT | Baseline water stress category for April |
| bws\_04\_label | STRING | Baseline water stress label for April |
| bws\_04\_raw | DOUBLE | Baseline water stress raw value for April |
| bws\_04\_score | DOUBLE | Baseline water stress score for April |
| bws\_05\_cat | INT | Baseline water stress category for May |
| bws\_05\_label | STRING | Baseline water stress label for May |
| bws\_05\_raw | DOUBLE | Baseline water stress raw value for May |
| bws\_05\_score | DOUBLE | Baseline water stress score for May |
| bws\_06\_cat | INT | Baseline water stress category for June |
| bws\_06\_label | STRING | Baseline water stress label for June |
| bws\_06\_raw | DOUBLE | Baseline water stress raw value for June |
| bws\_06\_score | DOUBLE | Baseline water stress score for June |
| bws\_07\_cat | INT | Baseline water stress category for July |
| bws\_07\_label | STRING | Baseline water stress label for July |
| bws\_07\_raw | DOUBLE | Baseline water stress raw value for July |
| bws\_07\_score | DOUBLE | Baseline water stress score for July |
| bws\_08\_cat | INT | Baseline water stress category for August |
| bws\_08\_label | STRING | Baseline water stress label for August |
| bws\_08\_raw | DOUBLE | Baseline water stress raw value for August |
| bws\_08\_score | DOUBLE | Baseline water stress score for August |
| bws\_09\_cat | INT | Baseline water stress category for September |
| bws\_09\_label | STRING | Baseline water stress label for September |
| bws\_09\_raw | DOUBLE | Baseline water stress raw value for September |
| bws\_09\_score | DOUBLE | Baseline water stress score for September |
| bws\_10\_cat | INT | Baseline water stress category for October |
| bws\_10\_label | STRING | Baseline water stress label for October |
| bws\_10\_raw | DOUBLE | Baseline water stress raw value for October |
| bws\_10\_score | DOUBLE | Baseline water stress score for October |
| bws\_11\_cat | INT | Baseline water stress category for November |
| bws\_11\_label | STRING | Baseline water stress label for November |
| bws\_11\_raw | DOUBLE | Baseline water stress raw value for November |
| bws\_11\_score | DOUBLE | Baseline water stress score for November |
| bws\_12\_cat | INT | Baseline water stress category for December |
| bws\_12\_label | STRING | Baseline water stress label for December |
| bws\_12\_raw | DOUBLE | Baseline water stress raw value for December |
| bws\_12\_score | DOUBLE | Baseline water stress score for December |
| iav\_01\_cat | INT | Interannual variability category for January |
| iav\_01\_label | STRING | Interannual variability label for January |
| iav\_01\_raw | DOUBLE | Interannual variability raw value for January |
| iav\_01\_score | DOUBLE | Interannual variability score for January |
| iav\_02\_cat | INT | Interannual variability category for February |
| iav\_02\_label | STRING | Interannual variability label for February |
| iav\_02\_raw | DOUBLE | Interannual variability raw value for February |
| iav\_02\_score | DOUBLE | Interannual variability score for February |
| iav\_03\_cat | INT | Interannual variability category for March |
| iav\_03\_label | STRING | Interannual variability label for March |
| iav\_03\_raw | DOUBLE | Interannual variability raw value for March |
| iav\_03\_score | DOUBLE | Interannual variability score for March |
| iav\_04\_cat | INT | Interannual variability category for April |
| iav\_04\_label | STRING | Interannual variability label for April |
| iav\_04\_raw | DOUBLE | Interannual variability raw value for April |
| iav\_04\_score | DOUBLE | Interannual variability score for April |
| iav\_05\_cat | INT | Interannual variability category for May |
| iav\_05\_label | STRING | Interannual variability label for May |
| iav\_05\_raw | DOUBLE | Interannual variability raw value for May |
| iav\_05\_score | DOUBLE | Interannual variability score for May |
| iav\_06\_cat | INT | Interannual variability category for June |
| iav\_06\_label | STRING | Interannual variability label for June |
| iav\_06\_raw | DOUBLE | Interannual variability raw value for June |
| iav\_06\_score | DOUBLE | Interannual variability score for June |
| iav\_07\_cat | INT | Interannual variability category for July |
| iav\_07\_label | STRING | Interannual variability label for July |
| iav\_07\_raw | DOUBLE | Interannual variability raw value for July |
| iav\_07\_score | DOUBLE | Interannual variability score for July |
| iav\_08\_cat | INT | Interannual variability category for August |
| iav\_08\_label | STRING | Interannual variability label for August |
| iav\_08\_raw | DOUBLE | Interannual variability raw value for August |
| iav\_08\_score | DOUBLE | Interannual variability score for August |
| iav\_09\_cat | INT | Interannual variability category for September |
| iav\_09\_label | STRING | Interannual variability label for September |
| iav\_09\_raw | DOUBLE | Interannual variability raw value for September |
| iav\_09\_score | DOUBLE | Interannual variability score for September |
| iav\_10\_cat | INT | Interannual variability category for October |
| iav\_10\_label | STRING | Interannual variability label for October |
| iav\_10\_raw | DOUBLE | Interannual variability raw value for October |
| iav\_10\_score | DOUBLE | Interannual variability score for October |
| iav\_11\_cat | INT | Interannual variability category for November |
| iav\_11\_label | STRING | Interannual variability label for November |
| iav\_11\_raw | DOUBLE | Interannual variability raw value for November |
| iav\_11\_score | DOUBLE | Interannual variability score for November |
| iav\_12\_cat | INT | Interannual variability category for December |
| iav\_12\_label | STRING | Interannual variability label for December |
| iav\_12\_raw | DOUBLE | Interannual variability raw value for December |
| iav\_12\_score | DOUBLE | Interannual variability score for December |




### Terms of Use


**Terms of Use**


The WRI datasets are available without restriction
on use or distribution. WRI does request that the
user give proper attribution and identify WRI, where applicable,
as the source of the data. For more information check
[WRI's open data commitment](https://www.wri.org/data/open-data-commitment),




### Explore with Earth Engine


**Important:** 
 Earth Engine is a platform for petabyte\-scale scientific analysis and visualization of
 geospatial datasets, both for public benefit and for business and government users.
 Earth Engine is free to use for research, education, and nonprofit use. To get started, please
 [register for Earth Engine access.](https://console.cloud.google.com/earth-engine)



### Code Editor (JavaScript)



```
vardataset=
ee.FeatureCollection('WRI/Aqueduct_Water_Risk/V4/baseline_monthly');

varreds=ee.List([
'67000D','9E0D14','E32F27','F6553D','FCA082','FEE2D5'
]);

functionnormalize(value,min,max){
returnvalue.subtract(min).divide(ee.Number(max).subtract(min));
}
functionsetColor(feature,property,min,max,palette){
varvalue=normalize(feature.getNumber(property),min,max)
.multiply(palette.size())
.min(palette.size().subtract(1))
.max(0);
returnfeature.set({style:{color:palette.get(value.int())}});
}

varbws_cat_style=function(f){
returnsetColor(f,'bws_01_cat',-1,4,reds);
};

varwaterLand=ee.Image('NOAA/NGDC/ETOPO1').select('bedrock').gt(0.0);
varwaterLandBackground=
waterLand.visualize({palette:['cadetblue','lightgray']});
Map.addLayer(waterLandBackground);

// Baseline water stress
varpolygons=dataset.filter('bws_01_cat > -2').map(bws_cat_style);

Map.setCenter(10,20,4);

Map.addLayer(polygons.style({styleProperty:'style',pointSize:3}));
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WRI/WRI_Aqueduct_Water_Risk_V4_baseline_monthly)
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
varfvLayer=ui.Map.FeatureViewLayer(
'WRI/Aqueduct_Water_Risk/V4/baseline_monthly_FeatureView');

varvisParams={
isVisible:false,
pointSize:20,
rules:[{
// Baseline water stress with low category in January
filter:ee.Filter.eq('bws_01_cat',-1),
isVisible:true,
pointFillColor:{
property:'bws_01_cat',
mode:'linear',
palette:['f1eef6','d7b5d8','df65b0','ce1256'],
min:-1,
max:100
}
}]
};

fvLayer.setVisParams(visParams);
fvLayer.setName('Low Water Stress January');

Map.setCenter(-10,25,5);
Map.add(fvLayer);
```



[Open in Code Editor](https://code.earthengine.google.com/?scriptPath=Examples:Datasets/WRI/WRI_Aqueduct_Water_Risk_V4_baseline_monthly_FeatureView)


[WRI Aqueduct Baseline Monthly Version 4\.0](/earth-engine/datasets/catalog/WRI_Aqueduct_Water_Risk_V4_baseline_monthly)

Aqueduct 4\.0 is the latest iteration of WRI's water risk framework designed to translate complex hydrological data into intuitive indicators of water related risk. This dataset has curated 13 water risk indicators for quantity, quality and reputational concerns into a comprehensive framework. For 5 of the 13 indicators, a global …

 WRI/Aqueduct\_Water\_Risk/V4/baseline\_monthly,
 aqueduct,flood,monitoring,surface\-ground\-water,table,wri

2010\-01\-01T00:00:00Z/2080\-12\-31T23:59:59Z



 \-90 \-180 90 180
 



Google Earth Engine
https://developers.google.com/earth\-engine/datasets








