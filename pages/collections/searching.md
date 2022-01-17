# Collection searching

## Overview

Internally we use Elasticsearch [query string](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-query-string-query.html). 

Here’s a quick reference.

### Field names
where "status" field contains "active"
```
status:active
```

"title" field contains "quick" or "brown". If you omit the OR operator the default operator will be used
```
title:(quick OR brown)
title:(quick brown)
```

where "author" field contains the exact phrase "john smith"
```
author:"John Smith"
```

where any of the fields "book.title", "book.content" or "book.date" contains quick or brown (note how we need to escape the "*" with a backslash
```
book.*:(quick brown)
```

where the field "title" has no value (or is missing):
```
_missing_:title
```

where the field "title" has any non-null value:
```
_exists_:title
```

### Wildcards

Wildcard searches can be run on individual terms, using "?" to replace a single character, and "*" to replace zero or more characters
qu?ck bro*

*note: wildcard queries can use an enormous amount of memory and
perform very badly*

### Grouping

Multiple terms or clauses can be grouped together with parentheses, to
form sub-queries:
```
(quick OR brown) AND fox
```

Groups can be used to target a particular field, or to boost the result of a sub-query:
```
status:(active OR pending) title:(full text search)^2
```

### Fuzziness
Search for terms that are similar to, but not exactly like the used search terms, using the "fuzzy"' operator
```
quikc~ brwn~ foks~
```

The default edit distance is 2, but an edit distance of 1 should be sufficient to catch 80% of all human misspellings.
It can be specified as

```
quikc~1
```

### Proximity searches

While a phrase query (eg "john smith") expects all of the terms in exactly the same order, a proximity query allows the specified words to be further apart or in a different order. A proximity search allows us to specify a maximum edit distance of words in a phrase:
```
fox quick"~5
```

### Ranges

Ranges can be specified for date, numeric or string fields. Inclusive ranges are specified with square brackets [min TO max] and exclusive ranges with curly brackets {min TO max}.

All days in 2012
```
date:[2012-01-01 TO 2012-12-31]
```

Numbers 1..5
```
count:[1 TO 5]
```

Tags between alpha and omega, excluding alpha and omega
```
tag:{alpha TO omega}
```

Numbers from 10 upwards
```
count:[10 TO *]
```

Dates before 2012
```
date:{* TO 2012-01-01}
```

Numbers from 1 up to but not including 5
```
count:[1 TO 5}
```

### Boolean operators
+ (this term must be present) and - (this term must not be present)
All other terms are optional
```
quick brown +fox -news
```