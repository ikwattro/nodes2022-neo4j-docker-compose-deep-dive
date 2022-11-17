* An image is compose of multiple immutable layers
* A container reuses the layers of the image with an addition Read/Write thin layer of top for storing data
* When a container needs to change the image's data, it will perform a copy on write operation to the R/W thin layer
* The Neo4j image exposes two volume layers, `/data` and `/logs`