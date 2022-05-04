# Process Execution

## Processing Deployment

The programmatic deployment of a Unity Algorithm to the Unity Processing System. The Common Workflow Language document which is part of the Algorithm Package, is used to define the inputs/outputs of the process and build the WPS-get-capabilities response.

## Processing Request

The programmatic request for processing of data using a specified algorithm. Data inputs must be queried for ahead of creating WPS request as they are a component of the request itself.

## Processing Status

Once processing is requested, the status of a job can be queried through the WPS interface.

## Processing Results

The result of a getStatus on an async completed processing request will return, by reference, a pointer to the resulting data products.
