# Multrees.WebAPI Documentation

## Contents

- [Introduction](#introduction)
- [RAML Tooling](#raml-tooling)
- [Publish to GitHub Project page](#publish-to-github-project-page)

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
easier with a specialized editor like [Atom][] with the
[API Workbench][api workbench plugin] plugin.

There's also [Restlet Studio][] or [APIMATIC Transfomer][] or [API Workbench][].

Producing API documentation can be done easily (even within the build process)
with tooling like [raml2html][].

Install `raml2html`:

    npm i -g raml2html

Generate HTML markup for the API:

    raml2html api.raml > api.html

To produce Markdown from the RAML which is used with the GitHub README:

    npm i -g raml2html-markdown-theme

    raml2html --theme raml2html-markdown-theme api.raml > README.md

[atom]: https://atom.io/ "Atom"
[api workbench plugin]: https://atom.io/packages/api-workbench "API Workbench plugin"
[restlet studio]: https://restlet.com/modules/studio/ "Restlet Studio"
[apimatic transfomer]: https://apimatic.io/transformer "APIMATIC Transfomer"
[api workbench]: http://apiworkbench.com/ "API Workbench"
[raml2html]: https://github.com/raml2html/raml2html "raml2html"

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

Remember to also update the README.md by running `raml2html` with the markdown
theme, as above ([RAML Tooling](#raml-tooling)).

## Generate Clients

Use [OAS RAML Converter](https://github.com/mulesoft/oas-raml-converter) to translate to Swagger format:

    oas-raml-converter --from RAML10 --to OAS api.raml > api-oas.json

[AutoRest](https://github.com/Azure/autorest/blob/master/docs/user/cli.md) doesn't work with this translated file but it's possible it might later:

    autorest --input-file=api-oas.json --csharp --output-folder=generated\csharp --namespace=Multrees.WebAPI

[Swagger.io](https://github.com/swagger-api/swagger-codegen#docker) can generate code, for example, this creates a Go client:

    docker run --rm -v ${PWD}:/local swaggerapi/swagger-codegen-cli generate -i https://raw.githubusercontent.com/multrees/api/master/api-oas.json -l go -o /local/generated/go
