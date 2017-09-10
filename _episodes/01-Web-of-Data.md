---
title: "Introduction to the Web of Data"
teaching: Self Paced
exercises: 2
questions:
- "What is a research object and how do I properly identify it?"
- "What is linked open data?"
- "What are the FAIR Data principles?"

objectives:
- "Understanding identifiers"
- "History of open and linked data"
- "Overview of the FAIR principles"

keypoints:
- "Understanding the FAIR Data principles"
- "Understanding identification of FAIR data"

---

### Introduction

This module provides an overview of strategies for making research outputs available through the web, with an emphasis on data.  It introduces concepts such persistent identifiers, linked data, the semantic web and the FAIR principles.  It is designed for those with little to no familiarity with these concepts. More technical discussions can be found in the reference materials.

> #### Lessons
> - Overview of the current ecosystem
> - Research objects and identifier systems
> - Short history of open & linked data technologies
> - Benefits of linked open data with examples
> - Towards the FAIR principles
{: .callout}

> #### References
> Additional materials:
>
>   - [Linked Data Guides and Tutorials](http://linkeddata.org/guides-and-tutorials)
>   - [Linked Data: Tim Berners-Lee, 2006](https://www.w3.org/DesignIssues/LinkedData.html)
>   - McMurray et al. (2015) 10 Simple rules for design, provision, and reuse of persistent identifiers for life science data, [Zenodo, 10.5281/zenodo.31765](https://doi.org/10.5281/zenodo.31765)
>   - [W3C RDF Primer](https://www.w3.org/TR/rdf11-concepts/)
>
> Relevant Books:
>
>   - [Tom Heath and Christian Bizer (2011) Linked Data: Evolving the Web into a Global Data Space (1st edition). Synthesis Lectures on the Semantic Web: Theory and Technology, 1:1, 1-136. Morgan & Claypool.](http://linkeddatabook.com/editions/1.0/)
{: .callout}

### Research objects and identifier systems

The advent of computers and networks have allowed scientists to share not only the final report of the work, i.e., the scientific article, but also additional research products that form an integral part of the work, e.g., data, code,  workflows and even works like slide presentations.  The term "research object" in a general sense connotes these many outputs of scientific research. The term ["research object"](https://en.wikipedia.org/wiki/Research_Object) is also used specifically to refer to a method for the identification, aggregation and exchange of scholarly information on the Web.  The basic idea is that each of these objects should have its own persistent identifier (see below) and objects that belong together, e.g., an article with its associated code and data, should have some means of being aggregated, so that all associated research objects can be discovered together.  Although this might seem to be obvious, as research objects are scattered across different repositories on the web, the connections between them are often lost.

One of the most important concepts to understand and implement when developing information systems on the web for robust and reproducible science is that of globally unique and persistent identifiers [(PIDs)](https://en.wikipedia.org/wiki/Persistent_identifier). You will see references to PIDs throughout this tutorial.  Globally unique and peristent identifiers are exactly what they sound like:  a unique and long-lasting reference to something, e.g., documents, files, books, people and even the concepts that define a field (ontologies).  Globally unique means that the identifier points to only a single entity on a global scale. Many of you may be familiar with locally unique identifiers, e.g., database accession numbers, that are unique within a single source.  But when utilizing the web to retrieve information, we have to consider the entire web.

Identifiers for non-digital objects: Persistent identifiers can still be assigned to things that are not natively digital, e.g., people, reagents, concepts.  In this case, some authority issues identifiers for these entities.  The PID can be thought of as "digital middle names" for things we refer to. If they are unique-that is, each identifier identifies only one thing-and they are designed to be used by computers, then PIDs can be used to locate references to these particular entities reliably and disambiguate that one entity from others that may have similar names. For example, the concept "nucleus" can point to the nucleus of a cell, of an atom or of the brain. But these three concepts each have unique identifiers in biological terminologies such as the Gene Ontology or UMLS (Unified Medical Language System).  When these identifiers are used inside of databases or research articles, a machine can easily tell them apart.

PIDs are distinct from locators like URL's in that they retrieve an object independent of where the object is located on the web.  We are all familiar with broken links on the web.  A broken link happens when a web browser sends out a request to a server for a document with a specified URL.  If that URL no longer exists, because, for example, the system administrator migrated systems and created a new URL or if someone decided no longer to pay the fee to keep up a particularly domain name on the internet, we get a 404: Document not found error. In scholarship, the [404 error](http://www.cs.umd.edu/~golbeck/LBSC690/SemanticWeb.html) is particularly pernicious as it breaks the chain of evidence that is provided within a scientific paper.  If we refer to a web page that no longer exists, we have no way to verify or benefit from the information in that web page.  Broken links can be avoided by making sure that re-direct pages are available for old URLs, but how do you know that the new URL actually points to the same document?  Also, what happens when multiple copies of the same article exist in different places?  Each of those places would have its own URL, making it look to a computer as if the objects they reference are different.

PIDs actually address both of these problems. The identifier is separated from the location so that it buffers against changes in location.  If a web document is moved to a new location, the new location is registered with the resolving system so that it now points to the same object in a new place.  If the same object is present in multiple locations, e.g., a scientific article can be found at the publisher's web site, in Pub Med Central and in platforms such as Mendeley,the DOI listed as part of the metadata is the same, so we know that it is the same article in different places.  It is important to note that these identifier systems, as will discussed below in the FAIR principles, are not magic.  Rather they are a social contract between the publisher of research objects and users that they will maintain the integrity of the resolution services.

> ## Exercise: Identifiers (click on the arrow to the right to open)
> **What is the difference between a globally unique and locally unique identifier?**
>
> Consider the Pub Med database.  Pub Med assigns a unique idenfier, the PMID, to each article, e.g., PMID:26978244.  If you type in the identifier, [26978244](https://www.ncbi.nlm.nih.gov/pubmed/?term=26978244), into the Pub Med search box, you will get exactly one article, in this case on the FAIR data principles.  But now type that number into Google search. You will see the [the article about the FAIR data principles](https://www.ncbi.nlm.nih.gov/pubmed/26978244) but also lots of other things identifed by this number, e.g., [an image of a soccer player](https://www.dreamstime.com/stock-images-sk-rapid-vs-austria-wien-image26978244), [a house for sale](http://www.rightmove.co.uk/property-for-sale/property-26978244.html). In other words, divorced from a particular database, the identifer 26978244 is meaningless.
>
> In contrast, when you type in a globally unique identifer, e.g., a DOI, it should identify one and only one object on the web, in this case the article about the FAIR data principles. To see the difference, notice the list of search results when you type in the DOI for this article: 10.1038/sdata.2016.18.

> As we will discuss in a later session, it is possible to turn a locally unique ID into a globally unique ID by adding additional features, e.g., namespaces before the ID, e.g., pubmed/.
>
>
> **What is the difference between searching for an PID and resolving an PID?**
>
> There is a difference between identifying an object and accessing it.  In the above exercise, when you type the DOI or PMID into a web search, it performs a search for that number just like it would for any search string.  Note that the list of results includes URl's that will take you to the article itself, e.g., https://www.nature.com/articles/sdata201618, or that contain references to the article, e.g., http://www.ontoforce.com/why-data-should-be-fair/.  A resolving service is more specific;  it is designed to resolve to the object that is being referenced. To see how a resolver works, copy  http://dx.doi.org/ into your browser followed by the DOI for the FAIR principles article 10.1038/sdata.2016.18. Note that it takes you to the web URL https://www.nature.com/articles/sdata201618 where the article is found.  This exercise also illustrates the difference between a PID and URL. If the URL for the article changes, Nature is obliged to notify the DOI maintaniner of the new location.
{: .challenge}

### Short history of open & linked data technologies

The concepts introduced in the above section: research objects and PIDs, are important for understanding how we can adapt the web for sharing and integrating data. We are all familiar with web-accessible databases, that is, databases that are available for searching through the web.  PubMed is one well known example. But just because a database is web accessible, doesn't mean that its data are designed for use on the web. In fact, data contained in dynamic databases are often considered to be part of the [hidden web](https://en.wikipedia.org/wiki/Deep_web), that is, it is not easily indexed in search engines like Google. The [Neuroscience Information Framework](http://neuinfo.org) was designed to search inside of these databases.  But there are ways to design databases so that they are more web friendly.  A major proponent of using the internet for sharing data and not simply web document is Tim Berners-Lee,

Linked data is a method of publishing structured data on the web so that it can be interlinked and queried using a formal semantic query language (https://en.wikipedia.org/wiki/Linked_data). Linked Open Data is linked data that is covered under on open source license so that it can be reused by third parties.  Linked data builds upon standard Web technologies, e.g., HTTP, RDF (Resource Description Framework) and URIs (Uniform resource identifiers).  But rather than using these technologies to share web pages, linked data extends them to share information in a way that can be read automatically by computers. The goal is to allow data from different sources to be connected and queried through a web browser.

Tim Berners-Lee coined the term [Linked Data in 2006](https://www.w3.org/DesignIssues/LinkedData.html) and laid out 4 basic principles:

1. Use URIs to name (identify) things.
1. Use HTTP URIs so that these things can be looked up (interpreted, "dereferenced").
1. Provide useful information about what a name identifies when it's looked up, using open standards such as RDF, SPARQL, etc.
1. Refer to other things using their HTTP URI-based names when publishing data on the Web.

We've introduced a few new terms here, so let's give a few explanations.

[URI](https://en.wikipedia.org/wiki/Uniform_Resource_Identifier):  A URI is a PID, i.e, a string of characters used to identify an entity. URI's have a specific syntax (that's what makes them uniform), which we will not go into here (see [Wikipedia](https://en.wikipedia.org/wiki/Uniform_Resource_Identifier)). One of the biggest points of confusion in the world of PIDs is the difference between a URI and a URL.  In fact, the terms URI and URL are often used interchangeably, but they are distinct. The easiest way to think about it is that a URL is a URI that happens to point to a resource over a network ([Wikipedia](https://en.wikipedia.org/wiki/Uniform_Resource_Identifier)).  In other words, all URLs are URIs but not all URIs are URLs. In our above examples, we could turn a local identifier into a globally unique identifier by adding a namespace before the ID, pubmed/26978244 If we add a network access protocol to that identifier, https://www.ncbi.nlm.nih.gov/pubmed/26978244, we have a URI that is also a URL. Because we are dealing here with data on the web, most of our URI examples will, in fact, be URL's in accordance with rule 2 of Linked Data above.

[RDF]((https://www.w3.org/RDF/): According to the W3C,the standards body for the web, RDF is "a standard model for data interchange on the Web. RDF has features that facilitate data merging even if the underlying schemas differ, and it specifically supports the evolution of schemas over time without requiring all the data consumers to be changed.

RDF extends the linking structure of the Web to use URIs to name the relationship between things as well as the two ends of the link (this is usually referred to as a “triple”). Using this simple model, it allows structured and semi-structured data to be mixed, exposed, and shared across different applications.

This linking structure forms a directed, labeled graph, where the edges represent the named link between two resources, represented by the graph nodes. This graph view is the easiest possible mental model for RDF and is often used in easy-to-understand visual explanations."

[SPARQL](https://en.wikipedia.org/wiki/SPARQL) is the query language that is used to query RDF databases.

**Examples**:
An RDF triple comprises a subject, predicate and object, each identified by a URI.  In a simple example, a statement such as: Kevin Bacon stars in the movie Footloose can be turned into RDF by coding the subject (Kevin Bacon), the predicate (is star of) and object (Movie:Footloose). A SPARQL query can then be formulated to Find all movies where "is star of" = Kevin Bacon.  Note that this example is highly simplified: please refer to [Wikipedia](https://en.wikipedia.org/wiki/Resource_Description_Framework) and [W3C](https://www.w3.org/RDF/) examples for actual coding examples.

Although the majority of biomedical data sources have been slow to adopt the [Open Linked Data protocol](http://lod-cloud.net/), a perusal of the Linked Open Data Cloud indicates that life sciences comprises a substantial part of the web of data.

### Benefits of linked open data with examples
The benefits of Linked Open Data are encapuslated in the description of RDF above:
* It facilitates data interchange on the web
* It facilitates data integration across sources even when schemas are different
* It supports evolution of schemas over time with minimal disruption to data consumers

What these benefits mean is that we can use the general architecture of the web to link not just web pages to each other, but objects within databases to similar objects in other databases.  Why is this important?  Currently, information about brain structures, diseases or genes is scattered across hundreds of databases. Searching NIF for [cerebellum](https://neuinfo.org/data/search?q=cerebellum&l=cerebellum#all), for example, yields over 1 million records from > 100 databases. These databases contain different types of information;  some contain information on connectivity of the cerebellum, others on gene expression.  Still others provide imaging data or measurements of the cerebellum in disease.  Currently, a search across NIF will let you see what databases contain the term "cerebellum" and will let you visit each of them.  But to integrate the information across them, e.g., find all images of cerebellum showing genes known to be implicated in Parkinson's disease requires a fair amount of work and multiple queries to multiple databases. For example, I might go to ClinVar to find a list of genes associated with Parkinson's disease, then use these genes to query NIF to find [image databases](https://neuinfo.org/data/source/nif-0000-00508-1/search?q=NR4A2&l=+NR4A2) that show expression of these genes.

With Linked Open Data (LOD), this process becomes much easier.  If each of these databases had exposed their data as LOD, it would be possible to construct the query: find all images of cerebellum showing genes known to be implicated in Parkinson's disease, so that it returned the same data in far fewer steps. Why?  Because the links between these different data sources would be explicit, so the "mash up" of results from different data sources is facilitated.

Of course, this type of integration is only possible if developers of databases for the life sciences agree to the same set of URI's for the things they refer to, in this case, concepts like "cerebellum" and "disease" and the relationships that connect them. These concepts are typically assigned URI's when they are represented in data structures called ontologies, essentially, formal models of knowledge within a domain.  If each database develops its own identifier for Parkinson's Disease, then we are in the same boat as today:  we'd have to go to each database, find their data dictionaries and extract the particular identifier.  A single set of identifiers for entities in the life sciences is one of the goals of the [OBO Foundry:  Open Biological Ontologies](http://www.obofoundry.org/).  Where it has been achieved, e.g., the Gene Ontology in genomics, cross query of databases is highly facilitated.  But for other biological domains, e.g., neuroscience, consistent use of identifiers for concepts and relationships across databases has been less successful. For this reason, life sciences has also had to maintain a lot of cross-mapping between concepts in ontologies and other controlled vocabularies.

[//]: # ( ## Exercise:  Working with Linked Data ) would be ideal if the example came from TRD2.

### Towards the FAIR principles

While LOD has had some uptake across the web, the number of databases using this protocol compared to the other technologies is still modest. But whether or not we use LOD, we do need to ensure that databases are designed specifically for the web and for reuse by humans and machines. To provide guidance for creating such databases independent of the technology used,  the FAIR principles were issued through [FORCE11](http://force11.org): the Future of Research Communications and e-Scholarship. The FAIR principles put forth characteristics that contemporary data resources, tools, vocabularies and infrastructures should exhibit to assist discovery and reuse by third-parties. [Wilkinson et al.,2016](https://www.nature.com/articles/sdata201618).  FAIR stands for:  Findable, Accessible, Interoperable and Re-usable. The definition of FAIR is provided in Table 1:

Number | Principle
--------- | -----------
**F**         | **Findable**
F1        | (meta)data are assigned a globally unique and persistent identifier
F2        | data are described with rich metadata
F3        | metadata clearly and explicitly include the identifier of the data it describes
F4        | (meta)data are registered or indexed in a searchable resource
**A**         | **Accessible**
A1        | (meta)data are retrievable by their identifier using a standardized communications protocol
A1.1      | the protocol is open, free, and universally implementable
A1.2      | the protocol allows for an authentication and authorization procedure, where necessary
A2        | metadata are accessible, even when the data are no longer available
**I**         |**Interoperable**
I1        | (meta)data use a formal, accessible, shared, and broadly applicable language for knowledge representation.
I2        |(meta)data use vocabularies that follow FAIR principles
I3        |(meta)data include qualified references to other (meta)data
**R**       | **Reusable**
R1        |meta(data) are richly described with a plurality of accurate and relevant attributes
R1.1      |(meta)data are released with a clear and accessible data usage license
R1.2      |(meta)data are associated with detailed provenance
R1.3      |(meta)data meet domain-relevant community standards

A detailed explanation of each of these is included in the [Wilkinson et al.,2016](https://www.nature.com/articles/sdata201618) article, and the Dutch Techcenter for Life Sciences has a set of excellent [tutorials](https://www.dtls.nl/fair-data/fair-principles-explained/), so we won't go into too much detail here.

## Findable
Findable comprises two major attributes: the data set be identifed by a PID, so that it can be unambiguously located by a machine and the data be described by sufficient metadata so that it an be discovered by a human. F3 connects the identifier to this rich metadata so that a human can verify that the dataset is corretly resolved.

## Accessible
Accessible provides requirements for ensuring that third parties can access the data by specifying that the PID is resolvable and that the access protocol is standard, e.g., http, and open.  The access protocol should allow for authentiation and authorization to protect sensitive data.  Finally, a critical requirement to ensure the integrity of links across the web is that the metadata persist, even if the data they describe have been removed for some reason. ideally, the page describing the metadata includes a statement about when and why the data were removed (Starr et al., 2015).

## Interoperable
Interoperable outlines requirements for ensuring that data across databases can be combined with minimal effort. Note that this principle specifically calls for the use of formal vocabularies widely used in a community that are themselves FAIR, i.e., have a persistent identifier and access protocol.

## Reusable
Reusable also emphasizes rich metadata, but in this case so that the dataset can be sufficiently understood by a human so that it can be reused appropriately. Many communities have published minimal information models that provide the minimum set of attributes required for proper interpretation of a given data set, e.g., [MIAME](http://fged.org/projects/miame/). Reusable also specifies that a data licence, preferable in a machine-readable form, accompanies the data specifying how it may be re-used, e.g., a CC-BY license specifies that the data may be re-used without restriction, but attribution of the source must accompany the reuse.

It is important to reiterate that, unlike LOD described in the previous section, the FAIR principles are not a protocol or a standard.  Rather, they are viewed as characteristics modern databases, and, indeed, any researh object, should have if they are to be useful. Along these lines, some of the original authors of the FAIR paper published a follow up paper in 2017 [Mons et al., 2017](http://content.iospress.com/articles/information-services-and-use/isu824), outlining what the FAIR principles are not.  FAIR is not:
* A standard
* Equivalent to RDF, Linked Data, or the Semantic Web
* Equivalent to open

The Linked Data protocol can be fully FAIR, if implemented properly, but as the authors discuss, these technologies may not be optimal for representing certain types of data. The authors also explicitly state that FAIR data need not be open data, although it is hard to see how data can be maximally reusable if they are not.  But even the most ardent open advocates recognize that all data may not be openly shared, particularly in the case where sharing would cause potential harm to either the research subjects or the researcher. Because FAIR is aspirational and flexible, it has enjoyed wide endorsement by the US National Institutes of Health, the G20, ELIXIR and H2020.

> ## Exercise (click on the arrow to the right to open)
>  At the current time, the best way to ensure that your data are FAIR is to deposit them in a database that observes the FAIR principles.  How do you know if a repository observes FAIR?  In this exercise, you will visit some repositories and mark them against the principles above to create a FAIR scorecard. To create your scorecard, create an Excel spreadsheet with the FAIR principles listed above in each row and list each repository as a column.
>
>  1. [NITRC-IR](http://www.nitrc.org/ir/)
>  1. [OpenfMRI](https://openfmri.org/)
>  1. [UniProt](http://www.uniprot.org/)
>  1. [DataVerse](https://dataverse.harvard.edu/)
>  1. A repository of your choosing
{: .challenge}
