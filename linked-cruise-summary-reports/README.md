# Ontologies & Vocabularies: Linked Cruise Summary Reports
| | |
|-|-:|
| This vocabulary describes the classes and predicates needed to represent Cruise Summary Reports as Linked Data. | ![IOC Logo][ioc-logo] |

### 01 May 2020

### IRI: `http://purl.org/org/iode/po/voc/cruise-summary-reports`

**This version**
  - [http://purl.org/org/iode/po/voc/cruise-summary-reports/2020-05-01.md](http://purl.org/org/iode/po/voc/cruise-summary-reports/2020-05-01.md) ([rdf](http://purl.org/org/iode/po/voc/cruise-summary-reports/2020-05-01))
  
**Latest version**
  - [http://purl.org/org/iode/po/voc/cruise-summary-reports.md](http://purl.org/org/iode/po/voc/cruise-summary-reports.md) ([rdf](http://purl.org/org/iode/po/voc/cruise-summary-reports))
  
**Editors:**
  - [Adam Leadbetter](https://github.com/adamml), Marine Institue, Ireland
  - [Rob Thomas](https://github.com/robthomas-marine), Marine Institute, Ireland
  
**Contributors:**
  - Bob Arko, Lamont-Doherty Earth Observatory, Columbia University, USA
  - [Cynthia Chandler](https://github.com/cynDC42), Biological and Chemical Oceanography Data Management Office, Woods Hole Oceanographic Institution, USA

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
| dbo | http://dbpedia.org/ontology/ |  |
| dct | http://www.purl.org/dc/terms/ | All metadata terms maintained by the Dublin Core Metadata Initiative |
| foaf | http://xmlns.com/foaf/spec/# | A language linking people and information using the Web |
| gl | http://schema.geolink.org/1.0/base/main# | The GeoLink Ontology Design Patterns for marine sciences data markup |
| gsp | http://www.opengis.net/ont/geosparql# | A Geographic Query Language for Resource Description Framework Data |
| marineTLO | http://www.ics.forth.gr/isl/ontology/MarineTLO/ | The Marine Top Level Ontology, used here as a basis of uppler-level ontology alignment |
| org | http://www.w3.org/ns/org# | A core ontology for organizational structures, aimed at supporting linked data publishing of organizational information |
| prov | http://www.w3.org/ns/prov# | The PROV Ontology expresses the PROV Data Model using the Web Ontology Language |
| rdf | http://www.w3.org/1999/02/22-rdf-syntax-ns# | The Resource Description Framework Concepts Vocabulary |
| rdfs | http://www.w3.org/2000/01/rdf-schema# | A data-modelling vocabulary for Resource Description Framework data |
| sdo | http://schema.org/ | Schema.org vocabulary for publishing structured data on the Web |
| vann | http://purl.org/vocab/vann/ | A vocabulary for annotating descriptions of vocabularies with examples and usage notes |
| xsd | http://www.w3.org/2001/XMLSchema# | Used in XML Schemas for the elements, attributes, and types of the W3C XML Schema Recommendation itself. |

## Classes
[AssociatedEvent](#associatedevent) | [Cruise](#cruise) | [Measurement](#measurement) | [Mooring](#mooring) | [Operation](#operation) | | [CruiseSummaryReport](#cruisesummaryreport) | [Port Call](#portcall)

![Class level overview of the Cruise Summary Report vocabulary][top-level]

### AssociatedEvent

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#AssociatedEvent`

**Is subclass of**
[prov:Activity](http://www.w3.org/ns/prov#Activity)

**Described with properties**
[atLocation](#atlocation) | [hasTimeStamp](#hasTimeStamp)

**In range of**
[associatedEvent](#associatedevent)

### Cruise

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#Cruise`

A cruise is a port-to-port activity undertaken by a research vessel, or other ship equipped with instrumentation for oceanographic or marine scientific observations. A cruise is not limited to scintific operations but may also be an activity to relocate the vessel to another port for operational reasons.

**Example**
```ttl
	_:01 a csr:Cruise;
        rdfs:label "IGFS2016";
        csr:undertakenBy <http://vocab.nerc.ac.uk/collection/C17/45CE/>;
        csr:hasStartPortCall [ 
			a csr:PortCall; 
            csr:atPort <http://vocab.nerc.ac.uk/collection/C38/current/BSH75/>;
            csr:hasTimeStamp "2016-11-14"^^xsd:date
        ];
        <#hasEndPortCall> [ 
			a csr:PortCall;
            csr:atPort <http://vocab.nerc.ac.uk/collection/C38/current/BSH75/>;
            csr:hasTimeStamp "2016-12-18"^^xsd:date
        ];
        <#hasChiefScientist> []
```

**Is subclass of**
[gl:Cruise](http://schema.geolink.org/1.0/base/main#Cruise), [marineTLO:BC61_Capture_Activity](http://www.ics.forth.gr/isl/ontology/MarineTLO/BC61_Capture_Activity), [prov:Activity](http://www.w3.org/ns/prov#Activity), [sdo:Event](http://schema.org/Event)

**Described with properties**

[hasChiefScientist](#haschiefscientist) | [hasCoChiefScientist](#hascochiefscientist) | [hasDOI](#hasdOI) | [hasEndPortCall](#hasendportcall) | [hasIdentifier](#hasidentifier) | [hasStartPortCall](#hasstartportcall) | [hasTrack](#hastrack)  | [label](#label)| [undertakenBy](#undertakenby)

**In range of**

[describesCruise](#describescruise), [undertakes](#undertakes)

### CruiseSummaryReport

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#CruiseSummaryReport`

Cruise Summary Reports are the usual means for reporting on cruises or field experiments at sea. Traditionally, it is the Chief Scientist's obligation to submit a Cruise Summary Report to their National Oceanographic Data Centre not later than two weeks after the cruise.

**Example**

```ttl
_:02 a csr:CruiseSummaryReport;
	csr:collate-centre <http://edmo.seadatanet.org/396>;
   	dct:created "2017-01-10"^^xsd:date;
 	dct:language <http://id.loc.gov/vocabulary/iso639-1/en>;
   	dct:subject <http://vocab.nerc.ac.uk/collection/P22/current/28/>;
   	dct:subject <http://registry.it.csiro.au/def/isotc211/MD_TopicCategoryCode/oceans>;
   	csr:boundingBox "POLYGON((-12.4827 54.475, -3.7473 54.475, -3.7473 50.446, -12.4827 50.446, -12.4827 54.475))"^^gsp:wktLiteral;
   	csr:describesCruise [];
   	csr:describesDataset [];
   	csr:description "The Irish Groundfish Survey (IGFS) is carried out in the 4th quarter annually as part of an internationally coordinated demersal trawl survey effort under the ICES working group for International Bottom Trawl Surveys (IBTS). The primary objective is to use trawl sampling to provide an annual relative index of abundance and recruitment for commercially exploited fish stocks."@en;
   	csr:responsibleLaboratory <http://edmo.seadatanet.org/396>;
   	csr:generalOceanArea <http://vocab.nerc.ac.uk/collection/C19/current/1_6/>;
   	csr:generalOceanArea <http://vocab.nerc.ac.uk/collection/C19/current/SVX00017/>;
   	csr:marsdenSquare <http://vocab.nerc.ac.uk/collection/C37/current/146/>;
   	csr:marsdenSquare <http://vocab.nerc.ac.uk/collection/C37/current/181/>;
   	csr:marsdenSquare <http://vocab.nerc.ac.uk/collection/C37/current/182/>.
```

**Is subclass of**

[foaf:Document](http://xmlns.com/foaf/spec/#Document), [gl:Document](http://schema.geolink.org/1.0/base/main#Document), [prov:Entity](http://www.w3.org/ns/prov#Entity)

**Described with properties**

[additionalDocumentation](#additionaldocumentation) | [boundingBox](#boundingbox) | [collateCentre](#collateCentre) | [describesCruise](#describescruise) | [describesDataset](#describesDataset) | [describesOperation](#describesOperation) | [description] | [generalOceanArea] | [hasProgram] | [marsdenSquare] | [responsibleLaboratory] | [specificGeographicArea] | [trackChart]

**GeoLink Document Type**

`Cruise Summary Report`

### Measurement

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#Measurement`

**Is subclass of**

[Operation](#operation), [prov:Activity](http://www.w3.org/ns/prov#Activity)

**Described with properties**
[associatedEvent](#associatedevent) | [description](#description) | [numberOfMeasurements](#numberofmeasurements)

**In range of**
[describesoperation](#describesOperation)

### Mooring

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#Measurement`

**Is subclass of**
[Operation](#operation), [prov:Activity](http://www.w3.org/ns/prov#Activity)

**Described with properties**
[associatedEvent](#associatedevent) | [description](#description)

**In range of**
[describesoperation](#describesOperation)

### Operation

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#Operation`

An activity (such as a measurement or mooring) occuring on a research vessel cruise, flight, deployment, etc...

**Is subclass of**
[prov:Activity](http://www.w3.org/ns/prov#Activity)

**Described with properties**
[associatedEvent](#associatedevent) | [description](#description)

**In range of**
[describesoperation](#describesOperation)

### PortCall

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#PortCall`

A designated, specific port visited by a Vessel for some significant reason - the start or end of a mission; transfer of passengers, goods, or equipment

**Is subclass of**
[prov:InstantaneousEvent](http://www.w3.org/ns/prov#InstantaneousEvent)

**Described with properties**
[atPort](#atport) | [hasTimeStamp](#hastimestamp)

**In range of**
[hasEndPortCall](#hasendportcall) | [hasStartPortCall](#hasstartportcall)

## Attributes

[additionalDocumentation](#additionaldocumentation) | [associatedEvent](#associatedevent) | [atLocation](#atlocation) | [atPort](#atport) | [boundingBox](#boundingbox) | [collateCentre](#collatecentre) | [describesCruise](#describescruise) | [describesDataset](#describesdataset) | [describesOperation](#describesoperation) | [description](#description) | [generalOceanArea](#generaloceanarea) | [hasChiefScientist](#haschiefscientist) | [hasCoChiefScientist](#hascochiefscientist) | [hasDOI](#hasdoi) | [hasEndPortCall](#hasendportcall) | [hasIdentifier](#hasidentifier) | [hasProgram](#hasprogram) | [hasStartPortCall](#hasstartportcall) | [hasTimeStamp](#hastimestamp) | [hasTrack](#hastrack) | [instrumentID](#instrumentid) | | [instrumentPlatformCode](#instrumentplatformcode) | [instrumentPlatformDescription](#instrumentplatformdescription) | [label](#label) | [marsdenSquare](#marsdensquare) | [numberOfMeasurements](#numberofmeasurements) | [responsibleLaboratory](#responsiblelaboratory) | [specificGeographicArea](#specificgeographicarea) | [trackChart](#trackchart) | | [undertakenBy](#undertakenby) | [undertakes](#undertakes)

### additionalDocumentation

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#additionalDocumentation`

Provides a link from the Cruise Summary Report object to any supporting documentation, such as cruise report or scientific papers written from the research undertaken on the Cruise

**Is sub-property of**
[rdfs:seeAlso](http://www.w3.org/2000/01/rdf-schema#seeAlso)

**Has domain**
[CruiseSummaryReport](#cruisesummaryreport)

**Has range**
[xsd:anyURI](http://www.w3.org/2001/XMLSchema#anyURI)

## associatedEvent

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#associatedEvent`

Connects an Operation to an AssociatedEvent describing a time and location associated with the Operation

**Has domain**
[Operation](#operation)

**Has range**
[AssociatedEvent](#associatedevent)

### atLocation

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#atLocation`

Describes the port at which a PortCall takes place. It is advised to use a term from a controlled vocabulary describing a gazetteer entry for the port as the object for the triple, such as the [SeaDataNet Ports Gazetteer](http://vocab.nerc.ac.uk/collection/C38/current/)

**Is sub-property of**
[prov:atLocation](http://www.w3.org/ns/prov#atLocation)

**Has domain**
[AssociatedEvent](#associatedevent)

**Has range**
[gsp:wktLiteral](http://www.opengis.net/ont/geosparql#wktLiteral)

### atPort

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#atPort`

Describes the port at which a PortCall takes place. It is advised to use a term from a controlled vocabulary describing a gazetteer entry for the port as the object for the triple, such as the [SeaDataNet Ports Gazetteer](http://vocab.nerc.ac.uk/collection/C38/current/)

**Is sub-property of**
[gl:atPort](http://schema.geolink.org/1.0/base/main#atPort),[prov:atLocation](http://www.w3.org/ns/prov#atLocation)

**Has domain**
[PortCall](#portcall)

**Has range**
[xsd:anyURI](http://www.w3.org/2001/XMLSchema#anyURI)

### boundingBox

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#boundingBox`

Describes a bounding box in which the track of the Cruise described by the Cruise Summary Report fits. The object of the triple is a Well Known Text string

**Is sub-property of**
[dct:spatial](http://www.purl.org/dc/terms/spatial)

**Has domain**
[CruiseSummaryReport](#cruisesummaryreport)

**Has range**
[gsp:wktLiteral](http://www.opengis.net/ont/geosparql#wktLiteral)

### collateCentre

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#collateCentre`

Connects a CruiseSummaryReport with the National Oceanographic Data centre which collates and submits these reports for the SeaDataNet infrastructre. The IRI of the org:Organization at the subject of the triple should come from the Linked Data representation of the [European Directory of Marine Organisations](https://edmo.seadatanet.org/sparql/)

**Has domain**
[CruiseSummaryReport](#cruisesummaryreport)

**Has range**
[org:Organization](http://www.w3.org/ns/org#Organization)

### describesCruise

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#describesCruise`

Connects a Cruise Summary Report with the Cruise object which the Summary Report decribes

**Is sub-property of**
[foaf:primaryTopic](http://xmlns.com/foaf/spec/#primaryTopic)

**Has domain**
[CruiseSummaryReport](#cruisesummaryreport)

**Has range**
[Cruise](#cruise)

### describesDataset

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

Provides a link from a Cruise Summary Report to a dataset which was created from or by the activity of the Cruise which the Cruise Summary Report describes

**Example**

```ttl
_:02 csr:describesDataset [ 
   	a gl:Dataset;
	gl:hasInstrument [
    a gl:Instrument;
       	gl:hasInstrumentType <http://vocab.nerc.ac.uk/collection/L05/current/308/>
    ], [
      	a gl:Instrument;
      	gl:hasInstrumentType <http://vocab.nerc.ac.uk/collection/L05/current/102/>
    ], [
    	a gl:Instrument;
       	gl:hasInstrumentType <http://vocab.nerc.ac.uk/collection/L05/current/133/>
    ];
    gl:hasMeasurementType <http://vocab.nerc.ac.uk/collection/P02/current/CAPH/>, 
							<http://vocab.nerc.ac.uk/collection/P02/current/CDTA/>,
							<http://vocab.nerc.ac.uk/collection/P02/current/CHUM/>
].
```

**Has domain**
[CruiseSummaryReport](#cruisesummaryreport)

**Has range**
[gl:Dataset](http://schema.geolink.org/1.0/base/main#Dataset)

### describesOperation

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#describesOperation`

Provides a link from a Cruise Summary Report to an Operation which occurred on the Cruise which the Cruise Summary Report describes

**Example**

```ttl
_:02 csr:describesOperation [
   	csr:Mooring;
    csr:description "This is an example mooring record"@en;
    csr:hasAssociatedEvent [
       	a csr:AssociatedEvent;
       	csr:hasTimeStamp "2017-03-16"^^xsd:date;
       	csr:atLocation "POINT(9.0568,53.2707)"^^gsp:wktLiteral
    ];
    csr:hasInstrument [
       	a gl:Instrument;
       	csr:instrumentId "instrument-1-D01-487"@en;
       	gl:hasInstrumentType <http://vocab.nerc.ac.uk/collection/C77/current/D71/>;
       	csr:instrumentPlatformCode "D01/487";
       	csr:instrumentPlatformDescription "Current meters, conducted by LABORATORY of PHYSICAL OCEANOGRAPHY (LPO) UMR 6523 CNRS-IFREMER-IRD-UBO"
    ]
]
```

```ttl
_:02 csr:describesOperation [
	a csr:Measurement;
    csr:hasDescription "This is an example measurement record"@en;
    csr:hasAssociatedEvent [
       	a csr:AssociatedEvent;
       	csr:hasTimeStamp "2017-03-17"^^xsd:date;
       	csr:atLocation "POINT(9.0568,53.2707)"^^gsp:wktLiteral
    ]
]
```	

**Is sub-property of**
[prov:wasGeneratedBy](http://www.w3.org/ns/prov#wasGeneratedBy)

**Has domain**
[CruiseSummaryReport](#cruisesummaryreport)

**Has range**
[Operation](#operation)

### description

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#description`

Provides a detailed abstarct of a Cruise (describing in plain-text the who, what, when, where, why, how of the activity), or an overview of an Operation

**Is sub-property of**
[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)

**Has domain**
[CruiseSummaryReport](#cruisesummaryreport), [Operation](#operation)

**Has range**
[rdfs:literal](http://www.w3.org/2000/01/rdf-schema#literal)

### generalOceanArea

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#generalOceanArea`

Provides a link to a gazetteer entry from a controlled vocabulary to describe any number of sea areas visited during a Cruise. Such controlled vocabularies include the [SeaVoX salt and fresh water body gazetteer](http://vocab.nerc.ac.uk/collection/C19/current/)

**Has domain**
[CruiseSummaryReport](#cruisesummaryreport)

**Has range**
[xsd:anyURI](http://www.w3.org/2001/XMLSchema#anyURI)

### hasChiefScientist

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#hasChiefScientist`

The prov:Agent at the range of this predicate should represent the chief scientist undertaking the research cruise

**Example**

```ttl
_:01 csr:hasChiefScientist [
   	a foaf:Person, gl:Person, prov:Agent;
   	org:memberOf <http://edmo.seadatanet.org/396>;
   	prov:actedOnBehalfOf <http://edmo.seadatanet.org/396>;
   	foaf:name "John Doe";
   	foaf:mbox <mailto:john.doe@example.org>
]
```

**Is sub-property of**
[gl:hasChiefScientist](http://schema.geolink.org/1.0/base/main#hasChiefScientist), [prov:wasAssociatedWith](http://www.w3.org/ns/prov#wasAssociatedWith)

**Has domain**
[Cruise](#cruise)

**Has range**
[prov:Agent](http://www.w3.org/ns/prov#Agent)

### hasCoChiefScientist

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#hasCoChiefScientist`

The prov:Agent at the range of this predicate should represent one of a number of co-chief scientists undertaking the research cruise

**Example**

```ttl
_:01 csr:hasCoChiefScientist [
	   	a foaf:Person, gl:Person, prov:Agent;
   		org:memberOf <http://edmo.seadatanet.org/123456>;
   		prov:actedOnBehalfOf <http://edmo.seadatanet.org/123456>;
   		foaf:name "John Doe";
   		foaf:mbox <mailto:john.doe@example.org>
    ], [
		a foaf:Person, gl:Person, prov:Agent;
    	org:memberOf <http://edmo.seadatanet.org/123456>;
    	prov:actedOnBehalfOf <http://edmo.seadatanet.org/123456>;
    	foaf:name "Jane Doe";
    	foaf:mbox <mailto:jane.doe@example.org>
	]
```

**Is sub-property of**
[gl:hasCoChiefScientist](http://schema.geolink.org/1.0/base/main#hasCoChiefScientist), [prov:wasAssociatedWith](http://www.w3.org/ns/prov#wasAssociatedWith)

**Has domain**
[Cruise](#cruise)

**Has range**
[prov:Agent](http://www.w3.org/ns/prov#Agent)

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
[gl:hasEndPortCall](http://schema.geolink.org/1.0/base/main#hasEndPortCall), [prov:qualifiedEnd](http://www.w3.org/ns/prov#qualifiedEnd)

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

### hasProgram

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#`

**Has domain**

**Has range**

### hasStartPortCall

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#hasStartPortCall`

Links a Cruise object to the PortCall object which describes the event which started the Cruise

**Is sub-property of**
[gl:hasStartPortCall](http://schema.geolink.org/1.0/base/main#hasStartPortCall), [prov:qualifiedEnd](http://www.w3.org/ns/prov#qualifiedEnd)

**Has domain**
[Cruise](#cruise)

**Has range**
[PortCall](#portcall)

### hasTimeStamp

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#hasTimeStamp`

Describes the time at which an Operation or a PortCall occurred

**Is sub-property of**
[prov:atTime](http://www.w3.org/ns/prov#atTime)

**Has domain**
[Operation](#operation), [PortCall](#portcall)

**Has range**
[xsd:date](http://www.w3.org/2001/XMLSchema#date), [xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime)

### hasTrack

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#hasTrack`

Provides a representation of the track taken by the research vessel during the Cruise as a Well Known Text literal.

**Is sub-property of**
[gl:hasTrack](http://schema.geolink.org/1.0/base/main#hasTrack)

**Has domain**
[Cruise](#cruise)

**Has range**
[gsp:wktLiteral](http://www.opengis.net/ont/geosparql#wktLiteral)

### instrumentID

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#instrumentID`

A lexical label, or, title for the Instrument

**Is sub-property of**
[label](#label), [rdfs:label](http://www.w3.org/2000/01/rdf-schema#label)

**Has domain**
[gl:Instrument](http://schema.geolink.org/1.0/base/main#Instrument)

**Has range**
[rdfs:Literal](http://www.w3.org/2000/01/rdf-schema#label)

### instrumentPlatformCode

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#instrumentPlatformCode`

A lexical label, or, title for the Instrument Platform Code

**Is sub-property of**
[label](#label), [rdfs:label](http://www.w3.org/2000/01/rdf-schema#label)

**Has domain**
[gl:Instrument](http://schema.geolink.org/1.0/base/main#Instrument)

**Has range**
[rdfs:Literal](http://www.w3.org/2000/01/rdf-schema#label)

### label

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#label`

A lexical label, or, title for the object

**Is sub-property of**
[rdfs:label](http://www.w3.org/2000/01/rdf-schema#label)

**Has domain**
[Cruise](#cruise)

**Has range**
[rdfs:Literal](http://www.w3.org/2000/01/rdf-schema#label)

### marsdenSquare

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#marsdenSquare`

Marsden squares is a system that divides a chart of the world with latitude-longitude gridlines between 80N and 70S latitudes (or 90N and 80S) into grid cells of 10-degree latitude by 10-degree longitude, each with a unique, numeric identifier. The object of the triple should be one Marsden Square visted during the Cruise, and enough triples instantiated to describe all Marsden Squares visited during the Cruise. A controlled vocabulary of Marsden Squares is maintained be the [British Oceanographic Data Centre](http://vocab.nerc.ac.uk/collection/C37/current/)

**Has domain**
[CruiseSummaryReport](#cruisesummaryreport)

**Has range**
[xsd:anyURI](http://www.w3.org/2001/XMLSchema#anyURI)

### numberOfMeasurements

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#numberOfMeasurements`

Describes the number of measurements made during a Measurement Operation

**Has domain**
[Measurement](#measurement)

**Has range**
[xsd:integer](http://www.w3.org/2001/XMLSchema#integer)

### responsibleLaboratory

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#responsibleLaboratory`

Describes the laboratory, or one of the laboratories, responsible for the Cruise which is described by the Cruise Summary Report

**Is sub-property of**
[gl:hasAuthor](http://schema.geolink.org/1.0/base/main#hasAuthor)

**Has domain**
[CruiseSummaryReport](#cruisesummaryreport)

**Has range**
[foaf:Organization](http://xmlns.com/foaf/spec/#Organization), [gl:Organization](http://schema.geolink.org/1.0/base/main#Organization), [org:Organization](http://www.w3.org/ns/org#Organization), [prov:Organization](http://www.w3.org/ns/prov#Organization)

### specificGeographicArea

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#specificGeographicArea`

A lexical comment which gives a more specific description of the area visited by the Cruise which is the Cruise Summary Report describes

**Is sub-property of**
[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)

**Has domain**
[CruiseSummaryReport](#cruisesummaryreport)

**Has range**
[rdfs:literal](http://www.w3.org/2000/01/rdf-schema#literal)

### trackChart

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#trackChart`

Points to a graphical representation (e.g. a TIFF, PNG or JPG file) showing the track taken by the vessel during the Cruise described by the Cruise Summary Report 

**Has domain**
[CruiseSummaryReport](#cruisesummaryreport)

**Has range**
[xsd:anyURI](http://www.w3.org/2001/XMLSchema#anyURI)

### undertakenBy

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#undertakenBy`

The prov:Agent at the range of this predicate should represent the vessel undertaking the research cruise. Ideally, a controlled vocabulary resource should be used to instantiate the prov:Agent, such as the International Council for the Exploration of the Seas [ship and platform code list](https://vocab.ices.dk/services/rdf/collection/SHIPC)

**Is sub-property of**
[prov:used](http://www.w3.org/ns/prov#used)

**Is super-property of**
[gl:hasVessel](http://schema.geolink.org/1.0/base/main#hasVessel)

**Has domain**
[Cruise](#cruise)

**Has range**
[prov:Agent](http://www.w3.org/ns/prov#Agent)

**Has inverse**
[undertakes](#undertakes)

### undertakes

**IRI** `http://purl.org/org/iode/po/voc/cruise-summary-reports#undertakes`

The prov:Agent at the domain of this predicate should represent the vessel which undertook the Cruise at its range. Ideally, a controlled vocabulary resource should be used to instantiate the prov:Agent, such as the International Council for the Exploration of the Seas platform code list.

**Is sub-property of**
[prov:wasGeneratedBy](http://www.w3.org/ns/prov#wasGeneratedBy)

**Has domain**
[prov:Agent](http://www.w3.org/ns/prov#Agent)

**Has range**
[Cruise](#cruise)

**Has inverse**
[isUndertakenBy](#undertakenBy)

## Acknowledgments
| | |
|-|-:|
| This work was developed under the SeaDataCloud project (2016-2020), grant agreement 730960, EU H2020 programme. The publication of this work via GitHub was made possible with the support of the International Oceanographic Data and Information Exchange of UNESCO's Intergovernmental Oceanographic Commission. | ![SeaDataCloud logo][sdc-logo] |

The advice of Simon Cox of the Commonwealth Scientific and Industrial Research Organisation, Australia was greatly appreciated at various stages in the ontology design phase.

The assistance of Arno Lambert and Peter Pissiersens at the Project Office of the International Oceanographic Data and Information Exchange of UNESCO's Intergovernmental Oceanographic Commission was invaluable in the web publishing of the vocabulary resource.

## References

### Normative references

### Informative References

[ioc-logo]: ./img/ioc_logo.png
[sdc-logo]: ./img/sdc_logo.png
[top-level]: ./img/linked_cruise_summary_reports_top_level.png