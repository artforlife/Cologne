# Basic Display page

## Get a single entry detail

### URL

http://www.sanskrit-lexicon.uni-koeln.de/scans/MWScan/2014/web/webtc/getword.php?key=Davala&filter=deva&noLit=off&accent=no&transLit=slp1

### Input parameters

accent	no
filter	deva
key	Davala
noLit	off
transLit	slp1

### Suggested Clean URL

http://www.sanskrit-lexicon.uni-koeln.de/entries/dictcode/word/{inputtransliteration}/{outputtransliteration}/{accent}

### Defaults

1. inputtransliteration - slp1
2. outputtransliteration - deva
3. accent - no

### Allowable values

1. inputtransliteration - slp1/deva/hk
2. outputtransliteration - slp1/deva/hk
3. accent - yes/no

### Rewrite rules

```
RewriteRule ^entries/([^/]*)/([^/]*)/([^/]*)/([^/]*)/([^/]+)$ http://www.sanskrit-lexicon.uni-koeln.de/scans/$1Scan/2014/web/webtc/getword.php?key=$2&filter=$4&noLit=off&accent=$5&transLit=$3
RewriteRule ^entries/([^/]*)/([^/]*)/([^/]*)/([^/]*)/$ http://www.sanskrit-lexicon.uni-koeln.de/scans/$1Scan/2014/web/webtc/getword.php?key=$2&filter=$4&noLit=off&accent=no&transLit=$3
RewriteRule ^entries/([^/]*)/([^/]*)/([^/]*)/([^/]*)$ http://www.sanskrit-lexicon.uni-koeln.de/scans/$1Scan/2014/web/webtc/getword.php?key=$2&filter=$4&noLit=off&accent=no&transLit=$3
RewriteRule ^entries/([^/]*)/([^/]*)/([^/]*)/$ http://www.sanskrit-lexicon.uni-koeln.de/scans/$1Scan/2014/web/webtc/getword.php?key=$2&filter=deva&noLit=off&accent=no&transLit=$3
RewriteRule ^entries/([^/]*)/([^/]*)/([^/]*)$ http://www.sanskrit-lexicon.uni-koeln.de/scans/$1Scan/2014/web/webtc/getword.php?key=$2&filter=deva&noLit=off&accent=no&transLit=$3
RewriteRule ^entries/([^/]*)/([^/]*)/$ http://www.sanskrit-lexicon.uni-koeln.de/scans/$1Scan/2014/web/webtc/getword.php?key=$2&filter=deva&noLit=off&accent=no&transLit=slp1
RewriteRule ^entries/([^/]*)/([^/]*)$ http://www.sanskrit-lexicon.uni-koeln.de/scans/$1Scan/2014/web/webtc/getword.php?key=$2&filter=deva&noLit=off&accent=no&transLit=slp1
```

### Questions

1. What is the purpose of noLit?

2. List of dictionaries still using 2013 display will have to be handled slightly differently. Their list is needed.

3. 
