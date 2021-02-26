Utility to retrieve the location of all the Edgar filings of  a specified type filed in a specified date range. Optionally downloads the filing retrieved in full.

###### Usage

```python
df_urls = get_edgar_filing_urls(filing_type, start_date, end_date, get_clean_filing)
```

Returns a Pandas dataframe containing CIK, Company Name, Filing type, Date of filing and URL for each filing retrieved.

All inputs are optional. Defaults to N-PX filings uploaded between Jan 2018 and Jan 2019. Can optionally retrieve the html version, but time expensive.

```python
download_filings(df_urls, path_files='edgar_filings')
```

Downloads files from URLs retrieved from get_edgar_filing_urls().

###### How

Search in the Edgar Masterfile all the filings of the specified type. Gets the location and fix the URL to download.

###### To Do

Implement multi threading for html retrieval and filing download


