# Facts

Facts are small pieces of information that form the base layer of the ChronoScio database, called the _facts layer_. Each fact is obligatorily backed up by one or several references, so that it can be verified by peers.

We distinguish three types of facts: Entites, Territories and Diplomatic Relations.

## Entities

An Entity is an abstract concept providing for two general properties:

1. Identification by name or appellation, and in particular by a preferred identifier.
2. Classification by type, allowing further refinement of the specific subclass an instance belongs to.

In [ChronoScio v1](/roadmap/v1.md), only the Political Entity subclass has been implemented.

### Political Entities

A Political Entity represents a unit with political responsibilities. Some examples of Political Entities are empire, city-state, republic, and hunter-gatherers. To see the full list of Political Entities, please refer to the database architecture at the end of the page.

[CIDOC reference](http://www.cidoc-crm.org/Entity/e48-place-name/version-6.2).

### 💡 People

[CIDOC reference](http://www.cidoc-crm.org/Entity/E21-Person/Version-6.2).

### 💡 Events

[CIDOC reference](http://www.cidoc-crm.org/Entity/E5-Event/Version-6.2).

### 💡 Other ideas

Documents, monuments, buildings etc, could all possibly be added in the future as entities. See http://www.cidoc-crm.org/Version/version-6.2 for more ideas.

## Territories

Each Entity has one or more Territories. A Territory is simply a shapefile (i.e. a shape on the map), with a start date and an end date. This shape can be a polygon (for Political Entities), or a point (for Events or People).

The start and end dates of Territories linked to the same Entity cannot overlap. Therefore, put together, the Territories show the evolution in time of this Entity. For example, a moving Person can have a series of Territories (of type point) with consecutive start and end dates, which represent his/her trajectory; a kingdom may see its borders changing with a series of polygon Territories.

[CIDOC reference](http://www.cidoc-crm.org/Entity/E94-Space-Primitive/Version-6.2).

## Diplomatic Relations

Diplomatic Relations represent links between Entities. Today, only Diplomatic Relations between Political Entities are implemented, they represent wars, alliances, and dominance between Political Entities.

See the technical implementation at the bottom of the page to learn more about all types of Diplomatic Relations.

CIDOC reference (none).

## Technical Implementation

Here is a Google Sheet describing the database architecture of the facts layer: https://docs.google.com/spreadsheets/d/1lYX3tjX7DY0fsSadBmtzd6OSG3DMXi-irEQA5H2J9eA
