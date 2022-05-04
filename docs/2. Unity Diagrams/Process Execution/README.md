# Process Execution

`/2. Unity Diagrams/Process Execution`

* [Overview](../../README.md)
  * [1. Unity Architecture](../../1.%20Unity%20Architecture/README.md)
    * [Algorithm Development](../../1.%20Unity%20Architecture/Algorithm%20Development/README.md)
      * [Algorithm Catalog](../../1.%20Unity%20Architecture/Algorithm%20Development/Algorithm%20Catalog/README.md)
    * [Analysis Services](../../1.%20Unity%20Architecture/Analysis%20Services/README.md)
    * [Common Services](../../1.%20Unity%20Architecture/Common%20Services/README.md)
    * [Data Services](../../1.%20Unity%20Architecture/Data%20Services/README.md)
    * [Science Processing](../../1.%20Unity%20Architecture/Science%20Processing/README.md)
  * [2. Unity Diagrams](../../2.%20Unity%20Diagrams/README.md)
    * [Algorithm Execution](../../2.%20Unity%20Diagrams/Algorithm%20Execution/README.md)
    * [**Process Execution**](../../2.%20Unity%20Diagrams/Process%20Execution/README.md)
      * [Process Deploment](../../2.%20Unity%20Diagrams/Process%20Execution/Process%20Deploment/README.md)
      * [Process Request](../../2.%20Unity%20Diagrams/Process%20Execution/Process%20Request/README.md)
      * [Process Status](../../2.%20Unity%20Diagrams/Process%20Execution/Process%20Status/README.md)
      * [Processing Response](../../2.%20Unity%20Diagrams/Process%20Execution/Processing%20Response/README.md)

---

[2. Unity Diagrams (up)](../../2.%20Unity%20Diagrams/README.md)

- [Process Deploment](../../2.%20Unity%20Diagrams/Process%20Execution/Process%20Deploment/README.md)

- [Process Request](../../2.%20Unity%20Diagrams/Process%20Execution/Process%20Request/README.md)

- [Process Status](../../2.%20Unity%20Diagrams/Process%20Execution/Process%20Status/README.md)

- [Processing Response](../../2.%20Unity%20Diagrams/Process%20Execution/Processing%20Response/README.md)

---

## Processing Deployment

The programmatic deployment of a Unity Algorithm to the Unity Processing System. The Common Workflow Language document which is part of the Algorithm Package, is used to define the inputs/outputs of the process and build the WPS-get-capabilities response.

## Processing Request

The programmatic request for processing of data using a specified algorithm. Data inputs must be queried for ahead of creating WPS request as they are a component of the request itself.

## Processing Status

Once processing is requested, the status of a job can be queried through the WPS interface.

## Processing Results

The result of a getStatus on an async completed processing request will return, by reference, a pointer to the resulting data products.
