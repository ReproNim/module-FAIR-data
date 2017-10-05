---
title: "Data Publishing"
teaching: Self Paced
exercises: 1
questions:
- "Q1:  Am I ready to publish my data?"
objectives:
- "Objective 1"
- "Objective 2"
keypoints:
- We want to use this template to provide lesson materials in an open and useful format.

- This is in line with our overall goal of making science (including scientific training) more open.

---

### Introduction

This module provides an overview of best practices in data publishing.  Note that we prefer the term "data publishing" to "data sharing" because the goal of this module is to make data available in public for third party inspection and re-use.    
> #### Lessons
> *_History of open mandates and guidelines_

Prior to computers and the internet, pubishing data routinely was really not possible beyond what we could publish in articles or books.  Consequently, a culture grew up around scholarly publishing where data were considered disposable after some specified regulatory period. Rather it was the hypotheses proposed, the experimental design, the analysis and the insights gained from collected data that were valued and preserved through our system of journals and books.  
 
Almost all major funding agencies in the US and abroad are developing policies around open sharing of research data and other research products. These policies have been put into place to promote the integrity of scientific research through greater transparency in light of recent concerns about scientific reproducibility across several fields. These policies are also driven by the promises of new insights to be gained from increased human- and machine-based access to research outputs. 

> *Data sharing versus data publishing
 
Towards these ends, we are seeing more and more calls for domains not just to establish a basic culture of human-centric sharing, i.e., “upon request”, but to move towards a more e-Science vision, where researchers conduct their research digitally and where data standards and programmatic interfaces make it easy for machines to access and ingest large amounts of data.  To achieve this goal requires that the products of research, including the data, be easily coupled to computational resources that can operate on them at scale, and that the provenance of these research products can be tracked as they transition between uses. It requires the ability to find, access and reuse digital artifacts using computational interfaces (API’s) with minimal restrictions. 

In other words, to take advantage of data, time, attention and resources must be devoted to publishing data and code, just as we spend time and energy publishing enduring narrative works to be understood and used by third parties, now and in the future.  

> *Best Practices for publishing data

We have already covered the FAIR principles in another module.  As a review, FAIR stands for Findable, Accessible, Interoperable and Re-usable.  

We are still in the early days of publishing data, and the FAIR principles have not yet been interpreted completely within any domain [Mons et al., 2017](http://content.iospress.com/articles/information-services-and-use/isu824#ref007).  Part of the remit of ReproNIM is to establish a viable set of FAIR data practices for neuroimaging.  But some best practices and practical guidelines have already become clear:

**1)  Proper data management throughout the research lifecycle:**  Documentation and management of data within the laboratory is a critical first step in publishing data. Many laboratories still have no formal systems for storing, annotating and managing critical lab data.  Often when a graduate student or post-doc leaves, valuable data and metadata are lost.  How many data sets are on archival media such as zip drives that are no longer readable?  As the FAIR standard states, rich and standardized metadata is critical to ensure interoperability and re-usability.  While some of this annotation can be done after the fact, establishing good data management practices within the laboratory, understanding what minimal information and data standards will be required before the experiment is performed, and ensuring that the data are properly stewarded throughout the lifecycle will save countless hours during and after the study. 

Funding agencies are starting to require that researchers have a data management plan in their grant applications.  Towards that end, many research libraries are now creating [practical guidance and resources for effective data management](https://library.ucsd.edu/research-and-collections/data-curation/data-management/best-practices.html) and for creating acceptable data management plans for funding agencies.

**2)  Ensure that your data is deposited into a reputable repository when publishing data:**  The simplest and most effective mechanism for making data FAR is to deposit data in a qualified data repository (Roche et al., 2014; Gewin, 2016; White et al., 2013).  Hosting data on personal websites or even as supplementary material for a published article is not ideal. The first instance is prone to link rot while both generally mean that data will not be further curated. Known impediments to re-usability, e.g, proprietary formats, may not be caught. Putting data in the cloud is also not a panacea, if the FAIR principles are not followed.  

Many data repositories have been created for scientific data (see Exercise 1:  Finding a data repository for your data). Qualified data repositories ensure long term maintenance of the data, generally enforce enforce community standards, and handle things like obtaining an identifier, maintaining a landing page with appropriate descriptive metadata, and providing programmatic access. Many institutions are beginning to provide data management services

Types of repositories:  A variety of types of repositories are available, from specialized repositories developed around a specific domain, e.g., NITRC-IR, openfMRI, to general repositories that will take all domains and most data types, e.g.,Figshare, Dryad, OSF, DataVerse, Zenodo (Table 2). Many research institutions are maintaining data repositories for their researchers as well (e.g., University of California DASH).  
 
The advantage of more specific repositories is that they can invest in much more specialized metadata, data models, formats and tools, compared to the more generalist repositories. Because the generalist repositories contain mixtures of different data types across many domains, they have a difficult time harmonizing across different data sets or developing data representations that allow programmatic access to the full data without the need for significant human intervention.  

**3) Plan ahead when publishing your data:**  The process and costs associated with publishing research articles are well known to researchers, and they ensure that they include adequate resources within their research proposals to ensure that they can prepare and publish articles.  Data are a lot more varied in size and complexity than research articles, and thought must be given to how they are going to be published before they are collected. For data of a reasonable size, most repositories are still hosting the data free of charge. Some repositories, e.g., NDAR, require a fee to deposit data, but they also provide cost estimates that can be included within grant proposals.In addition to costs, just as with publishing articles, you need to ensure that all parties who have contributed to the data are credited and agree to publishing the data (see below: Data citation).  

Here are some things to consider:

***Before the data are collected:***
..*Consult your library or someone else familiar with proper data management to ensure that your data will be properly managed throughout the lifecycle.  Both the US National Institutes of Health and the National Science Foundation require a data management plan as part of the proposal.  
..*Make sure that you have requested adequate funds for proper management and curation of the data in order to make it open.
..*Identify the repository that you will use to publish your data.  Make sure you have requested appropriate funds for archiving the data.  If the data are of reasonable size (a moving target), most repositories will archive the data for free.  But very large data sets, e.g., large imaging datasets, may have costs associated with long term archiving.  Consult with the repository before submitting your proposal to ensure adequate funds are available.
..*Ensure you have the proper permissions to make your data open from your institution, colleagues and subjects.  See the [permissions worksheet](https://docs.google.com/document/d/1jLlWbzyTP9m3uMXPrAsrgEx5iXdPJvZ60cB7sDPGgxE/edit) for guidance.
..*Consider not only the primary data, but any background or supplemental data, e.g., animal care records, and whether these can be shared.  You may be required to go through your university for this.





> *DataLad (todo:  Publishing data using Data Lad). 

> *Credit for publishing data*

Publishing data should be no different than publishing an article:  the creators should be credited and the authors and data formally cited when it is reused. This view is expressed in the [Joint Declaration of Data Citation principles](https://www.force11.org/group/joint-declaration-data-citation-principles-final), issued and endorsed by organizations around the globe. 

In recognition of the growing importance of publishing data, publishers are providing specilized journals, e.g., Scientific Data, published by Springer-Nature, or a specialized article type called a data paper, specifically for publishing well curated and described data sets. These papers are published using traditional publishing metadata and article structure, but are not expected to include any analyses or conclusions;  rather the paper is devoted to providing rich metadata and a rigorous description of experimental and data collection mechanisms.  Scientific Data also implements a standard format for structuring metadata, to ensure that the data is FAIR.  These journals usually require that data are deposited in an approved community repository and they provide lists of [recommended repositories](https://www.nature.com/sdata/policies/repositories).

Publishing a data paper is one way to ensure that data can be cited.  But many journals are currently working on implementing more formal systems of data citation, led by community efforts to push for equal status for data in the publishing pipeline (e.g., Joint Declaration of Data Citation Principles; Starr et al., 2015)).  Citations to data sets would look like citations to articles, with a standard set of metadata, and would appear in the reference list. With the ability to list published datasets on a scientific CV, cite them within published articles, and search for them via tools like DataMed, data is finally taking its place as a primary product of scholarship.

A formal citation system assigns credit for the re-use of data, but also establishes links to the evidence on which claims are based while providing the means for tracking and therefore measuring impact of data re-use. In our current publishing system, authors adopt a variety of styles for referencing data when they are re-used, from accession numbers, to URL’s, to citing a paper associated with the data set. Some journals set aside a special section on data use which contain lists of data sets and other resources. Unlike references to articles which have a standard format and tools and services to insert them and analyze citations, uncovering and tracking re-use of data typically involves using manual identification, text mining and natural language processing approaches, requiring full text access and considerable time and effort (Read et al., 2015). 

[Honor et al. (2016)](http://journal.frontiersin.org/article/10.3389/fninf.2016.00034/full) have published a recommendation for citing neuroimaging data sets:





> #### References
> Online courses:
>
>   - [FORCE11 Decision trees for making data open, FAIR and citable ](https://www.force11.org/scholarly-commons/practice)
>
> Additional materials:
>
>   - [Description](http://URL)
>   - [Description](http://URL)
>
> Relevant Books:
>
>   - [Description](http://URL) Text1...
>     TEXT2...
{: .callout}

### Best Practices for publishing data

Lesson...

#### Publishing your data via community resources

#### Publishing data with journals

#### Publishing via local or cloud resources

### DataLad

Lesson...

### Data citation best practices

Lesson...


> ## Exercises and challenges (click on the arrow to the right to open)
>
>  Boxes with "challenges" can be interleaved with the lesson materials.
>  Consider adding a challenge every 15 minutes or so.
>    - This helps participants stay engaged.
>    - It surfaces questions that learners have as they go along.
>    - It breaks up the instruction, providing a bit of a diversion.
>    - It gives people a chance to engage in peer instruction, which is
>      is [known to help learning](https://en.wikipedia.org/wiki/Peer_instruction).
{: .challenge}


