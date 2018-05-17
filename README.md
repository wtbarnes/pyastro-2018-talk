# pyastro-2018-talk
[![Build Status](https://travis-ci.org/wtbarnes/pyastro-2018-talk.svg?branch=master)](https://travis-ci.org/wtbarnes/pyastro-2018-talk)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1249002.svg)](https://doi.org/10.5281/zenodo.1249002)

Slides for my talk at the PyAstro 2018 meeting in New York City, NY

## Outline
* Introduction/Motivation
  * Two takeaways:
    * How to parse and wrangle (biggish) data in difficult formats, particularly static data, e.g. atomic data, maybe old observational data
    * Common interface for atomic data for astronomers
  * CHIANTI database
  * Explanation of name
  * Challenges of using IDL
* Parsing the Data
  * CHIANTI formats
  * Show some `head`, `tail` examples of the files, why they are difficult to parse
  * Talk about use of factory pattern
* Accessing the data
  * From ASCII to HDF5
  * Faster more organized storage
  * HDF5 like a filesystem so lends itself well to structure
* High Level API
  * Provide separation between the details of CHIANTI and the data itself
  * The user should not have to worry about how the data is stored, filetypes etc.
  * Maybe even able to write higher level functions without knowledge of underlying data storage model?
* Infrastructure challenges
  * Large data
  * Keeping data up to date
  * Remote data (h5serv, h5pyd, etc.)
  * This section will summarize much future work as well
  * A common interface to many atomic databases (see point above regarding abstracting away details of data storage)
  * Other databases: Cloudy, ADS, ...
* Conclusion

## Overall Notes
* Provide examples of Python throughout
* Show code snippets that show the API
* Discuss *some* implementation details that may be useful to others, e.g.
  * Factory patterns and use of metaclasses
  * `__add__`
  * `__repr__`
  * `__getitem__`