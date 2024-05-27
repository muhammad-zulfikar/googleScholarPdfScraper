# Google Scholar PDF Scraper

This repository contains an R script to scrape Google Scholar search results and download PDF files. The script also stores metadata about the downloaded PDFs.

## Required Libraries

To run the script, you need the following R libraries:

- `rvest`
- `httr`
- `tools`

You can install these libraries using the following commands in R:

```R
install.packages("rvest")
install.packages("httr")
install.packages("tools")
```

## Usage Example
The main function of `googleScholarPdfScraper` takes three arguments:

- `query`: The search query you want to use on Google Scholar.
- `pages`: The number of search result pages to scrape.
- `output_dir`: The directory where the PDFs and metadata will be saved.

Here's an example of how to use the script to search for PDFs related to "Hillary Clinton" and save the results to a directory named "pdf/hillary+clinton":

```R
scrape_google_scholar("hillary+clinton", 20, "pdf/hillary+clinton")
```

### Output Tree
```
pdf/
└── hillary+clinton/
    ├── pdf_metadata.csv
    ├── <safe_filename_1>.pdf
    ├── <safe_filename_2>.pdf
    ├── ...
```

- `pdf_metadata.csv`: A CSV file containing metadata for the downloaded PDFs, including the original link and the safe filename.
- `<safe_filename>.pdf`: The downloaded PDF files, named using a sanitized version of the original URL.
