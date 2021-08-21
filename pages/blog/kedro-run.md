---
templateKey: blog-post
tags: ['kedro', 'python']
title: Running your Kedro Pipeline from the command line
date: 2021-08-24T22:40:45
status: draft

---

Running your kedro pipeline from the command line could not be any easier to
get started.  This is a concept that you may or may not do often depending on
your workflow, but its good to have under your belt.  I personally do this half
the time and run from ipytho half the time.  In production, I mostly use docker
and that is all done with this cli.


## Kedro run

To run the whole darn project all we need to do is fire up a terminal, activate
our environment, and tell kedro to run.

``` bash
kedro run 
```

## Specific Pipelines

Running a sub pipeline that we have created is as easy as telling kedro which
one we want to run.

``` bash
kedro run --pipeline dp
```

## Single Nodes

While developing a node or a small list of nodes in a larger pipeline its handy
to be able to run them one at a time.  Besides the use case of developing a
single node I would not reccomend leaning very heavy on running single nodes,
let the DAG do the work of figuring out which nodes to run for you.

``` bash
kedro run --pipeline dp --node create_master_table_node
kedro run --pipeline dp -n create_master_table_node
```

## Some DAG concepts

We will cover more of the benefits that we get from the graph nature of the DAG
in the future, but here is a quick peek at some things we can do.

``` bash
kedro run --pipeline dp --from-inputs preprocessed_shuttles
kedro run --pipeline dp --to-outputs preprocessed_shuttles
kedro run --pipeline dp --to-nodes create_master_table_node
```


## Multiple things

You can stack up multiple kedro dag concepts into a single run command.

```
kedro run --pipeline dp --to-nodes create_master_table_node --to-nodes preprocess_shuttles_node
```

## Related Links

[kedro run docs](https://kedro.readthedocs.io/en/latest/06_nodes_and_pipelines/04_run_a_pipeline.html)

https://waylonwalker.com/kedro-environment/

https://waylonwalker.com/kedro-new/

