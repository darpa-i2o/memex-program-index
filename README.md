# Memex tools and components

A list of memex-related tools and their repository URLs

## Crawlers

#### Scrapy Cluster
[https://github.com/istresearch/scrapy-cluster](https://github.com/istresearch/scrapy-cluster) (stable)
This project uses Redis and Kafka to create a distributed on demand scraping cluster. 
Additional documentation: [http://scrapy-cluster.readthedocs.io/](http://scrapy-cluster.readthedocs.io/) 

## Domain discovery systems

## Extractors/NLP/Image processing


#### Extraction Toolkit (etk)
[https://github.com/usc-isi-i2/etk](https://github.com/usc-isi-i2/etk]) (alpha).
A general purpose toolkit for easily extracting semi-structured data, tables and entities from arbitrary web pages. Contains a rich set of entity extractors.

#### Landmark Extractor (landmark)
[https://github.com/inferlink](https://github.com/inferlink) (beta).
An automated tool to create rules that extract data from web sites containing templetized pages.
Landmark rules are directly usable in **etk**.

#### ImageSift - Color Fingerprint Image Similarity
[https://github.com/unchartedsoftware/TellFinder-ImageSift](https://github.com/unchartedsoftware/TellFinder-ImageSift) (stable).
A reference implementation of the image similarity algorithm used by TellFinder. Includes a sample application and training data.

## End-to-end search systems

### DIG: Domain-Specific Insight Graphs
DIG provides generic components to build end-to-end domain-specific search applications. 
The DIG components are available as standalone tools.
In addition to the tools listed below, the component suite includes **etk** and **landmark**, listed above.


#### Karma Information Integration Tool 
[https://github.com/usc-isi-i2/Web-Karma](https://github.com/usc-isi-i2/Web-Karma]) (stable, full-featured). 
An information integration tool that enables users to quickly and easily integrate data from a variety of data sources including databases, spreadsheets, delimited text files, XML, JSON, KML and Web APIs. 


#### Record Linkage Toolkit (rltk)
[https://github.com/usc-isi-i2/rltk](https://github.com/usc-isi-i2/rltk) (stable, incomplete).
A general-purpose, highly-scalable, easy-to-use record linkage toolit contraining a wide variety of similarity metrics, blocking schemes and machine learning algorithms for matching records.

#### Knowledge Graph Search
[https://github.com/usc-isi-i2/dig-sandpaper](https://github.com/usc-isi-i2/dig-sandpaper) (beta).
A search engine that translates structured queries for a knowledge graph to sophisticated ElasticSearch queries that retrieve ranked results on noisy knowledge graphs.

#### Graphical Interface For Searching Knowledge Graphs
[https://github.com/NextCenturyCorporation/digapp-ht](https://github.com/NextCenturyCorporation/digapp-ht) (stable).
A rich set of visual components for creating rich user interfaces for querying and visualizing knowledge graphs.

### TellFinder

#### Personas
[https://github.com/uncharted/TellFinder-Personas](https://github.com/uncharted/TellFinder-Personas) (development - eta March 2017).
UI component for the TellFinder 'Personas' visualization.

#### Facets
[https://github.com/uncharted/TellFinder-Facets](https://github.com/uncharted/TellFinder-Facets) (development - eta March 2017).
UI component for the TellFinder 'Facets' visualization.

#### TellFinder Data API
[https://github.com/uncharted/TellFinder-DataAPI](https://github.com/uncharted/TellFinder-DataAPI) (development - eta March 2017).
RESTful server for accessing all of TellFinder data models, analytics and search strategies. Includes authentication and case management modules.

#### TellFinder Pipeline
[https://github.com/uncharted/TellFinder-Pipeline](https://github.com/uncharted/TellFinder-Pipeline) (development - eta May 2017).
General purpose distributed processes pipeline for ingesting web data into the TellFinder data model. Includes general purpose data cleaning, extraction, normalization and analytics. Based on the [https://github.com/unchartedsoftware/sparkpipe-core](Uncharted Spark Pipeline).

#### TellFinder Example Component Application
[https://github.com/uncharted/TellFinder-ComponentExample](https://github.com/uncharted/TellFinder-ComponentExample) (development - eta June 2017).
Example application showing TellFinder UI components and Data API on a new domain. Includes sample data. 

### TorFlow
[https://github.com/unchartedsoftware/torflow](https://github.com/unchartedsoftware/torflow) (stable demo).
A visualization of data flow in the Tor Network.

