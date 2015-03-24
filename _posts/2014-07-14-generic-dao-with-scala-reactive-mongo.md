---
layout: post
title: Generic DAO with Scala, MongoDB and ReactiveMongo
tags: [Scala, MongoDB]
---

Generic DAO pattern applied to the Scala language and ReactiveMongo framework! <!--more-->

The collectionName should be defined in the class that will extend the MongoDAO trait(the concrete DAO) and the BSONDocumentReader and BSONDocumentReader traits
are usually defined in the companion object along with the case class definition.

More specific queries are also defined in the concrete DAOs. In this case my model entities don't use id, but its another common method
to be inserted in the trait.

{% gist maiostri/627491f56998d85a1ed1 %}
