# A.02.IR01.DQ_DomainConsistency.report.for.classification

**Purpose**: To find services fit to be consumed by given client applications, it's necessary to be able to
discover if a Spatial Data Service is classified as ```harmonised```.

**Prerequisites**

* The metadata record for the service needs to pass as a valid ISO 19139 metadata record (schema validation) including both ```gmd``` and the ```srv``` schemas (see [namespaces](README.md#namespaces)).

**Test method**

* Check that there is at least one DQ_ConformanceResult returned from query [classification result harmonised](#result_harmonised). If so, pass the test. Otherwise fail the test.

**Reference(s)**

* [SDS ALT](README.md#ref_SDS_ALT), Example of XML encoding Category

**Test type**: Automated

**Notes**

* It's assumed, that separate ```gmd:report``` elements are provided for each passed classification ```invocable```, ```interoperable``` and ```harmonised``` that the service conforms to. Otherwise the tests for these "super class" CCes will not pass.
* It's assumed that the ```gmd:specification``` element refers to this conformance class only by using ```xlink:href``` attribute pointing to URL ```http://inspire.ec.europa.eu/conformanceClass/MD/1.4/SDS_Harmonised```, and any of it's children (like ```gmd:CI_Citation``` elements), if given, are ignored.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
classification result harmonised <a name="result_harmonised"></a> | /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:report/gmd:DQ_DomainConsistency/gmd:result/gmd:DQ_ConformanceResult[child::gmd:specification/@xlink:href='http://inspire.ec.europa.eu/conformanceClass/MD/1.4/SDS_Harmonised' and child::gmd:pass/gco:Boolean='true']
