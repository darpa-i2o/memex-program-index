# Memex tools and components

A list of memex-related tools and their repository URLs

## Crawlers

#### ACHE Crawler

[https://github.com/ViDA-NYU/ache/](https://github.com/ViDA-NYU/ache/)

ACHE is a focused web crawler. It collects web pages that satisfy some specific criteria, e.g., pages that belong to a given domain or that contain a user-specified pattern. ACHE differs from generic crawlers in that it: employs learning classifiers to distinguish between relevant and irrelevant pages in a given domain, and automatically learns how to prioritize links in order to efficiently locate relevant content while avoiding the retrieval of irrelevant content.

#### Scrapy Cluster
[https://github.com/istresearch/scrapy-cluster](https://github.com/istresearch/scrapy-cluster) (stable).
This project uses Redis and Kafka to create a distributed on demand scraping cluster.
Additional documentation: [http://scrapy-cluster.readthedocs.io/](http://scrapy-cluster.readthedocs.io/)



#### Undercrawler
[https://github.com/TeamHG-Memex/undercrawler](https://github.com/TeamHG-Memex/undercrawler) (stable) This is a generic Scrapy crawler designed to handle a number of challenges that are hard for traditional generic crawlers, such as dynamic content, login and search forms, pagination. It crawls from the given seed url in breadth first order, exporting all crawled pages and documents into the Memex CDRv2 format.

#### Deep-Deep
[https://github.com/TeamHG-Memex/deep-deep](https://github.com/TeamHG-Memex/deep-deep) (dev) Deep-Deep is a Scrapy-based crawler which uses Reinforcement Learning methods to learn which links to follow. It is called Deep-Deep, but it doesn't use Deep Learning, and it is not only for Deep web. Weird.

#### Scrapy-Dockerhub
[https://github.com/TeamHG-Memex/scrapy-dockerhub](https://github.com/TeamHG-Memex/scrapy-dockerhub) (alpha) Scrapy-Dockerhub is a deployment setup for Scrapy spiders that packages the spider and all dependencies into a Docker container, which is then managed by a Fabric command line utility. With this setup, users can run spiders seamlessly on any server, without the need for Scrapyd, which typically handles the spider management. With Scrapy-Dockerhub, users issue one command to deploy spider with all dependencies to the server and second command to run it. There are also commands for viewing jobs, logs, etc. 

#### Splash
[https://github.com/scrapinghub/splash](https://github.com/scrapinghub/splash) (stable) Splash is a lightweight, scriptable browser-as-a-service with an HTTP API. 

#### Frontera
[https://github.com/scrapinghub/frontera](https://github.com/scrapinghub/frontera) (dev) Frontera is a web crawling framework consisting of crawl frontier, and distribution/scaling primitives, allowing to build a large scale online web crawler. Frontera takes care of the logic and policies to follow during the crawl. It stores and prioritises links extracted by the crawler to decide which pages to visit next, and capable of doing it in distributed manner.

#### DomainSpider
[https://github.com/TeamHG-Memex/domainSpider](https://github.com/TeamHG-Memex/domainSpider) (WIP) A simple Python web crawler that stays within a set list of domains.

#### Crawl Data Repository (CDR) Schema
[https://github.com/istresearch/memex-cdr](https://github.com/istresearch/memex-cdr) (stable).
This repository hosts code and schema information related to the Memex Crawl Data Repository (CDR).

#### SRI Forum Spider 
[https://github.com/pporras7/TeamSRI-LIGHTS] (https://github.com/pporras7/TeamSRI-LIGHTS) (stable).
An interactive web forum analysis tool that operates over Tor hidden services. This tool is capable of passive forum data capture and posting dialog at random or user-specifiable intervals. (Python) 

### Crawler Utilities


#### Aquarium
[https://github.com/TeamHG-Memex/aquarium](https://github.com/TeamHG-Memex/aquarium) (stable) Aquarium is a cookiecuter template for hassle-free Docker Compose + Splash setup. Think of it as a Splash instance with extra features and without common pitfalls.

#### Arachnado
[https://github.com/TeamHG-Memex/arachnado](https://github.com/TeamHG-Memex/arachnado) (stable) Arachnado is a management interface for launching deep crawls of specific websites. It provides a Tornado-based HTTP API and a web UI for managing Scrapy-based crawlers. 

#### AutoLogin
[https://github.com/TeamHG-Memex/autologin](https://github.com/TeamHG-Memex/autologin) (stable) AutoLogin is a utility that allows a web crawler to start from any given page of a website (for example the home page) and attempt to find the login page, where the spider can then log in with a set of valid, user-provided credentials to conduct a deep crawl of a site to which the user already has legitimate access. AutoLogin can be used as a library or as a service. 

#### AutoLogin-middleware
[https://github.com/TeamHG-Memex/autologin-middleware](https://github.com/TeamHG-Memex/autologin-middleware) (stable) Scrapy middleware for the AutoLogin utility.

#### AutoPager
[https://github.com/TeamHG-Memex/autopager](https://github.com/TeamHG-Memex/autopager) (stable) Autopager is a Python package which detects and classifies pagination links.

#### AutoRegister
[https://github.com/TeamHG-Memex/autoregister](https://github.com/TeamHG-Memex/autoregister) (POC, WIP) AutoRegister is a python package that attempts to find a registration form on site and submit information to create an account. 

#### Crazy-Form-Submitter
[https://github.com/TeamHG-Memex/crazy-form-submitter](https://github.com/TeamHG-Memex/crazy-form-submitter) (POC, WIP) A library to find a search form on a page and submit strings to the form.

#### Formasaurus
[https://github.com/TeamHG-Memex/Formasaurus](https://github.com/TeamHG-Memex/Formasaurus) (stable) Formasaurus is a Python package that tells users the type of an HTML form: is it a login, search, registration, password recovery, join mailing list, contact form or something else. Under the hood it uses machine learning. 

#### Fortia
[https://github.com/TeamHG-Memex/fortia](https://github.com/TeamHG-Memex/fortia) (WIP) Firefox extension for automatic data extraction. It uses scrapely under the hood.

#### LinkRot
[https://github.com/TeamHG-Memex/linkrot](https://github.com/TeamHG-Memex/linkrot) (dev) A script (Scrapy spider) to check a list of URLs periodically to determine whether a page is still alive or whether it has been 404’d. 

#### MaybeDont
[https://github.com/TeamHG-Memex/MaybeDont](https://github.com/TeamHG-Memex/MaybeDont) (stable) MaybeDont is a library that helps avoid downloading pages with duplicate content during crawling. It learns which URL components are important and which are not important during crawling, and tries to predict if the page will be duplicate based on its URL. The idea is that if you have a crawler that just follows all links, it might download a lot of duplicate pages: for example, for a forum there might be pages like /view.php?topicId=10 and /view.php?topicId=10&start=0 - the only difference is added start=0, and the content of this pages is likely duplicate. If we knew that adding start=0 does not change content, then we would avoid downloading the page /view.php?topicId=10&start=0 if we have already fetched /view.php?topicId=10, and thus save time and bandwidth.

#### Scrash-LUA-Examples
[https://github.com/TeamHG-Memex/scrash-lua-examples](https://github.com/TeamHG-Memex/scrash-lua-examples) (POC, WIP) A set of LUA directives with JavaScript helpers that are useful to scrape dynamic pages with extensive AJAX calls.

#### Scrapy Rotating Proxies
[https://github.com/TeamHG-Memex/scrapy-rotating-proxies](https://github.com/TeamHG-Memex/scrapy-rotating-proxies) (stable) This package provides a Scrapy middleware to use rotating proxies, check that they are alive and adjust crawling speed.

#### Scrapy-Crawl-Once
[https://github.com/TeamHG-Memex/scrapy-crawl-once](https://github.com/TeamHG-Memex/scrapy-crawl-once) (stable) This package provides a Scrapy middleware which allows to avoid re-crawling pages which were already downloaded in previous crawls.

#### SRI HSProbe
[https://github.com/pporras7/TeamSRI-LIGHTS] (https://github.com/pporras7/TeamSRI-LIGHTS) (stable).
HSProbe is a python multi-threaded STEM-based application designed to interrogate the status of Tor hidden services (HSs) and extracting hidden service content. It is an HS-protocol savvy crawler, that uses protocol error codes to decide what to do when a hidden service is not reached. HSProbe tests whether specified Tor hidden services (.onion addresses) are listening on one of a range of pre-specified ports, and optionally, whether they are speaking over other specified protocols. As of this version, support for HTTP and HTTPS is implemented. Hsprobe takes as input a list of hidden services to be probed and generates as output a similar list of the results of each hidden service probed. (Python)


### Web Page Classifiers

#### Page-class
[https://github.com/Sotera/page-class](https://github.com/Sotera/page-class) (In development) A tool to classify web pages into categories used by MEMEX such as blog|wiki|news|forum|classified|shopping. Testing several approaches and subsystems including `webpageclassifier`, below. Includes simple web app with JSON and HTML interfaces.

`webpageclassifier`: Categorizes urls as one of: blog|wiki|news|forum|classified|shopping|undecided. Manually-created if-then rules (decision tree) intended as a quick first-pass.
* [https://github.com/asitang/webpageclassifier](https://github.com/asitang/webpageclassifier) (Original JPL webpageclassifier).
* [https://github.com/Sotera/webpageclassifier](https://github.com/Sotera/webpageclassifier) (Sotera's branch)

#### Page-Compare
[https://github.com/TeamHG-Memex/page-compare](https://github.com/TeamHG-Memex/page-compare) (stable) This is a simple toolset for measuring the similarity of web pages.

#### Soft404
[https://github.com/TeamHG-Memex/soft404](https://github.com/TeamHG-Memex/soft404) (stable) A classifier for detecting soft 404 pages.


### Machine Learning Utilities

#### ELI5
[https://github.com/TeamHG-Memex/eli5](https://github.com/TeamHG-Memex/eli5) (dev) ELI5 is a Python package which helps to debug machine learning classifiers and explain their predictions.

#### SKLearn-CRFsuite
[https://github.com/TeamHG-Memex/sklearn-crfsuite](https://github.com/TeamHG-Memex/sklearn-crfsuite) (stable) sklearn-crfsuite is a thin CRFsuite (python-crfsuite) wrapper which provides interface similar to scikit-learn. sklearn_crfsuite.CRF is a scikit-learn compatible estimator: you can use e.g. scikit-learn model selection utilities (cross-validation, hyperparameter optimization) with it, or save/load CRF models using joblib.

#### Tensorboard-Logger
[https://github.com/TeamHG-Memex/tensorboard_logger](https://github.com/TeamHG-Memex/tensorboard_logger) (stable) Log TensorBoard events without touching [TensorFlow](https://www.tensorflow.org/), an open source software library for numerical computation using data flow graphs. TensorFlow was originally developed by researchers and engineers working on the Google Brain Team within Google's Machine Intelligence research organization for the purposes of conducting machine learning and deep neural networks research, but the system is general enough to be applicable in a wide variety of other domains as well.

## Domain discovery systems

### Domain Discovery Tool (DDT)

[https://github.com/ViDA-NYU/domain_discovery_tool](https://github.com/ViDA-NYU/domain_discovery_tool)

DDT is an interactive system that helps users explore and better understand a domain (or topic) as it is represented on the Web. DDT allows a domain expert to visualize and analyze pages returned by a search engine or a crawler and provide feedback about their relevance. Based on this feedback, the system guides the user in the creation of a model for the domain of interest. This model can then be used by a focused crawler such as ACHE to automatically discover and download a large number of web pages that belong to the domain.

### Site Hound (formerly THH)
[https://github.com/TeamHG-Memex/sitehound ](https://github.com/TeamHG-Memex/sitehound)

Site Hound (previously THH) is a Domain Discovery Tool that extends the capabilities of commercial search engines using automation and human-in-the-loop (HITL) machine learning, allowing the user efficiently expand the set of relevant web pages within his domain/s or topic/s of interest. Site Hound is the UI to a more complex set of tools (which are described and linked to in this repository READ ME). Site Hound was developed under the Memex Program by HyperionGray LLC in partnership with Scrapinghub, Ltd.

### QuickPin
[https://github.com/TeamHG-Memex/quickpin](https://github.com/TeamHG-Memex/quickpin) (stable) QuickPin is a tool for quickly flagging and examining online accounts related to a topic of interest. A Python wrapper for the API can be found at https://github.com/TeamHG-Memex/quickpin-api.

## Extractors/NLP/Image/Text processing

#### Extraction Toolkit (etk)
[https://github.com/usc-isi-i2/etk](https://github.com/usc-isi-i2/etk]) (alpha).
A general purpose toolkit for easily extracting semi-structured data, tables and entities from arbitrary web pages. Contains a rich set of entity extractors.

#### Landmark Extractor (landmark)
[https://github.com/inferlink](https://github.com/inferlink) (beta).
An automated tool to create rules that extract data from web sites containing templetized pages.
Landmark rules are directly usable in **etk**.

#### FreeEed 
[https://github.com/shmsoft/FreeEed](https://github.com/shmsoft/FreeEed) (stable) FreeEed (Free Electronic Evidence Discovery) is open source software for legal discovery (eDiscovery). It is created and maintained by SHMsoft, Inc., and is licensed under Apache 2 license. Development on FreeEed was partially supported under the Memex program. FreeEed software is intended to process any number of electronic documents, extract metadata and text, and cull them based on keywords. It produces a "load file" with metadata, and an output zip file, which contains all of the text extracted from each document, as well as original (or "native") files. It is designed to be scalable. It works on a Hadoop cluster of tens or hundreds of machines. Work is be divided among and processed by all the machines. It will also work on the Amazon EC2 cloud.

#### HTML-Text Extractor
[https://github.com/TeamHG-Memex/html-text](https://github.com/TeamHG-Memex/html-text) (stable) Extract text from HTML. How is html_text different from .xpath('//text()') from LXML or .get_text() from Beautiful Soup? Text extracted with html_text does not contain inline styles, javascript, comments and other text that is not normally visible to the users.

#### Extract-HTML-Diff
[https://github.com/TeamHG-Memex/extract-html-diff](https://github.com/TeamHG-Memex/extract-html-diff) (stable) This package allows you to extract a difference between two html pages: given pages A and B, it will try to extract parts of A that are changed in B. It uses lxml.html.diff under the hood. but provides only changed parts as HTML.

#### ImageSift - Color Fingerprint Image Similarity
[https://github.com/unchartedsoftware/TellFinder-ImageSift](https://github.com/unchartedsoftware/TellFinder-ImageSift) (stable).
A reference implementation of the image similarity algorithm used by TellFinder. Includes a sample application and training data.

#### ImageSimilarity
[https://github.com/TeamHG-Memex/imageSimilarity](https://github.com/TeamHG-Memex/imageSimilarity) (WIP) Given a new image, the ImageSimilarity library will score it based on its similarity to a known set of images using ssim, diff hash, average hash, and phash.

#### BK-String
[https://github.com/TeamHG-Memex/bk-string](https://github.com/TeamHG-Memex/bk-string) (stable) A BK Tree based approach to storing and querying strings by Levenshtein Distance.

#### Py-BKString
[https://github.com/TeamHG-Memex/py-bkstring](https://github.com/TeamHG-Memex/py-bkstring) (stable) A python wrapper for the bk-string C project.

#### Rs-BKString
[https://github.com/TeamHG-Memex/rs-bkstring](https://github.com/TeamHG-Memex/rs-bkstring) (stable) A BK Tree Library written in Rust.

#### CMU - Compute Features
https://github.com/autoncompute/ComputeFeatures This project contains the code for pre-computing pool5 features of database images.

#### CMU - ITQ Hashing and Similarity Search Service
https://github.com/autoncompute/ScalableLSH This project contains the code for computing ITQ hashing results based on pre-computed pool5 features and deploying a search server.

#### CMU - Distribured ITQ
https://github.com/autoncompute/BigITQ This project contains a distributed implementation of ITQ over SPARK.

#### MIT-LL - pySLGR
[https://github.com/mitll/pyslgr](https://github.com/mitll/pyslgr) A Python tool for Speaker, Language, and Gender Recognition (SLGR) and general meta-data extraction.

#### MIT-LL - MITIE
[https://github.com/mit-nlp/MITIE](https://github.com/mit-nlp/MITIE) State-of-the-art information extraction tools for named entity extraction and binary relation detection as well as tools for training custom extractors and relation detectors.

#### MIT-LL - topic-clustering
[https://github.com/mitll/topic-clustering](https://github.com/mitll/topic-clustering) Efficient topic-modeling via Probabilistic Latent Semantic Analysis (pLSA)

#### MIT-LL - TweetE
[https://github.com/mitll/TweetE](https://github.com/mitll/TweetE) Tools for scraping of twitter data, conversion, text analysis and graph construction. This software consists of several easy-to-use Python modules for several aspects of natural language processing with Twitter.

#### MIT-LL - LiLAC
[https://github.com/mitll/LiLAC](https://github.com/mitll/LiLAC) A python tool for author classification via lexiographical features.

#### MIT-LL - LLString
[https://github.com/mitll/LLString](https://github.com/mitll/LLString) A python library for basic string processing and soft-string matching. Includes basic string normalization and similarity matching as well as functionality to build classifiers.

#### MIT-LL - LLHash
[https://github.com/mitll/LLHash](https://github.com/mitll/LLHash) Tools for efficient nearest-neighbor search of vector and string data using locality sensitive hashing techniques.

#### MIT-LL - LLClass
[https://github.com/mitll/LLClass](https://github.com/mitll/LLClass) Document classification in Java. Pre-trained models for language identification.

#### MIT-LL - Text.jl
[https://github.com/mit-nlp/Text.jl](https://github.com/mit-nlp/Text.jl) Text processing and document classification in Julia. 

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

#### Stories Components
[https://github.com/unchartedsoftware/stories-personas](https://github.com/unchartedsoftware/stories-personas) (stable).
UI component for the Stories 'Personas' visualization.

[https://github.com/unchartedsoftware/stories-facets](https://github.com/unchartedsoftware/stories-facets) (stable).
UI component for the Stories 'Facets' visualization.

#### TellFinder Data API
[https://github.com/unchartedsoftware/tellfinder-data](https://github.com/unchartedsoftware/tellfinder-data) (stable).
RESTful server for accessing all of TellFinder data models, analytics and search strategies.

#### TellFinder Pipeline Core
[https://github.com/unchartedsoftware/tellfinder-pipeline-core](https://github.com/unchartedsoftware/tellfinder-pipeline-core) (stable).
General purpose distributed processes pipeline for ingesting web data into the TellFinder data model. Includes general purpose data cleaning, extraction, normalization and analytics. Based on the [https://github.com/unchartedsoftware/sparkpipe-core](Uncharted Spark Pipeline).

#### TellFinder UI core
[https://github.com/unchartedsoftware/tellfinder-ui-core](https://github.com/unchartedsoftware/tellfinder-ui-core) (stable).
UI Component library for building TellFinder applications.  

#### TellFinder Universal
[https://github.com/unchartedsoftware/tellfinder-universal](https://github.com/unchartedsoftware/tellfinder-universal) (stable).
Fully functional end-to-end application showing TellFinder UI components and Data API on a new domain. Includes sample data.

### TorFlow
[https://github.com/unchartedsoftware/torflow](https://github.com/unchartedsoftware/torflow) (stable demo).
A visualization of data flow in the Tor Network.

### Georgetown Dynamic Search
[https://github.com/SharonLingqiongTan/QA_interface](https://github.com/SharonLingqiongTan/QA_interface) (development)

#### Structured query Search
Provide phone basic search like phone, email search. And also provide other features search like name, age (range search), ethnicity, nationality, location, hair color, eye color and so on.
Search interface based on Lemur and ElasticSearch, allowing user to search by structured query, unstructured query and tag documents. Also provides text/image drag & drop function and image search.

### HG Profiler
[https://github.com/TeamHG-Memex/hgprofiler](https://github.com/TeamHG-Memex/hgprofiler) (stable) HG Profiler is a tool that allows users to take a list of entities from a particular source and look for those same entities across a predefined list of other sources.

## Other Utilities

#### Agnostic
[https://github.com/TeamHG-Memex/agnostic](https://github.com/TeamHG-Memex/agnostic) (stable) Agnostic is a light-weight, easy-to-learn, and flexible database migration tool in which migration scripts are written in pure SQL. It is agnostic to database, programming language, and object relational mapper (ORM).

#### JSON Lines
[https://github.com/TeamHG-Memex/json-lines](https://github.com/TeamHG-Memex/json-lines) (dev) This is a tiny library for reading JSON lines (.jl) files, including gzipped and broken files. JSON lines is a text file format where each line is a single json encoded item. Reading a well-formed JSON lines file is a one-liner in Python. But if the file can be broken (this happens when the process writing it is killed), handling all exceptions takes 10x more code, especially when the file is compressed.

#### Image and text drag and drop
Allow user to drag and drop image or text to drop box.

#### Image search
Allow user to search similar image and return document.

### Clustering

#### CMU - Text Clustering
https://github.com/autoncompute/KwikCluster Scalable clustering of text documents.

### Anomaly Detection

#### CMU - TAD
https://github.com/autonlab/tad  A service to run temporal anomaly detection on time series of counts.
