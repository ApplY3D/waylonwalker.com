---
content: ''
cover: ''
date: 2020-05-09
datetime: 2020-05-09 00:00:00+00:00
description: run checks before running the pipeline
long_description: This is a very rough idea for a kedro package to prevent time lost
  to get partway through a pipeline run only to realize that you dont have access
  to data or resources. This is a very rough idea for a kedro package to prevent time
  lost to get partway
now: 2022-05-07 21:32:25.892329
path: pages/notes/kedro-preflight.md
slug: kedro-preflight
status: published
super_description: This is a very rough idea for a kedro package to prevent time lost
  to get partway through a pipeline run only to realize that you dont have access
  to data or resources. This is a very rough idea for a kedro package to prevent time
  lost to get partway through a pipeline run only to realize that you dont have access
  to data or resources. check that inputs exist or are of a type to skip (sql) check
  that inputs exist or are of a type to skip (sql) check that all input and output
  databases are access
tags: []
templateKey: blog-post
title: "\U0001F4DD Kedro Preflight Notes"
today: 2022-05-07
year: 2020
---

This is a very rough idea for a kedro package to prevent time lost to get partway through a pipeline run only to realize that you dont have access to data or resources.

## Must Haves

* check that inputs exist or are of a type to skip (sql)

# Good to haves
* check that all input and output databases are accessible with good credentials
* check for s3 bucket access
* check for spark install


## Implementation

``` python
@hook_spec
def before_pipeline_run(run_params, pipeline, catalog):

```

## run params
``` json
{
  "run_id": str
  "project_path": str,
  "env": str,
  "kedro_version": str,
  "tags": Optional[List[str]],
  "from_nodes": Optional[List[str]],
  "to_nodes": Optional[List[str]],
  "node_names": Optional[List[str]],
  "from_inputs": Optional[List[str]],
  "load_versions": Optional[List[str]],
  "pipeline_name": str,
  "extra_params": Optional[Dict[str, Any]]
}
```