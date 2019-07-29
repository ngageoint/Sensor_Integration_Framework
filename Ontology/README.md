# Sensor Integration Framework Ontology

## Introduction

The OGC Sensor Web Enablement (SWE) set of standards define the Web Services and data formats necessary to provide sensor information to the DCGS enterprise which is independent of the reporting sensor and phenomenology. This capability is key to multi-INT analysis. However, SWE does not address how that data gets into the SWE software.  The Sensor Integration Framework provides the tools and processes to address that issue.

## The Ontology

The SIF Ontology is a pragmatic effort. Many rules have been violated in the quest to build a useful tool. First of which, this ontology is encoded in UML. While purists will be horrified, the SMEs contributing to this work understand UML and have the tools necessary to work with it. They are not (by and large) conversant with OWL/RDF. So heresy has been committed in the name of progress.

The SIF Ontology five major parts:

. Base Data Types: These classes capture the relevant concepts from SWE Common. In addition, the Base Simple Types define a set of basic concepts for use elsewhere in the ontology. These classes align basic concepts such as Amps or Hertz with the corresponding SWE Common construct for representing that concept. The classes exist primarily for re-use by other classes in the Ontology.

. Measure Types: These are concepts which one would expect to be reported by a sensor system.  

. Observations: Observations organize information reported about the target (Feature of Interest) of the sensor. Observations are reported out as OGC Observation and Measurement (OM) Observations.

. Performers: These are abstract concepts for modeling the sensor system. They serve to organize descriptive and status data about the sensor system. They also provide the conceptual framework for generating OGC SensorML documents.

. Properties: SensorML and OM Observations are populated with properties. A property agregates one or more measures to represent a more complex concept.

## Using the Ontology

A key property of SWE is that it defines syntax, not semantics. Most SWE data elements contain a "definition" element. This element is a scoped name which identifies the semantics of an instance of that element. For example, it could serve as a reference to an ontology where the definition for that element can be found. So integrating an existing sensor system into SWE can be done in two steps:
1) Map the sensor system syntax
2) Map the sensor system semantics

### Map the Syntax

The first step in mapping the syntax is to understand and model the sensor system.

1) Identify the components of the sensor system which are the subject of reported information.
2) Allocate those components to Performer classes from the Ontology
3) Associate the Performer classes to reflect the structure of the Sensor System.

We have now mapped the Sensor System components into the corresponding SWE SensorML constructs. 

Next, map each reported value into the corresponding SWE Common construct. The SWE Common aligns with traditional Computer Science types, so this should not be too hard.

### Map the Semantics


