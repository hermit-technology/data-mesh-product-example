# data-mesh-product-example
An example of a possible data product descriptor that could be used to allow humans or code to interrogate and understand a data product

# Contents

The `data-mesh` directory contains a collection of data products. This could potentially be a data lake location (eg. an s3 bucket).

The `_data-index.json` file contains some domain-level information, along with a collection of all data products published for this domain / mesh.

The `cat-pictures` directory contains a sample versioned data product, comprising two versions: `v20240404-1` and `v20250528-1`, which include some column and data changes over time.

Each version has a sub-directory which includes a `_manifest.json` file that serves as a data contract for what consumers may expect, as well a `.csv` file of data. In a real world scenario this would likely be a large collection of folder-partitioned parquet files or similar.

The versioning structure here allows for parallel data publishing allowing clients to migrate to new versions on their own timeframes, and also to preserve historical data without mutating it.