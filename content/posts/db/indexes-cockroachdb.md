
---
title: "Optimize CockroachDB using Index"
date: 2023-03-07T15:15:16+07:00
tags:
  - "tech"
  - "learn"
draft: false
cover:
    #image: "https://i.ibb.co/K0HVPBd/paper-mod-profilemode.png"
    # can also paste direct link from external site
    # ex. https://i.ibb.co/K0HVPBd/paper-mod-profilemode.png
    alt: "<alt text>"
    caption: "<text>"
    relative: false # To use relative path for cover image, used in hugo Page-bundles
---
# Indexes

## How do indexes works
When you create an index, CockroachDB "indexes" the columns you specify, which creates a copy of the columns and then sorts their values (without sorting the values in the table itself).

After a column is indexed, SQL can easily filter its values using the index instead of scanning each row one-by-one. 

## Creation
Primary key -> auto index

Secondary index -> find another column

## Performance
Trade-off between read and write, read faster but write longer because we have to write the data to the index column as well 

## Index best pratices
+ Index all columns that plan to use for **sorting or filtering** data **(in WHERE clause)**

+ Use a STORING clause to store columns of data that you want returned by common queries **(SELECT)** , but that you do not plan to use in query filters **(WHERE)**.
-> The STORING clause specifies columns which are not part of the index key but should be stored in the index. This optimizes queries that retrieve those columns without filtering on them, because it prevents the need to read the primary index.