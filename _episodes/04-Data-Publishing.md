---
title: "Lesson 3: Data Publishing"
teaching: Self-paced
exercises: 1
questions:
- "Am I ready to publish my data?"
- "What resources are available for your research data needs?"
objectives:
- "To learn what constitutes good stewardship of research data"
- "To learn about resources that can be used to assist in the process of data stewardship and publication"
keypoints:
- There exist well defined recommendations for publishing data.
- There are practical guidelines and tools to assist in the publication of data.

---

### Introduction

This lesson provides an overview of best practices in data publishing.  Note that we prefer the term "data publishing" to "data sharing" because the goal of this module is to make data available in public for third party inspection and re-use.

#### History of open mandates and guidelines

Prior to computers and the internet, publishing data routinely was really not possible beyond what we could publish in articles or books. Rather it was the hypotheses proposed, the experimental design, the analysis and the insights gained from collected data that were valued and preserved through our system of journals and books. Eventually, a culture grew up around scientific publishing where data were considered disposable after some specified regulatory period or a personal asset to be maintained and exploited for personal use ([Martone et al., 2018](https://www.ncbi.nlm.nih.gov/pubmed/29481105)).

As science continues to move online, almost all major funding agencies in the US and abroad are developing policies around open sharing of research data and other research products like code. These policies seek to promote the integrity of scientific research through greater transparency given recent concerns about scientific reproducibility but are also driven by the promises of new insights to be gained from increased human- and machine-based access to data.

Within neuroimaging there exist a set of recommendations for best practices in data analysis and sharing. To advance open science in neuroimaging, the Organization for Human Brain Mapping's Committee on Best Practice in Data Analysis and Sharing (COBIDAS) has released a number of recommendations. ([doi: https://doi.org/10.1101/054262](dx.doi.org/https://doi.org/10.1101/054262)). These guidelines for various aspects of a study are provided via tabular listings of items that will help plan, execute, report and finally share research in support of reproducible neuroimaging.

#### Data sharing versus data publishing

We are seeing more and more calls for domains not just to establish a culture of human-centric sharing, i.e., “data available upon request”, but to move towards a more e-science vision, where researchers conduct their research digitally and where data standards and programmatic interfaces make it easy for machines to access and ingest large amounts of data. To achieve this goal requires that the products of research, including the data, be [FAIR](http://www.reproducibleimaging.org/module-FAIR-data/01-Web-of-Data/) not just by humans but by machines. We have already covered the [FAIR principles](http://www.reproducibleimaging.org/module-FAIR-data/01-Web-of-Data/) in another module. As a review, FAIR stands for Findable, Accessible, Interoperable and Re-usable. FAIR requires that enough metadata be associated with a data set so that it can be interpreted and reused appropriately, but also that data can be easily coupled to computational resources that can operate on them at scale, the provenance of these research products can be tracked as they transition between uses and the ability to find, access and reuse digital artifacts using computational interfaces (APIs) with minimal restrictions.

In other words, to take advantage of data, time, attention and resources must be devoted to **publishing** data and code, just as we spend time and energy publishing enduring narrative works to be understood and used by third parties, now and in the future.

#### Best Practices for publishing data

We are still in the early days of publishing data, and the FAIR principles have not yet been interpreted completely within any domain ([Mons et al., 2017](http://content.iospress.com/articles/information-services-and-use/isu824#ref007)). Part of the remit of ReproNim is to establish a viable set of FAIR data practices for neuroimaging.  But some best practices and practical guidelines have already become clear:

**1) Proper data management throughout the research lifecycle:**  Documentation and management of data within the laboratory is a critical first step in publishing data. Many laboratories still have no formal systems for storing, annotating and managing critical lab data. Often when a graduate student or post-doc leaves, valuable data and metadata are lost. How many data sets are on archival media such as zip drives that are no longer readable? As the FAIR standard states, rich and standardized metadata is critical to ensure interoperability and re-usability. While some of this annotation can be done after the fact, establishing good data management practices within the laboratory, understanding what minimal information and data standards will be required before the experiment is performed, and ensuring that the data are properly stewarded throughout the lifecycle will save countless hours during and after the study.

Funding agencies are starting to require that researchers have a data management plan in their grant applications. Towards that end, many research libraries are now creating [practical guidance and resources for effective data management](https://library.ucsd.edu/research-and-collections/data-curation/data-management/best-practices.html) and for creating acceptable data management plans for funding agencies.

**2) Ensure that your data is deposited into a reputable repository when publishing data:** The simplest and most effective mechanism for making data FAR is to deposit data in a qualified data repository ([Roche et al., 2014](dx.doi.org/10.1371/journal.pbio.1001779); [Gewin, 2016](https://doi.org/10.1038/nj7584-117a); [White et al., 2013](https://ojs.library.queensu.ca/index.php/IEE/article/view/4608)). Hosting data on personal websites or even as supplementary material for a published article is not ideal. The first instance is prone to link rot while both generally mean that data will not be further curated. Known impediments to re-usability, e.g, proprietary formats, may not be caught. Putting data in the cloud is also not a panacea, if the FAIR principles are not followed.

Many data repositories have been created for scientific data (see Exercise 1:  Finding a data repository for your data). Qualified data repositories ensure long term maintenance of the data, generally enforce enforce community standards, and handle things like obtaining an identifier, maintaining a landing page with appropriate descriptive metadata, and providing programmatic access. Many institutions are beginning to provide data management services

Types of repositories: A variety of types of repositories are available, from specialized repositories developed around a specific domain, e.g., NITRC-IR, OpenNeuro, to general repositories that will take all domains and most data types, e.g., Figshare, Dryad, OSF, DataVerse, Zenodo (Table 2). Many research institutions are maintaining data repositories for their researchers as well (e.g., University of California DASH).

The advantage of more specific repositories is that they can invest in much more specialized metadata, data models, formats and tools, compared to the more generalist repositories. Because the generalist repositories contain mixtures of different data types across many domains, they have a difficult time harmonizing across different data sets or developing data representations that allow programmatic access to the full data without the need for significant human intervention.

**3) Plan ahead when publishing your data:** The process and costs associated with publishing research articles are well known to researchers, and they ensure that they include adequate resources within their research proposals to ensure that they can prepare and publish articles.  Data are a lot more varied in size and complexity than research articles, and thought must be given to how they are going to be published before they are collected. For data of a reasonable size, most repositories are still hosting the data free of charge. Some repositories, e.g., NDAR, require a fee to deposit data, but they also provide cost estimates that can be included within grant proposals. In addition to costs, just as with publishing articles, you need to ensure that all parties who have contributed to the data are credited and agree to publishing the data (see below: Data citation).

Here are some things to consider:

***Before the data are collected:***

  -  **Consult your library or someone else familiar with proper data management** to **ensure that your data will be properly managed throughout the lifecycle**. Both the US National Institutes of Health and the National Science Foundation require a data management plan as part of the proposal.

  -  Make sure that you have **requested adequate funds for proper management and curation of the data** in order to make it open.

  -  **Identify the repository that you will use to publish your data.**  Make sure you have requested appropriate funds for archiving the data.  If the data are of reasonable size (a moving target), most repositories will archive the data for free. But very large data sets, e.g., large imaging datasets, may have costs associated with long term archiving.  Consult with the repository before submitting your proposal to ensure adequate funds are available.

  -  Ensure you have the proper **permissions to make your data open** from your institution, colleagues and subjects. See the [permissions worksheet](https://docs.google.com/document/d/1jLlWbzyTP9m3uMXPrAsrgEx5iXdPJvZ60cB7sDPGgxE/edit) for guidance.

  -  **Consider not only the primary data, but any background or supplemental data**, e.g., animal care records, and whether these can be shared. You may be required to go through your university for this.

**Tips for making data FAIR**
  -  Well documented data are easier to understand
  -  Properly formatted data are easier to use in a variety of software,
  -  Data that are shared in established repositories with no or minimally restrictive licenses are easier for others to find and use. (from White et al., 2013)
  - For more information on FAIR, please see the Web of Data lesson (http://www.reproducibleimaging.org/module-FAIR-data/01-Web-of-Data/)

#### DataLad

DataLad builds on top of git-annex and extends it with an intuitive command-line interface. It enables users to operate on data using familiar concepts, such as files and directories, while transparently managing data access and authorization with underlying hosting providers.

#### Credit for publishing data

Publishing data should be no different than publishing an article:  the creators should be credited and the authors and data formally cited when it is reused. This view is expressed in the [Joint Declaration of Data Citation principles](https://www.force11.org/group/joint-declaration-data-citation-principles-final), issued and endorsed by organizations around the globe.

In recognition of the growing importance of publishing data, publishers are providing specialized journals, e.g., Scientific Data, published by Springer-Nature, or a specialized article type called a data paper, specifically for publishing well curated and described data sets. These papers are published using traditional publishing metadata and article structure, but are not expected to include any analyses or conclusions;  rather the paper is devoted to providing rich metadata and a rigorous description of experimental and data collection mechanisms.  Scientific Data also implements a standard format for structuring metadata, to ensure that the data is FAIR.  These journals usually require that data are deposited in an approved community repository and they provide lists of [recommended repositories](https://www.nature.com/sdata/policies/repositories).

Publishing a data paper is one way to ensure that data can be cited.  But many journals are currently working on implementing more formal systems of data citation, led by community efforts to push for equal status for data in the publishing pipeline (e.g., Joint Declaration of Data Citation Principles; Starr et al., 2015)).  Citations to data sets would look like citations to articles, with a standard set of metadata, and would appear in the reference list. With the ability to list published datasets on a scientific CV, cite them within published articles, and search for them via tools like DataMed, data is finally taking its place as a primary product of scholarship.

A formal citation system assigns credit for the re-use of data, but also establishes links to the evidence on which claims are based while providing the means for tracking and therefore measuring impact of data re-use. In our current publishing system, authors adopt a variety of styles for referencing data when they are re-used, from accession numbers, to URL’s, to citing a paper associated with the data set. Some journals set aside a special section on data use which contain lists of data sets and other resources. Unlike references to articles which have a standard format and tools and services to insert them and analyze citations, uncovering and tracking re-use of data typically involves using manual identification, text mining and natural language processing approaches, requiring full text access and considerable time and effort (Read et al., 2015).

[Honor et al. (2016)](http://journal.frontiersin.org/article/10.3389/fninf.2016.00034/full) have published a recommendation for citing neuroimaging data sets:


> #### References
> Online courses:
>
>   - [FORCE11 Decision trees for making data open, FAIR and citable ](https://www.force11.org/scholarly-commons/practice)
>
> Additional materials:
>   -  [Honor, L. B., Haselgrove, C., Frazier, J. A., & Kennedy, D. N. (2016). Data Citation in Neuroimaging: Proposed Best Practices for Data Identification and Attribution. Frontiers in Neuroinformatics, 10, 34. doi:10.3389/fninf.2016.00034](http://journal.frontiersin.org/article/10.3389/fninf.2016.00034/full)
>
>   - [Martone, M. E., Garcia-Castro, A. and VandenBos, G. R. Data sharing in psychology. Am Psychol. 2018 Feb-Mar;73(2):111-125. doi: 10.1037/amp0000242](https://www.ncbi.nlm.nih.gov/pubmed/29481105)
>
>   - [White EP, Baldridge E, Brym ZT, Locey KJ, McGlinn DJ, Supp SR. (2013) Nine simple ways to make it easier to (re)use your data. PeerJ PrePrints 1:e7v2 https://doi.org/10.7287/peerj.preprints.7v2](https://doi.org/10.7287/peerj.preprints.7v2)
>   - [Description](http://URL)
>
{: .callout}
