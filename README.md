# **Comparing Apache Solr, Lucene, Elasticsearch servers**

 # ABSTRACT

 The paper presents a comparative analysis of the leading three platforms for developing  information retrieval syetems, Apache Solr , Lucene, Elasticsearch servers. I brefily examine otheer similar solutions , but focus on the previously mentioned solutions as they profide greater functionality with better performance. My goal was to examine three systems , including what they offeer and how they are used. After that I make a coparative analysis focusing on many aspects, from usability to working at scale.Finally I conclude which works better for our work.

 # INTRODUCTION

With the development of information communication technology more and more data is being written and stored digitally. While collecting data has become less of a problem, extracting useful information from massive volumes of digital documents has become a large issue. Relational database, which were the the previously leding solutions for data storge, aren't designed for such scale and big data searches. In order to solve this issue, a search engine needs to built that efficiently stores, indexes and searches data, so the end, users can quickly the information which they need.

The system needs to provide an easy to use, intuitive user interface, with which the user can utilize the search capabilities. The system needs to take into account not only the user’s lack of knowledge about the underlying structure of the data set, but also his\her inability to form precise queries. Another issue, related to indexing and searching in general, is that the result set for a given query will be imprecise, regardless of the quality of the query or the implementation of the search system. The previously mentioned issues can be solved by introducing a ranking system, which will sort the results for a given query by relevance.

As information retrieval has become a serious problem, 
As information retrieval has become a serious problem, many solutions have arisen over the years trying to address it. In this large set of solutions it is hard to choose the right tool without previous experience.

In the following chapter we take a look at examples
where Lucene, Solr and Elasticsearch have been utilized.This
includes comparing the differences in design, offered
functionalities, ease of use and resource consumption.

 # RELATED WORK
I examined several solutions which used Apache Solr, Apache lucene & Elasticsearch as their primary search engine. This
includes solutions produced by the scientific community
as well as several major organizations in the industry.

Atanassova and Bertin present an information retrieval system for scientific papers using Solr. Faceted search allows the user to visualize multiple categories and to filter the results according to these categories. They show a significant
improvement in the search function of their **CATH** system
when switching to Solr. **CATH**, which stands for Class,
Architecture, Topology and Homology, is a hierarchical
protein domain classification system.

Lucene was created in 1999 by Doug Cutting, better known as the creator of Apache Hadoop, and has been used both companies like AOL and LinkedIn to power search features.Apache Lucene is a high-performance, full-featured search engine library written entirely in Java. t is a technology suitable for nearly any application that requires structured search, full-text search, faceting, nearest-neighbor search across high-dimensionality vectors, spell correction or query suggestions.

Kononenko and colleagues describe thesignificant improvement in performance they got with their software analytics dashboard tool. This performance boost is solely due to switching from a traditional relational database to Elasticsearch.They Describe their use of Elasticsearch in querying graphical music documents.Elasticsearch to efficiently manage and search through the various logs their devices produce.There are organizations such as Foursquarewhich use both Solr and Elasticsearch in theirinfrastructure
In 2013 GitHub startedusing an Elasticsearch cluster which indexes code as itgets pushed to the repository.
Lucene is an open-source Java library used as a search engine. Elasticsearch is built on top of Lucene. Elasticsearch converts Lucene into a distributed system/search engine for scaling horizontally.

As thre Lucene, Solr and Elasticsearch are leading solutions for
information retrieval this paper aims to compare the three
systems. There are several articles written by experts in
the industry which compare these systems and
this paper represents a synthesis of those articles, as well
as my own experience.

 # ANALYZED SYSTEMS
Before examining Solr and Elasticsearch we take a look
at Apache Lucene which is the underlying information retrieval library for both systems. Lucene is a free, open source and independent library which has been widely recognized for its utility in the implementation of Internet search engines and local searching. The primary function of this library is indexing and searching and Lucene result ranking uses a combination of the Vector Space model and the Boolean model of information retrieval to determine how relevant a given document
is to a user’s query.

Apache Solr is an open source enterprise search server
originally written in Java. It runs as a standalone full text
search server, using Lucene for indexing and search
functionalities. The system exposes a REST-like API and
most of the interaction between the user and Solr is done
over HTTP. By sending HTTP PUT and POST requests it
is possible to send documents for storage and indexing,
while the HTTP GET request allows the user to retrieve
results based on queries. The data sent and retrieved
supports several formats, including XML, JSON and
CSV. Not only does Solr store, index and search data, it
also offers additional features, including analytics of the
indexed data. Unlike Lucene which offers indexing and
searching, but lacks the needed infrastructure to be a
standalone application, Solr is a web application which
can be deployed on any servlet container. This allows Solr
to be used as a tool by people from various professions, as
was shown in the related works section.

Similarly to Solr, Elasticsearch is also an open source
enterprise search server written in Java. It provides a
distributed full text search engine, with a REST-like web
interface and uses JSON for the document format. It
provides scalable search, has near real-time search and
supports multitenancy. A significant feature of this system
is massive distribution and high availability. Elasticsearch
allows users to start small and scale horizontally as they
grow. These clusters are resilient and will detect new or
failed nodes and reorganize data automatically, to ensure
that it stays safe and accessible. More so than Solr, this
system offers real time advanced analytics of the indexed
data. Elasticsearch can be used as a standalone system by
people of various professions.

It should be noted that Solr and ElasticSearch both systems evolved togetherand learned from another, reaching a point where they are very similar to one another.

 # COMPARATIVE ANALYSIS
Here the following comparision is only between Solr and Elasticsearch search engines.I done this comparision only by observing the images and compared them.

The main difference between these solutions derives
from their cores which significantly differ from one
another. Looking at the distributions, Solr takes more
space on the hard drive. This is primarily owed to the fact
that the standard Solr distribution includes functionality,
other than the base, which may or may not be useful to the
end user, such as Map-Reduce, a testing framework, a
web application which represents a GUI monitoring tool,
etc. Unlike Solr, Elasticsearch’s core consists of only the
base code and documentation, which is why it needs one
third of the space that Solr needs. Fig. 1 shows the
composition of the web application archives of both
systems.

![Solr and Elasticsearch](https://sematext.com/wp-content/uploads/2017/06/solr-vs-elasticsearch-trends-1.png )<br>
**Figure 1. Solr and Elasticsearch .war composition**

Elasticsearch starts from the premise that the end user
will always need the minimum functionality that Lucene
offers and not much else. By configuring the system and
using additional tools like Logstash, Kibana and Marvel,
the user can expand the basic functionality to suit his
needs. While Solr also offers a wide variety of plugins, its
core includes modules which aren’t always necessary.

A problem that both systems have, but is more evident with
Elasticsearch, is the lack of a centralized orchestration
tool, for plugin and dependency management. If the user
wants to create an Elasticsearch cluster he must manually
install Elasticsearch and all the needed plugins on each
node.

 # CONCLUSION

The paper examines three leading solutions for
information retrieval, Apache Solr , Apache lucene and Elasticsearch,presents a side by side comparison of these two systems.After researching these there bythe papers and articles on the subject we conclude thatboth systems are good choices when it comes to document indexing and searching.

Even though both teams continue to upgrade and develop new features, the fact of the matter is that Elasticsearch has a fresh, compact core, created after the various drawbacks of Solr were noticed. Solr hasn’t stood still and while many improvements were made it can be concluded that Elasticsearch will in time surpass this system. This coupled with the fact that Elasticsearch relies on one man to approve or decline changes to the system, while Solr requires that every new features goes through a more rigid protocol of evaluation means that Elasticsearch, as it stands, will have quicker and more
frequent updates.

While Elasticsearch does seem to be the go to solution
for use cases where serious analytics are needed this does
not mean Solr should be abandoned. Teams who have experience
with Solr shouldn’t switch to a new system without serious consideration, as both(solr and Elasticsearch) systems are near equal in most cases.

 # ACKNOWLEDGMENT
- Results presented in this paper are part of the research conducted within the laptop using web servises, tutorials and pdfs prepared by websites.

# REFERENCES
1. Google scholars.
2. Tutorials and explinations found in youtube videos. 
    Apache Software Foundation, Solr, http://lucene.apache.org/solr, retrieved: 20.10.2015.
3. S. Banon, Elasticsearch, https://www.elastic.co/, 
    retrieved: 20.10.2015.
4. R. Sonnek, Realtime Search: Solr vs Elasticsearch,
    http://blog.socialcast.com/realtime-search-solr-vs-elasticsearch, 
    retrieved: 20.10.2015.