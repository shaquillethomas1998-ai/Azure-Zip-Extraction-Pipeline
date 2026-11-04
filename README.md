# Cloud ZIP Extraction Pipeline — Azure Data Factory

A coursework project by Shaquille Thomas demonstrating archive extraction between Azure Blob Storage containers.

## Purpose

Extract compressed source files into a separate output container while preserving their folder structure.

## Tools

Azure Data Factory · Azure Blob Storage

## Pipeline Configuration

- **Pipeline:** Copydata
- **Activity:** Copy Data
- **Source dataset:** ds_zip_source
- **Source location:** landing/ADF_ABE_Data.zip
- **Source compression:** ZipDeflate (.zip)
- **Destination dataset:** ds_unzip_output
- **Destination container:** output
- **Destination compression:** None
- **Copy behavior:** Preserve hierarchy
- **Preserve ZIP filename as folder:** Enabled

Both datasets use the AzureBlobStorage1 linked service.

## Output

The destination folder contains:

- data_customers.csv
- data_orders.csv
- data_products.csv
- readme.txt

The extracted files are visible under:
output/ADF_ABE_Data.zip/ADF_ABE_Data/

## Project Evidence

The three screenshots document:

1. Source file and ZIP compression configuration.
2. Copy Data activity and destination settings.
3. Extracted files in the output container.

## Skills Demonstrated

- Configuring Azure Data Factory datasets and linked services.
- Building a cloud file-copy pipeline.
- Configuring ZIP decompression.
- Preserving folder hierarchy during extraction.
- Inspecting destination files.

## Scope and Limitations

This repository documents the configured pipeline and observed output files. It does not currently include a deployable pipeline export or run-history logs.

The workflow performs file extraction and copying. It does not clean CSV records, transform their contents or demonstrate scheduled execution.
