---
templateKey: blog-post
tags: ['blog', ]
title: How I deploy my blog in 2022 | https://waylonwalker.com/how-i-deploy-2022
title: https://waylonwalker.com/how-i-deploy-2022
date: 2021-10-29
status: draft
author: '@_waylonwalker'
styles:
    margin:
        bottom: 0
        left: 0
        right: 0
        top: 0
    padding:
        bottom: 0
        left: 10
        right: 10
        top: 0
    headings:
        '1':
            bg: default
            fg: '#ff66c4,bold,italics'
            prefix: ' ⇁ '
            suffix: ' ↽ '
    quote:
        side: '│'
        style:
            bg: default
            fg: '#aaa'
        top_corner: '╭'
        bottom_corner: '╰'
    title:
        bg: default
        fg: '#e1af66,bold,italics'
        fg: '#e1af66'
    author:
        bg: default
        fg: '#ff66c4,bold,italics'
        fg: '#368ce2'
    date:
        bg: default
        fg: '#ff66c4,bold,italics'
        fg: '#368ce2,bold,italics'
        fg: '#368ce2'
    slides:
        bg: default
        fg: '#ff66c4,bold,italics'
        fg: '#368ce2,bold,italics'
        fg: '#368ce2'

---

## How I Continuously Deliver Content to my Blog with Markdown, GItHub, Python, and netlify

Content at the speed of thought.

> well, as fast as I can type

## Ask Questions in slido

Please ask questions in slido # 983 911 | App Dev 1 Track

## Slido Poll

Do **you** have a personal blog / notes / website?

> * Yes - Static, built with python
> * Yes - I manage a server running python
> * Yes - Not python
> * No

we will circle back around in a few minutes

## I'll give away my answer

* Yes - Static, built with python

## Slack Channel: #track-1-appdev

If you are in the slack give me a 🔥🔥🔥🔥🔥🔥🔥

Let's light up slack 🔥🔥🔥🔥🔥🔥🔥

## 4 parts

* Why
* My workflow
* Under the hood
* Open Source

## Part 1 WHY

## I want to own my content

Twitter is a great networking tool, but it's rare to see anything more
than a few hours old.

## [Learn In Public](https://www.swyx.io/learn-in-public/)

I'm creating learning exhaust.

> Inspired by [swyx](https://www.swyx.io/learn-in-public/)
> https://www.swyx.io/learn-in-public/

## from swyx

> Whatever your thing is, make the thing you wish you had found when you
> were learning. Don’t judge your results by “claps” or retweets or
> stars or upvotes - just talk to yourself from 3 months ago. I keep an
> almost-daily dev blog written for no one else but me.


## Some of my Stats

* 48 Google top 10 ranking pages
* 6500 monthly clicks on google
* 12k page monthly views

## Focus on content

I could not do any of this if I was focused on Building rather than
writing.

## Focus on content

No one needs elastic search navigate your first 50 posts.

## Focus on content

No one is going to make comments.

## Write for yourself

You are your biggest audience out of the gate.

> If you continue writing others like you will find you

## Slido Check

Please ask questions in slack/slido

## Part 2 Workflow and tools

> To the meat of the talk

1. Let's start by making a post
2. then show how it works under the hood

## If you take away anything

Focus on content that you want to consume.

## My Flow

``` txt
   ┌───────┐
   │  TIL  │
   └─┬─────┘
     │
     │  ┌─────────────┐
     │  │             │
     └─►│    Posts    │
        │             │
        └─┬───────────┘
          │
          │   ┌────────────────┐
          └──►│    YouTube     │
          │   └────────────────┘
          │   ┌────────────────┐
          └──►│    Conference  │
              │    Talks       │
              └────────────────┘
```

## Let's start with a Til
_the process_

### shoutout to @[jbrancha](https://twitter.com/jbrancha)

Check out his amazing [til repo](https://github.com/jbranchaud/til)

> If you ask google very many questions about git, you will end up
> finding him on the top

## Copier

I use [copier](https://copier.readthedocs.io/en/stable/) for single file
templates.


## Copier give me a new page

``` bash
copier copy ~/.copier-templates/`ls ~/.copier-templates |\
    fzf --header $(pwd) --preview='tree ~/.copier-templates/{} |\
    lolcat'` . \
```

## nvim open my file

!TIP Once it starts getting uncomfortable to find posts, its nice to have
good shortcuts to get around.

## nvim open my file

``` bash
markata list --map path --filter 'templateKey=="til"' --sort date --reverse
```

``` vim
nnoremap geil <cmd>Telescope find_files find_command=markata,list,--map,path,--filter,templateKey=='til',--sort,date,--reverse<cr>
```

## Paste in a snippet

Often times I am working away on some sort of project, and I just need
to save a snippet for a later post.

## Write the content

Later I come back and fill in the content.

## git push

I have a vim hotkey `gic` to commit my current file, and `gpp` to push
it.

## It's nearly live

It will be live within a few minutes.

## Cross Post

I've tried to cross post to more, but it really gets overwhelming.

* Twitter
* dev.to

## Cross Post

I have a plugin to convert my markdown to a more dev.to friendly format.

## Slido Check

Let'g grab a question from slack/slido

## Part 3 How it's deployed

After being sick of long and broken builds from my javascript-based static site
generator I decided it was time to switch to a language I was far more
comfortable in.  At the time I was really interested in learning how to build
my own frameworks with pluggy, so a new static site generator was born.

## Part 3 How it's deployed

This part might be a lot of code coming quick.

* Show how it comes together
* Link to the slides


## Everything is markdown

``` python
pymdown-extensions
python-frontmatter
```

## frontmatter

All the metadata is defined in yaml frontmatter.

``` yaml
---
templateKey: blog-post
tags: ['webdev', 'meta' ]
title: How I deploy my blog in 2022
date: 2021-10-29
status: draft

---
```

## setting up extensions

markata supports pymdown-extensions.

``` python
DEFAULT_MD_EXTENSIONS = [
    "markdown.extensions.toc",
    "markdown.extensions.admonition",
    "markdown.extensions.tables",
    "markdown.extensions.md_in_html",
    "pymdownx.magiclink",
    "pymdownx.betterem",
    "pymdownx.tilde",
    "pymdownx.emoji",
    "pymdownx.tasklist",
    "pymdownx.superfences",
    "pymdownx.highlight",
    "pymdownx.inlinehilite",
    "pymdownx.keys",
    "pymdownx.saneheaders",
    "codehilite",
]
```

## setting the markdown object

``` python
self.markdown_extensions = [
    *DEFAULT_MD_EXTENSIONS,
    *markdown_extensions
]
self.md = markdown.Markdown(
    extensions=self.markdown_extensions
)
```

## Pluggy

* comes from pytest
* allows users to easily modify the framework to their liking

## Pluggy

This is what I use to create my lifecycle

* configure
* glob
* load
* pre_render
* render
* post_render
* save

## Pluggy

``` python
"""Define hook specs."""
import pluggy


hook_spec = pluggy.HookspecMarker("markata")
hook_impl = pluggy.HookimplMarker("markata")

class MarkataSpecs:
    """
    Namespace that defines all specifications for Load hooks.

    glob -> load -> render -> save
    """

    @hook_spec
    def glob(self, markata: "Markata") -> None:
        """Glob for files to load."""
        pass

    @hook_spec
    def load(self, markata: "Markata") -> None:
        """Load list of files."""
        pass

    @hook_spec
    def pre_render(self, markata: "Markata") -> None:
        """Pre render content from loaded data."""
        pass

    @hook_spec
    def render(self, markata: "Markata") -> None:
        """Render content from loaded data."""
        pass

    @hook_spec
    def post_render(self, markata: "Markata") -> None:
        """Post render content from loaded data."""
        pass

    @hook_spec
    def save(self, markata: "Markata") -> None:
        """Save content from data."""
        pass
```

``` python
self._pm = pluggy.PluginManager("markata")
self._pm.add_hookspecs(hookspec.MarkataSpecs)
self._register_hooks()
```

## Diskcache

Diskcache allows you to setup a persistent cache layer.

``` python
cache = FanoutCache(self.MARKATA_CACHE_DIR, statistics=True)
```

## make a key

To set soemthing to cache we need a unique identifier.

``` python
def make_hash(self, *keys: str) -> str:
    str_keys = [str(key) for key in keys]
    return hashlib.md5("".join(str_keys).encode("utf-8")).hexdigest()
```

## make a key

From my plugins I cache anything that the function I run touches.

* plugin code
* article content
* article frontmatter

``` python
from pathlib import Path

key = make_hash(Path(__file__).read_text(), article.content, article.metadata['title'])
```


## accessing the cache

Plugins can access the cache, add to it, and set thier own expiration interval.
Here is an example from the built in markdown rendering function.

## accessing the cache

Now that we have a cache and a key we can ask the cache for values.

``` python
html_from_cache = cache.get(key)
```

## if it's not yet been set

If the content is not yet set or has expired, you will get `None` back and need
to create the value.

``` python
html_from_cache = cache.get(key)
if html_from_cache is None:
    html = markata.md.convert(article.content)
    cache.add(key, html, expire=15 * 24 * 60)
else:
    html = html_from_cache
```

## Configuration

everything is in toml

## Markata was born

A plugins all the way doen static site generator written in python.

* 6 lifecycle methods
* 21 pre-defined plugins
* cache store
* toml based configuration

## GitHub Actions

Rendering the site inside of github actions with the cache is pretty
straightforward with these four steps.  Keying off of the configuration will
bust the cache every time we change the configuration.  You can hack a full
rebuild by changing anything inside of the configuration file.


## GitHub Actions

``` yaml

- name: Cache
uses: actions/cache@v2
with:
    path: .markata.cache
    key: ${{ runner.os }}-${{ hashfiles('markata.toml') }}-markata

- name: Set up Python 3.8
uses: actions/setup-python@v1
with:
    python-version: 3.8

- name: install markata
run: pip install git+https://github.com/WaylonWalker/markata.git@develop python-twitter background # checksumdir

- name: run markata
run: markata --no-rich
```

## GitHub Actions

``` python
- name: install markata
run: pip install git+https://github.com/WaylonWalker/markata.git@develop python-twitter background # checksumdir
```

I run bleeding edge, don't do that

## Netlify

I deploy to netlify but any static site host would work.

## Netlify -> Cloudflare Pages

Since Making the title I've moved to Cloudflare pages.

> Netlify is great, but I'm cheap and wanted analytics

## Results

markata.dev

Markdown to site, with seo, cover images, full works.

* seo/og tags
* cover images
* frontmatter cleansing
* feeds
* rss
* cli
* sitemap
* heading links
* build profiler


## Links

* [Learn In Public](https://www.swyx.io/learn-in-public/)
* [swyx](https://www.swyx.io/learn-in-public/)
* [jbrancha](https://twitter.com/jbrancha)
* [til repo](https://github.com/jbranchaud/til)
* [copier](https://copier.readthedocs.io/en/stable/)
