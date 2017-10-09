---
title: "Semantic Data Representations"
teaching: Self Paced
exercises: 0
questions:
- "Q1?"
objectives:
- "Objective 1"
- "Objective 2"
keypoints:
- We want to use this template to provide lesson materials in an open and useful format.

- This is in line with our overall goal of making science (including scientific training) more open.

---

### Introduction

We provided a very brief overview of some of the concepts involved in the semantic web and linked data in [Episode 01:  Web of Data](https://github.com/ReproNim/module-FAIR-data/blob/gh-pages/_episodes/01-Web-of-Data.md).  Please review this module if you need an introduction to concepts such as persistent identifiers, URI's, RDF and triples.  

Here we will focus specifically on a set of technologies collectively called the [semantic web](http://www.linkeddatatools.com/semantic-web-basics).  The concept of the [semantic web](https://en.wikipedia.org/wiki/Semantic_Web) was introduced by Tim Berners Lee to describe a web of data accessibly by machines through the web. The semantic web is often called web 3.0, "a way of linking data between systems or entities that allows for rich, self-describing interrelations of data available across the globe on the web" [Linked Data Tools](http://www.linkeddatatools.com/semantic-web-basics).

What does that mean exactly?  A more detailed and technical explanation is provided through the lessions below.  But in plain terms, the semantic web provides a protocol for publishing data on the web that allows machines to access them based on a set of relationships.  If fully realized, it allows bits of information about the same entity contained in different different databases, developed and maintained by different people, to be easily and automatically assembled without having to go through any manual mapping.  

The basis of this ability is the encoding of data as a graph rather than just a set of tables as is done in relational databases or spreadsheets, where each data point is connected to other data points through specific relationships. 

Let's say that there are two different databases in two different locations.  One has measured gene expression in different parts of the human brain while another has brain activation as a function of region and task.  

A reasonable question might be:  What brain regions express glutamate receptors and are active in memory tasks?

In order to answer this question, we would go to database 1 and ask for the set of brain regions that express glutamate receptors.  We may need to go to another source and find a list of glutamate receptors, because typically, expression is per gene and not gene category.  We would then go to database 2 and run that list of brain regions to return a list of tasks that activate them.  Finally, we would categorize each of these tasks as being a memory task or not.

Those of you who are familiar with working across multiple databases (see episode XXXXX) probably know the problems likely to be encountered (ToDO:  Could be an exercise). Even assuming that the two databases used the same terminology for brain regions (very unlikely), the query is very time consuming to do.  Note that the human has to do the integration here-there is no way to type a query into your web browser that would do the integration for you.

In the world of the semantic web (which, in truth, some say is mythical), this query could be done by typing one or two (albeit very complicated) queries into your web browser, using a query language called [SPARQL](https://en.wikipedia.org/wiki/SPARQL). How is that possible?

If both databases had used semantic web technologies to design their database, they would have included critical pieces of information that relate different aspects of the data in a way that a computer can "understand".  So in database 1, they may have statements such as:  "hippocampus" "is part of" "brain", "hippocampus" "expresses" "GRM1", "GRM1" "is a" "gene" and "GRM1" "encodes" "glutamate receptor".  Each of these statements is called a triple because it includes a subject, object and predicate.  These concepts and relationships also each have their own URI (Uniform resource identifier) as a unique and persistent identifier.  So you would be able to ask the computer for any thing that is a brain part and expresses a gene that encodes a glutamate receptor.

Similarly, database 2 might have encoded statements like "hippocampus" "is part of" "brain", "hippocampus" "is activated by" "Salthouse and Babcock Listening Span task", "Salthouse and Babcock Listening Span task" "measures" "working memory".  So you could ask for any brain region that is activated by tasks that measure working memory. These concepts and relationships also each have their own URI (Uniform resource identifier) as a unique and persistent identifier.

Now if both of these databases used the same URI's to identify their brain structures, genes and tasks, and the same sets of relationships through a common ontology, 

> #### Lessons
An excellent set of tutorials is available on the semantic web and associated technologies through [Linkeddatatools.com](http://www.linkeddatatools.com/index.php) and so we won't replicate them here. The tutorials cover:

  -  Introduction To Graph Databases - gives a brief overview of the way in which the semantic web stores data.
  -  RDF - A Quick Start - an introductory look at Resource Description Framework (RDF), the format the semantic web uses to store data in graph databases.
  -  Semantic Modeling - introduces the key aspects of describing data with meaning, or semantics - and the advantages this can offer.
  -  Introduction To RDFS & OWL - the key syntax the semantic web uses to encode semantic meaning into data.
  -  Querying Semantic Data - how to query published semantic data using SPARQL protocol - the means to harness the immense discovery capabilities of the semantic web.

> *Introduction to the semantic web and linked data 
> *RDF, SPARQL, Serialization of RDF
> *Ontologies
> *Tools for semantic alignment of data
{: .callout}

#### References
> Additional materials:
>
>   - [Linked Data Guides and Tutorials](http://linkeddata.org/guides-and-tutorials)
>   - [Linked Data: Tim Berners-Lee, 2006](https://www.w3.org/DesignIssues/LinkedData.html)
>   - [W3C RDF Primer](https://www.w3.org/TR/rdf11-concepts/)
>
> Relevant Books:
>
>   - [Tom Heath and Christian Bizer (2011) Linked Data: Evolving the Web into a Global Data Space (1st edition). Synthesis Lectures on the Semantic Web: Theory and Technology, 1:1, 1-136. Morgan & Claypool.](http://linkeddatabook.com/editions/1.0/)
{: .callout}
### RDF, SPARQL, Serialization of RDF

Lesson...

### Ontologies

Lesson...

### Tools for semantic alignment of data

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



