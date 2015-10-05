ats-harmonised-sds
===========================

Abstract Test Suite for "Harmonised Spatial Data Services"
as defined in the Technical Guidance for INSPIRE Spatial Data Services and services allowing spatial data services to be invoked.

*Note*: This ATS is in draft stage, none of the tests have an official INSPIRE MIG approval.

## External document references

| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
| INT SDS <a name="ref_INT_SDS"></a> | [Commission Regulation (EU) No 1089/2010 of 23 November 2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=OJ:L:2010:323:FULL&from=EN)
| INT SDS AMD <a name="ref_INT_SDS_AMD"></a> | [Commission Regulation (EU) No 1312/2014 of 10 December 2014 amending Regulation (EU) No 1089/2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32014R1312&from=EN)
| IR NS <a name="ref_IR_NS"></a>   | [Commission Regulation (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32009R0976&from=EN)
| IR NS AMD <a name="ref_IR_NS_AMD"></a> | [Commission Regulation (EU) No 1311/2014 of 10 December 2014 amending Regulation (EC) No 976/2009 as regards the definition of an INSPIRE metadata element](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32014R1311&from=EN)
| TG SDS <a name="ref_TG_SDS"></a> | [Technical Guidance for INSPIRE Spatial Data Services and services allowing spatial data services to be invoked](http://inspire.jrc.ec.europa.eu/documents/Spatial_Data_Services/TG_for_INSPIRE_SDS_3_1.pdf)
| ISO 19118 <a name="ref_ISO_19118"></a> | [ISO 19118:2011 Geographic information – Encoding](http://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=44212)

## TG Requirement coverage

Based on requirement numbering in [TG SDS](#ref_TG_SDS).

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 13     | Encoding follows [ISO 19118](#ref_ISO_19118) | | |
| 14     | Encoding follows [INT SDS](#ref_INT_SDS) annexes | | |
| 15     | Provide operations in the metadata   | | |
| 16     | Provide "Get Harmonised Spatial Data Service Metadata" operation | | |
| 17     | Provide a link to "Get Harmonised Spatial Data Service Metadata" | | |
| 18     | SDS Metadata shall follow the INSPIRE SDS XML Schema | | |

## Tests

The ATS for the "TG Conformance Class 3: Implementation of Spatial Data Services compliant with Harmonisation Requirements where practicable"
includes all the tests in the [ATS Invocable SDS](/inspire-eu-validation/ats-invocable-sds),
[ATS for Interoperable SDS](/inspire-eu-validation/ats-interoperable-sds), and additionally
the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |



## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
gmd | http://www.isotc211.org/2005/gmd
gml | http://www.opengis.net/gml/3.2
inspire\_common| http://inspire.ec.europa.eu/schemas/common/1.0
inspire\_dls   | http://inspire.ec.europa.eu/schemas/inspire_dls/1.0
ows | http://www.opengis.net/ows/1.1
xlink          | http://www.w3.org/1999/xlink
