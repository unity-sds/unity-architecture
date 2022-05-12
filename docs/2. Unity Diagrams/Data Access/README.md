# Data Access

`/2. Unity Diagrams/Data Access`

* [Overview](../../README.md)
  * [1. Unity Architecture](../../1.%20Unity%20Architecture/README.md)
    * [Algorithm Development](../../1.%20Unity%20Architecture/Algorithm%20Development/README.md)
      * [Application Catalog](../../1.%20Unity%20Architecture/Algorithm%20Development/Application%20Catalog/README.md)
    * [Analysis Services](../../1.%20Unity%20Architecture/Analysis%20Services/README.md)
    * [Common Services](../../1.%20Unity%20Architecture/Common%20Services/README.md)
    * [Data Services](../../1.%20Unity%20Architecture/Data%20Services/README.md)
    * [Science Processing](../../1.%20Unity%20Architecture/Science%20Processing/README.md)
  * [2. Unity Diagrams](../../2.%20Unity%20Diagrams/README.md)
    * [Algorithm Execution](../../2.%20Unity%20Diagrams/Algorithm%20Execution/README.md)
    * [**Data Access**](../../2.%20Unity%20Diagrams/Data%20Access/README.md)
    * [Process Execution](../../2.%20Unity%20Diagrams/Process%20Execution/README.md)
      * [Process Deploment](../../2.%20Unity%20Diagrams/Process%20Execution/Process%20Deploment/README.md)
      * [Process Request](../../2.%20Unity%20Diagrams/Process%20Execution/Process%20Request/README.md)
      * [Process Status](../../2.%20Unity%20Diagrams/Process%20Execution/Process%20Status/README.md)
      * [Processing Response](../../2.%20Unity%20Diagrams/Process%20Execution/Processing%20Response/README.md)
  * [3. Deployment Diagrams](../../3.%20Deployment%20Diagrams/README.md)
  * [4. Unity Glossary](../../4.%20Unity%20Glossary/README.md)

---

[2. Unity Diagrams (up)](../../2.%20Unity%20Diagrams/README.md)

---


# DAPA API

The Data Access and Processing API is a way of commonly defining access and available transformations to a given data product. It is the main point of interaction for consumers of Unity data, and should be agnostic to the underlying data container (e.g. netCDF, binary, zarr).

A formal OpenAPI definition is to follow

| End Point | Result | Implementing Service Area |
| ----------- | ----------- | ----|
| {root}| the main endpoint for the Unity API | Unknown |
| {root}/collections | basic Listing and Search for collections within the Unity system | U-DS |
| {root}/collections/{collectionId} | Collection information for the given collection | U-DS |
| {root}/collections/{collectionId}/items | list of files within the collection, bbox and datetime are the most likely 'filters' to be applied. |  U-DS |
| {root}/collections/{collectionId}/variables | variable definitions for measurements and observations within the collection | U-DS |
| {root}/collections/{collectionId}/processes | DAPA Processes that can be applied to the specified collection | U-AS |
| {root}/collections/{collectionId}/processes/area:retrieve | subset data by time and space | U-AS |

Example User Stories are as follows:

<table>
    <tr>
        <td>User Story</td>
        <td colspan="3">As a user, I want to find data in the system for a given collection that covers a specific time and space and then access</td>
    </tr>
    <tr>
        <td>End Point</td>
        <td>{root}/collections/{collectionId}/items</td>
        <td>query</td>
        <td>bbox=11.49,48.05,11.66,48.22&datetime=2018-02-12T00&#58;00&#58;00Z/2018-03-18T12&#58;31&#58;12Z</td>
    </tr>
</table>

<table>
    <tr>
        <td>User Story</td>
        <td colspan="3">As a user, I want to *subset* data in the system for a given collection that covers a specific time and space</td>
    </tr>
    <tr>
        <td>End Point</td>
        <td>{root}/collections/{collectionId}/processes/area:retrieve</td>
        <td>query</td>
        <td>bbox=11.49,48.05,11.66,48.22&datetime=2018-02-12T00&#58;00&#58;00Z/2018-03-18T12&#58;31&#58;12Z</td>
    </tr>
</table>


https://docs.ogc.org/bp/20-089r1.html#toc38
