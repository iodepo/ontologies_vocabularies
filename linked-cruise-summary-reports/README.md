# Ontologies & Vocabularies: Linked Cruise Summary Reports
This vocabulary describes the classes and predicates needed to represent Cruise Summary Reports as Linked Data.

### 01 May 2020

### IRI: `http://purl.org/org/iode/po/voc/cruise-summary-reports`

**Editors:**
  - [Adam Leadbetter](https://github.com/adamml), Marine Institue, Ireland
  - [Rob Thomas](https://github.com/robthomas-marine), Marine Institute, Ireland
  
**Contributors:**
  - Bob Arko, Columbia University, Lamont-Doherty Earth Observatory, USA
  - [Cynthia Chandler](https://github.com/cynDC42), Woods Hole Oceanographic Institution, USA

## Contents
1. [Namespaces Used](#namespaces-used)
1. [Classes](#classes)
1. [Attributes](#attributes)
1. [Acknowledgments](#acknowledgments)
1. [References](#references)
    1. [Normative References](#normative-references)
    1. [Informative References](#informative-references)

## Namespaces Used
| Prefix | Namespace IRI | Definition |
|:-------|:--------------|:-----------|
| csr | http://purl.org/org/iode/po/voc/cruise-summary-reports# | The Linked Cruise Summary Report namespace |
| dct | http://www.purl.org/dc/terms/ | All metadata terms maintained by the Dublin Core Metadata Initiative |
| gl | http://schema.geolink.org/1.0/base/main# | The GeoLink Ontology Design Patterns for marine sciences data markup |
| gsp | http://www.opengis.net/ont/geosparql# | A Geographic Query Language for Resource Description Framework Data |
| marineTLO | http://www.ics.forth.gr/isl/ontology/MarineTLO/ | The Marine Top Level Ontology, used here as a basis of uppler-level ontology alignment |
| prov | http://www.w3.org/ns/prov# | The PROV Ontology expresses the PROV Data Model using the Web Ontology Language |
| rdf | http://www.w3.org/1999/02/22-rdf-syntax-ns# | The Resource Description Framework Concepts Vocabulary |
| rdfs | http://www.w3.org/2000/01/rdf-schema# | A data-modelling vocabulary for Resource Description Framework data |
| sdo | http://schema.org/ | Schema.org vocabulary for publishing structured data on the Web |
| vann | http://purl.org/vocab/vann/ | A vocabulary for annotating descriptions of vocabularies with examples and usage notes |
| xsd | http://www.w3.org/2001/XMLSchema# | Used in XML Schemas for the elements, attributes, and types of the W3C XML Schema Recommendation itself. |

## Classes
[Cruise](#cruise) | [Operation](#operation) | [Port Call](#port-call) | [Summary Report](#summary-report)

### Cruise

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#Cruise`

A cruise is a port-to-port activity undertaken by a research vessel, or other ship equipped with instrumentation for oceanographic or marine scientific observations. A cruise is not limited to scintific operations but may also be an activity to relocate the vessel to another port for operational reasons.

**Is subclass of**
[gl:Cruise](http://schema.geolink.org/1.0/base/main#), [marineTLO:BC61_Capture_Activity](http://www.ics.forth.gr/isl/ontology/MarineTLO/BC61_Capture_Activity), [prov:Activity](http://www.w3.org/ns/prov#Activity), [sdo:Event](http://schema.org/Event)

**Described with properties**

[hasChiefScientist](#haschiefscientist) | [hasCoChiefScientist](#hascochiefscientist) | [hasDOI](#hasdOI) | [hasEndPortCall](#hasendportcall) | [hasIdentifier](#hasidentifier) | [hasStartPortCall](#hasstartportcall) | [hasTrack](#hastrack) | [isUndertakenBy](#isundertakenby) | [label](#label)

**In range of**

[describesCruise](#describescruise), [undertook](#undertook)

### Operation

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#Operation`

An activity (such as a measurement or mooring) occuring on a research vessel cruise, flight, deployment, etc...

**Is subclass of**
[prov:Activity](http://www.w3.org/ns/prov#Activity)

**Described with properties**

**In range of**

### Port Call

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#PortCall`

A designated, specific port visited by a Vessel for some significant reason - the start or end of a mission; transfer of passengers, goods, or equipment.

**Is subclass of**
[prov:InstantaneousEvent](http://www.w3.org/ns/prov#InstantaneousEvent)

**Described with properties**
[atPort](#atport) | [hasTimeStamp](#hastimestamp)

**In range of**

### Summary Report

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

**Described with properties**

**In range of**

## Attributes

[additionalDocumentation](#additionaldocumentation) | [atPort](#atport) | [created](#created) | [describesCruise](#describescruise) | [description](#description) | [generalOceanArea](#generaloceanarea) | [hasChiefScientist](#haschiefscientist) | [hasCoChiefScientist](#hascochiefscientist) | [hasDataset](#hasdataset) | [hasDOI](#hasdoi) | [hasEndPortCall](#hasendportcall) | [hasIdentifier](#hasidentifier) | [hasOperation](#hasoperation) | [hasProgram](#hasprogram) | [hasStartPortCall](#hasstartportcall) | [hasTimeStamp](#hastimestamp) | [hasTrack](#hastrack) | [isUndertakenBy](#isundertakenby) | [label](#isundertakenby) | [marsdenSquare](#marsdensquare) | [responsibleLaboratory](#responsiblelaboratory) | [spatial](#spatial) | [specificGeographicArea](#specificgeographicarea) | [trackChart](#trackchart) | [undertook](#undertook)

### additionalDocumentation

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

**Has domain**

**Has range**

### atPort

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#atPort`

Describes the port at which a PortCall takes place. It is advised to use a term from a controlled vocabulary describing a gazetteer entry for the port as the object for the triple.

**Is sub-property of**
[prov:atLocation](http://www.w3.org/ns/prov#atLocation)

**Has domain**
[PortCall](#portcall)

**Has range**
[xsd:anyURI](http://www.w3.org/2001/XMLSchema#anyURI)

### created

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

**Has domain**

**Has range**

### describesCruise

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

**Has domain**

**Has range**

### description

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

**Has domain**

**Has range**

### generalOceanArea

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

**Has domain**

**Has range**

### hasChiefScientist

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#hasChiefScientist`

The prov:Agent at the range of this predicate should represent the chief scientist undertaking the research cruise

**Is sub-property of**
[prov:wasAssociatedWith](http://www.w3.org/ns/prov#wasAssociatedWith)

**Has domain**
[Cruise](#cruise)

**Has range**
[prov:Agent](http://www.w3.org/ns/prov#Agent)

### hasCoChiefScientist

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#hasCoChiefScientist`

The prov:Agent at the range of this predicate should represent one of a number of co-chief scientists undertaking the research cruise

**Is sub-property of**
[prov:wasAssociatedWith](http://www.w3.org/ns/prov#wasAssociatedWith)

**Has domain**
[Cruise](#cruise)

**Has range**
[prov:Agent](http://www.w3.org/ns/prov#Agent)

### hasDataset

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

**Has domain**

**Has range**

### hasDOI

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#hasDOI`

Links a Cruise object to a persistent identifier assigned to it (such as a digital object identifier [doi])

**Is sub-property of**
[dct:identifier](http://www.purl.org/dc/terms/identifier)

**Has domain**
[Cruise](#cruise)

**Has range**
[rdfs:Literal](http://www.w3.org/2000/01/rdf-schema#Literal), [xsd:anyURI](http://www.w3.org/2001/XMLSchema#anyURI)

### hasEndPortCall

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#hasEndPortCall`

Links a Cruise object to the PortCall object which describes the event which ended the Cruise

**Is sub-property of**
[prov:qualifiedEnd](http://www.w3.org/ns/prov#qualifiedEnd)

**Has domain**
[Cruise](#cruise)

**Has range**
[PortCall](#portcall)

### hasIdentifier

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#hasIdentifier`

An identifier given to the research cruise by the organisation responsible for the research cruise taking place

**Is sub-property of**
[rdfs:label](http://www.w3.org/2000/01/rdf-schema#label)

**Has domain**
[Cruise](#cruise)

**Has range**
[rdfs:Literal](http://www.w3.org/2000/01/rdf-schema#Literal)

### hasOperation

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

**Has domain**

**Has range**

### hasProgram

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

**Has domain**

**Has range**

### hasStartPortCall

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#hasStartPortCall`

Links a Cruise object to the PortCall object which describes the event which started the Cruise

**Is sub-property of**
[prov:qualifiedEnd](http://www.w3.org/ns/prov#qualifiedEnd)

**Has domain**
[Cruise](#cruise)

**Has range**
[PortCall](#portcall)

### hasTimeStamp

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#hasTimeStamp`

Describes the time at which a PortCall occurred

**Is sub-property of**
[prov:atTime](http://www.w3.org/ns/prov#atTime)

**Has domain**
[PortCall](#portcall)

**Has range**
[xsd:date],[xsd:dateTime]

### hasTrack

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#hasTrack`

Provides a representation of the track taken by the research vessel during the Cruise as a Well Known Text literal.

**Has domain**
[Cruise](#cruise)

**Has range**
[gsp:wktLiteral](http://www.opengis.net/ont/geosparql#wktLiteral)

### isUndertakenBy

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

The prov:Agent at the range of this predicate should represent the vessel undertaking the research cruise. Ideally, a controlled vocabulary resource should be used to instantiate the prov:Agent, such as the International Council for the Exploration of the Seas platform code list.

**Is sub-property of**
[prov:used](http://www.w3.org/ns/prov#used)

**Has domain**
[Cruise](#cruise)

**Has range**
[prov:Agent](http://www.w3.org/ns/prov#Agent)

**Has inverse**
[undertook](#undertook)

### label

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

**Has domain**

**Has range**

### marsdenSquare

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

**Has domain**

**Has range**

### responsibleLaboratory

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

**Has domain**

**Has range**

### spatial

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

**Has domain**

**Has range**

### specificGeographicArea

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

**Has domain**

**Has range**

### trackChart

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

**Has domain**

**Has range**

### undertook

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#undertook`

The prov:Agent at the domain of this predicate should represent the vessel which undertook the Cruise at its range. Ideally, a controlled vocabulary resource should be used to instantiate the prov:Agent, such as the International Council for the Exploration of the Seas platform code list.

**Is sub-property of**
[prov:wasGeneratedBy](http://www.w3.org/ns/prov#wasGeneratedBy)

**Has domain**
[prov:Agent](http://www.w3.org/ns/prov#Agent)

**Has range**
[Cruise](#cruise)

**Has inverse**
[isUndertakenBy](#isUndertakenBy)

## Acknowledgments
This work was developed under the SeaDataCloud project (2016-2020), grant agreement 730960, EU H2020 programme. The publication of this work via GitHub was made possible with the support of the International Oceanographic Data and Information Exchange of UNESCO's Intergovernmental Oceanographic Commission.

The advice of Simon Cox of the Commonwealth Scientific and Industrial Research Organisation, Australia was greatly appreciated at various stages in the ontology design phase.

The assistance of Arno Lambert and Peter Pissiersens at the Project Office of the International Oceanographic Data and Information Exchange of UNESCO's Intergovernmental Oceanographic Commission was invaluable in the web publishing of the vocabulary resource.

## References

### Normative references

### Informative References
