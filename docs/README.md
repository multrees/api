# Multrees.WebAPI Documentation

## Introduction

The documentation for the Multrees WebAPI is available from here.
Code samples and auto-generated client libraries in multiple programming
languages are also provided.

## RAML Tooling

The API is described using RAML (RESTful API Modeling Language). This lends
itself to the creation of a design-first API. Other artifacts can be generated
from the RAML including client SDKs; documentation for client developers and
even test harnesses.

Editing the RAML can be done in any editor as it is human-readable YAML but it's
easier with a specialized editor like [Atom](https://atom.io/) with the
[API Workbench](https://atom.io/packages/api-workbench) plugin.

There's also [Restlet Studio](https://restlet.com/modules/studio/) or
[APIMATIC Transfomer](https://apimatic.io/transformer) or
[API Workbench](http://apiworkbench.com/).

Producing API documentation can be done easily (even within the build process)
with tooling like [raml2html](https://github.com/raml2html/raml2html).

Install `raml2html`:

    npm i -g raml2html

Generate HTML markup for the API:

    raml2html api.raml > api.html

To produce Markdown from the RAML which could be used with the GitHub README:

    npm i -g raml2html-markdown-theme

    raml2html --theme raml2html-markdown-theme api.raml > api.md

## Publish to GitHub Project page

To publish the resulting HTML do, for example, the following:

    git add -u
    git commit -m "Updated API HTML"
    git checkout gh-pages
    git cherry-pick --no-commit <commit>
    git add index.html
    git commit -m "Updated API HTML"
    git push

Basically you are taking the latest, generated, HTML from the `master` branch's
last commit (copy the SHA1 for the `git cherry-pick` command)
over to the `gh-pages` branch. Once pushed to GitHub this will be displayed as the
GitHub Project page. The `cherry-pick` knows that the `api.html` in `master` is
the `index.html` in `gh-pages` because of an earlier rename in a previous commit.