============================================
Sphider - a lightweight search engine in PHP
Version 1.2.x
By Ando Saabas          ando(a t)cs.ioc.ee
============================================

Sphider is a lightweight web spider and search engine written in PHP, using MySQL as its back end database. It is suitable for adding search functionality to small or medium sites (up to around 100,000 pages).
--------
Features
--------

Spidering and indexing

    * Full text indexing.
    * Can index both static and dynamic pages.
    * Finds links in <a href=...>, <frame ...>, <area ...> and <meta ...> tags, and can also follow links given in javascript as strings via window.location and window.open.
    * Respects robots.txt protocol.
    * Follows server side redirections.
    * Allows spidering to be limited by depth (ie maximum number of clicks from the starting page), by (sub)domain or by directory.
    * Supports indexing of pdf and doc files (using external binaries for file conversion).
    * Allows resuming paused spidering.
    * Possbility to exclude common words from being indexed.
    * Sophisticated administrator interface 

Searching

    * Supports AND, OR and phrase searches
    * Supports excluding words (by putting a '-' in front of a word, any page including the word will be omitted from the results).
    * Option to add and group sites into categories
    * Possibility to limit searching to a given category and its subcategories.
    * "Did you mean" search suggestion on mistyped queries.
    * Context-sensitive auto-completion on search terms (la Google Suggest)
    * Word stemming for english (searching for "run" finds "running", "runs" etc) 

Size and speed

    Sphider uses regular expressions to extract links from webpages, so indexing is not particularly fast. Searching is quite fast, if the database size is reasonable. Code base is very small, probably making it the smallest search engine with such functionality out there. 

Compatibility

    Sphider is a typical LAMP application (but of course it can also be run under Windows). Sphider was designed to be compatible with older versions of PHP and MySQL, it should work with at least PHP 4 and MySQL 3.23. 
6. Licence
Sphider is licenced under GNU General Public Licence. 


--------------------------------------------------------------------------------
Ando Saabas 2006 
Contact: ando (at) cs.ioc.ee