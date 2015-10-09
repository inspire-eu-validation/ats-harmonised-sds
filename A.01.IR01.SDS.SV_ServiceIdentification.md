# A.01.IR01.SDS.SV_ServiceIdentification

**Purpose**: To find services fit to be consumed by given client applications, it's necessary to be able to discover if a Spatial Data Service is classified as ```harmonised```.

**Prerequisites**

* The metadata record for the service needs to pass as a valid ISO 19139 metadata record (schema validation) including both ```gmd``` and the ```srv``` schemas (see [namespaces](README.md#namespaces)).
* The metadata record for the service needs to pass as a valid XML document against the INSPIRE SDS extended metadata XML Schema (inspire\_sds\_gmd).

**Test method**

* Check that at least one [category element](#sds_category) exists. If it does, pass the test. Otherwise fail the test.

**Reference(s)**

* [TG SDS](README.md#ref_TG_SDS), section 4.5.1

**Test type**: Automated

**Notes**

* It's assumed that for ```invocable``` and ```interoperable``` SDSes, additional category elements are used, so that all the "super class" categories are also included. If they are not, the test for the "super class" CCs will not pass.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
category element <a name="sds\_category"></a> | /gmd:MD_Metadata/gmd:identificationInfo/inspire\_sds\_gmd:SV_ServiceIdentification[child::inspire\_sds\_gmd:category='harmonised']
