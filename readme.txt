============================================
Sphider - a lightweight search engine in PHP
Version 1.2.x
By Ando Saabas          ando(a t)cs.ioc.ee
============================================

Sphider is a lightweight web spider and search engine written in PHP, using MySQL as its back end database. It is 
suitable for adding search functionality to small or medium sites (up to 10-20,000 pages). 

--------
Features
--------

1. Spidering
- Can index both static and dynamic pages. 
- Finds links in <a href=...>, <frame ...>, <area ...> and <meta ...> tags, and can also follow links given in 
javascript as strings via window.location and window.open. 
- Respects robots.txt protocol. 
- Follows server side redirections. 
- Allows spidering to be limited by depth (ie maximum number of clicks from the starting page), by (sub)domain or by 
directory. 
- Allows resuming paused spidering. 

2. Indexing
- Full text indexing. 
- Possbility to exclude common words from being indexed. 
- Option to define your custom page ranking function, which can depend on the number of times a given word occurs in the 
webpage, whether the word occurs in the domain name, path, or title of the document and also the relative "deepness" of 
the url (so that the same page in www.domain.com/ is ranked higher than in www.domain.com/dir1/dir2/foo.html) 

3. Searching
- Uses AND operator by default, if more than one query word is used, it finds pages that include all the query words. 
- Supports phrase searching. 
- Supports excluding words (by putting a '-' in front of a word, any page including the word will be omitted from the 
results). 
- Option to add and group sites into categories 
- Possibility to limit searching to a given category and its subcategories. 

4. Size and speed
- Sphider uses reguler expressions to extract links from webpages, so indexing is not particularly fast. Searching is 
quite fast, if the database size is reasonable. 
-Sphider is very small, its source code being under 70kb in size, probably making it the smallest search engine with 
such functionality out there (a pretty good indication of PHP as a rapid prototyping tool). 

5. Compatibility
It is a typical LAMP application (but of course it can also be run under Windows). Sphider was designed to be compatible 
with older versions of PHP and MySQL, it should work with at least PHP 3 and MySQL 3.23. 

6. Licence
Sphider is licenced under GNU General Public Licence. 


--------------------------------------------------------------------------------
Ando Saabas 2004 
Contact: ando (at) cs.ioc.ee