# A.04.IR16.IR17.link.to.get.harmonised.service.metadata

**Purpose**: Access point for retrieving technical Capabilities of a harmonised SDS should be discoverable via it's metadata description.

**Prerequisites**

* The metadata record for the service needs to pass as a valid ISO 19139 metadata record (schema validation) including both ```gmd``` and the ```srv``` schemas (see [namespaces](README.md#namespaces)).

**Test method**

Let [Get Harmonised Service Metadata URL](#get_service_metadata_url) be ```url-list```. For each ```url``` in ```url-list```:
* Fetch the resource pointed to by ```url```. If document could be fetched, pass the test.
* If none of the ```url```s could be resolved to a document, fail the test.

**Reference(s)**

**Test type**: Automated

**Notes**

* There are no requirements for the structure and contents of the Harmonised Service Metadata documents in [TG SDS](README.md#ref_TG_SDS), only a few examples are provided. Thus it's impossible to automatically validate these documents.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Get Harmonised Service Metadata URL <a name="get_service_metadata_url"></a> | /gmd:MD\_Metadata/gmd:distributionInfo/gmd:MD\_Distribution/gmd:transferOptions/gmd:MD\_DigitalTransferOptions/gmd:onLine/gmd:CI\_OnlineResource[child::gmd:linkage/gmd:URL and child::gmd:function/gmd:CI\_OnLineFunctionCode[@codeList='http://inspire.ec.europa.eu/draft-schemas/resources/Codelist/gmxCodelist.xml#INSPIRE_CI_OnLineFunctionCode' and (@codeListValue=providesServiceMetadata']]/gmd:linkage/gmd:URL
