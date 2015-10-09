# A.03.IR15.operations.declared

**Purpose**: A harmonised spatial data service shall have well documented
interfaces and list the end points for each operation to enable machine to machine communication.

**Prerequisites**

* The metadata record for the service needs to pass as a valid ISO 19139 metadata record (schema validation) including both ```gmd``` and the ```srv``` schemas (see [namespaces](README.md#namespaces)).

**Test method**

At least one of the following three checks must pass:

1. [OperationMetadata elements](#operation_metadata) must not be empty.
2. There must be at least one [Self-describing access point URL](#self-describing_access_point_url), or
3. There must be at least one [Get Harmonised Service Metadata URL](#get_service_metadata_url)

**Reference(s)**

**Test type**: Automated

**Notes**

* It's impossible to automatically validate that all operations of a service and all of the  parameters of each operation are described in a machine readable way, regardless of the check options chosen.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
OperationMetadata elements <a name="operation_metadata"></a> | /gmd:MD_Metadata/gmd:identificationInfo/srv:SV_ServiceIdentification/srv:containsOperations/srv:SV_OperationMetadata
Self-describing access point URL <a name="self-describing_access_point_url"></a> | /gmd:MD\_Metadata/gmd:distributionInfo/gmd:MD\_Distribution/gmd:transferOptions/gmd:MD\_DigitalTransferOptions/gmd:onLine/gmd:CI\_OnlineResource[child::gmd:linkage/gmd:URL and child::gmd:function/gmd:CI\_OnLineFunctionCode[@codeList='http://inspire.ec.europa.eu/draft-schemas/resources/Codelist/gmxCodelist.xml#INSPIRE_CI_OnLineFunctionCode' and (@codeListValue='accessPoint-selfDescribing']]/gmd:linkage/gmd:URL
Get Harmonised Service Metadata URL <a name="get_service_metadata_url"></a> | /gmd:MD\_Metadata/gmd:distributionInfo/gmd:MD\_Distribution/gmd:transferOptions/gmd:MD\_DigitalTransferOptions/gmd:onLine/gmd:CI\_OnlineResource[child::gmd:linkage/gmd:URL and child::gmd:function/gmd:CI\_OnLineFunctionCode[@codeList='http://inspire.ec.europa.eu/draft-schemas/resources/Codelist/gmxCodelist.xml#INSPIRE_CI_OnLineFunctionCode' and (@codeListValue=providesServiceMetadata']]/gmd:linkage/gmd:URL
