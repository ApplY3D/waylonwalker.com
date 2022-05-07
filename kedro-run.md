---
content: ''
cover: ''
date: 2021-08-24
datetime: 2021-08-24 00:00:00+00:00
description: 'Running your kedro pipeline from the command line could not be any easier
  to Running your kedro pipeline from the command line could not be any easier to
  https:'
long_description: Running your kedro pipeline from the command line could not be any
  easier to Running your kedro pipeline from the command line could not be any easier
  to https://youtu.be/ZmccpLy-OEI https://youtu.be/ZmccpLy-OEI https://waylonwalker.com/what-is-kedro
now: 2022-05-07 21:32:25.894248
path: pages/blog/kedro-run.md
slug: kedro-run
status: published
super_description: "Running your kedro pipeline from the command line could not be
  any easier to Running your kedro pipeline from the command line could not be any
  easier to https://youtu.be/ZmccpLy-OEI https://youtu.be/ZmccpLy-OEI https://waylonwalker.com/what-is-kedro/
  https://waylonwalker.com/what-is-kedro/ \U0001F446 Unsure what kedro is?  Check
  out this post. \U0001F446 Unsure what kedro is?  Check out this post. To run the
  whole darn project all we need to do is fire up a terminal, activate To run the
  whole darn project all we"
tags:
- kedro
- python
templateKey: blog-post
title: Running your Kedro Pipeline from the command line
today: 2022-05-07
year: 2021
---

Running your kedro pipeline from the command line could not be any easier to
get started.  This is a concept that you may or may not do often depending on
your workflow, but its good to have under your belt.  I personally do this half
the time and run from ipython half the time.  In production, I mostly use docker
and that is all done with this cli.

https://youtu.be/ZmccpLy-OEI


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


> 👆 Unsure what kedro is?  Check out this post.

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
kedro run --pipeline dp --node create_model_input_table_node
kedro run --pipeline dp -n create_model_input_table_node
```

## Some DAG concepts

We will cover more of the benefits that we get from the graph nature of the DAG
in the future, but here is a quick peek at some things we can do.

``` bash
kedro run --pipeline dp --to-outputs preprocessed_shuttles
kedro run --pipeline dp --from-inputs preprocessed_shuttles
kedro run --pipeline dp --to-nodes create_model_input_table_node
```

## Multiple things


You can stack up multiple kedro dag concepts into a single run command.
```
kedro run --pipeline dp --to-nodes create_model_input_table_node --to-nodes preprocess_shuttles_node
```

## Related Links

* [what is kedro](https://waylonwalker.com/what-is-kedro/)
* [setting up a kedro environment](https://waylonwalker.com/kedro-environment/)
* [creating a new kedro project](https://waylonwalker.com/kedro-new/)
* [kedro run docs](https://kedro.readthedocs.io/en/latest/06_nodes_and_pipelines/04_run_a_pipeline.html)