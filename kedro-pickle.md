---
content: ''
cover: ''
date: 2021-01-14
datetime: 2021-01-14 00:00:00+00:00
description: 'In python data science/engineering most of our data is in the form of
  some sort In python data science/engineering most of our data is in the form of
  some sort '
long_description: In python data science/engineering most of our data is in the form
  of some sort In python data science/engineering most of our data is in the form
  of some sort These containers for data contain many convenient methods to manipulate
  table These contai
now: 2022-05-07 21:32:25.892783
path: pages/blog/kedro-pickle.md
slug: kedro-pickle
status: published
super_description: In python data science/engineering most of our data is in the form
  of some sort In python data science/engineering most of our data is in the form
  of some sort These containers for data contain many convenient methods to manipulate
  table These containers for data contain many convenient methods to manipulate table
  https://waylonwalker.com/what-is-kedro/ https://waylonwalker.com/what-is-kedro/
  unfamiliar with kedro, check out this post unfamiliar with kedro, check out this
  post There are times wh
tags:
- kedro
- python
- data
templateKey: blog-post
title: Kedro - My Data Is Not A Table
today: 2022-05-07
year: 2021
---

In python data science/engineering most of our data is in the form of some sort
of table, typically a DataFrame from a library like pandas, spark, or dask.

## DataFrames are the heart of most pipelines

These containers for data contain many convenient methods to manipulate table
like data structures.  Sometimes we leverage other data types, namely vanilla
types like lists and dicts, or even numpy data types.


  <div class="onelinelink-wrapper">
      <a class="onelinelink" href="https://waylonwalker.com/what-is-kedro/">
          <img style="float: right;" align='right' src="https://images.waylonwalker.com/what-is-kedro-og_250x140.png" alt="article cover for 
 What is Kedro
"/>
          <p><strong>
 What is Kedro
</strong></p>
      </a>
  </div>


> unfamiliar with kedro, check out this post

## Sometimes datasets are not tables

There are times when our data doesn't fit nicely into a DataFrame. Lucky for us
Kedro has pickle support out of the box.  Pickle is a way to store any python
object to disk.  Beware that pickle files coming from an unknown source can run
malicous code and are considered unsafe.  For the most part though when you
read and write your own pickle files they are a good tool to consider.

> See more about [pickle](https://docs.python.org/3/library/pickle.html) from python.org.

## Cataloging Pickle

I may have a dictionary that describes some cars.

``` python
{
  'truck-012-abc': {
    'type': 'truck'
    'sales': [12, 2, 3, 4, 8]
    'weight': 9024,
    'accesories': ['leather', 'audio-1']
}
```

In the catalog we will simply set the type as `pickle.PickleDataSet` and give
it a filepath.

``` yaml
cars:
  filepath: data/cars.pkl
  type: pickle.PickleDataSet
```

> This filepath does not have to be on the local filesystem it can be on the
> cloud thanks to how kedro utilizes fsspec for each of its datasets.

## Loading the dataset

The benefit of cataloging this dataset compared to leaving it as a
`MemoryDataSet` is that you can easily load this data back into memory for
further development or debugging without running any of the pipeline.

``` python
catalog.load('cars')
```