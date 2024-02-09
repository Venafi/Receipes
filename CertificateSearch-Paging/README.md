# Venafi Certificate Search Script

This Python script demonstrates API paging using the Venafi `outagedetection/v1/certificatesearch` API. It allows you to retrieve certificates in your inventory in batches, with a default batch size of 250 certificates per request.

## Functionality

- Utilizes the Venafi `outagedetection/v1/certificatesearch` API for certificate retrieval.
- Implements paging to retrieve certificates in batches.
- Customizeable filters: This example filters certificates based on search criteria to return only "ACTIVE" certificates.
- Outputs the results into a `.csv` file in the same directory as this script.

## Prerequisites

- You need to retrieve your API key from your Venafi tenant.
- Set the API key as an OS environmental variable named `VAAS_API_KEY`.

## Note

- This script may take several minutes to run, depending on the number of certificates you are retrieving.

## Configuration

- **Line 16**: Change the URL if you are in the EMEA region.
- **Lines 42-50**: Define the search criteria for "ACTIVE" certificates. The script excludes any retired certificates from the results.
- **Lines 51-58**: Orders the results by the `certificateName` field.

## Usage

1. Ensure you have set up the prerequisites, including configuring the API key.
2. Adjust the configuration as necessary.
3. Run the script to retrieve and process certificates.

Feel free to modify the script and its configurations according to your requirements.
