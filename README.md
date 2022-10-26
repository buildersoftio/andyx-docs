<p align="center">
  <a href="https://getdoks.org/">
    <img alt="Andy X" src="~/../static/images/T1.png" width="200">
  </a>
</p>

<h3 align="center">
  Welcome to Andy X Documentation
</h3>

<p align="center">
  Welcome to thye Buildersoft Knowledgebase Repository! This Knowledgebase was established for Buildersoft Engineers and Andy X Community members to work together to find common solutions. 
</p>

<p align="center">
Submissions and merges to this repository are distrubuted at {to add later}.
This knowledgebase is licensed under Apache 2.0. Contributors who submit to the Buildersoft Knowledgebase for Andy agree to the Buildersoft Contribution License Agreement.
</p>

## How This Site is Rendered

This site is rendered using [Hugo](https://gohugo.io/) and the [Doks theme](https://doks.netlify.app/).

To test out the site on a local system:

1. Download the entire repo.
1. Install `hugo`.
1. From the command line, run `npm install` to allocate the proper packages locally.
1. From the command line, run `git submodule update --init --recursive` to populate the Docsy theme.
1. Edit the contents of the `./content/en` directory.  To add images/pdfs/etc , those go into `./static`.
1. To view the web page locally to verify how it looks, use `hugo server` and the web page will be displayed from `./docs` as a local server on `http://localhost:1313`.