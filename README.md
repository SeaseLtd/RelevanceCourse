Solr Index for the [Gutenberg Project](https://www.gutenberg.org).

# Start up Solr

1. Download and unpack [Solr 9.5.0](https://www.apache.org/dyn/closer.lua/solr/solr/9.5.0/solr-9.5.0.tgz?action=download)
2. Run Solr pointing at the Solr Home directory for the Relevance Course

```
./bin/solr start -s /path/to/relevanceCourse/
```

In your browser, navigate to "http://localhost:8983/solr/" to confirm Solr is up and running

# Index Gutenberg Project Books

1. Verify you can open books.json - this dataset has been extracted from the Gutenberg Project by [corgis](https://think.cs.vt.edu/corgis/json/index.html)
2. Install [Python 3.12.2](https://www.python.org/downloads/) and the [pysolr library](https://github.com/django-haystack/pysolr) library - pip install pysolr
3. Run `python index.py` to index the books

# Confirm Solr has 1006 books

Navigate [here](http://localhost:8983/solr/books/select?q=*:*) and confirm you get the results.
