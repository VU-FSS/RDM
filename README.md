# Introduction

This repository contains draft versions of the RDM pages of the Faculty of Social Sciences of the Vrije Universiteit Amsterdam. The purpose is to have an environment to quickly draft and view new or updated pages. The finished pages are published on VU.nl manually by the university's communication department.

The rendered pages were visible on `https://vu-fss.github.io/RDM` but were taken offline on 1 May 2025 to allow for further content development. The content on the pages in this repository are no longer in sync with the content on VU.nl. Please reference [these pages](https://vu.nl/en/employee/social-sciences-getting-started/ssc-starting-a-new-project) for current content.

# How to update

The faculty data steward owns the repository and can make updates. It's best to make updates first to the updates branch, and render them locally using bookdown-serve() or bookdown-render(). All updates to the main branch are published to the site using github actions using the procedure outlined 
[here](https://medium.com/@delucmat/how-to-publish-bookdown-projects-with-github-actions-on-github-pages-6e6aecc7331e).

# Folder structure

- .github: contains the information for github actions.
- _documents: folder containing documents for an old version of the website. 
- assets: contains files needed for the site
- outputs (ignored by git): folder created by bookdown-serve() or bookdown-render() for the local version of the website. It is ignored because it is entirely built off index.rmd and the files in the pages folder.
- pages: the various pages (bookdown chapters).
- presentations: a folder containing slides for previous presentations. Should probably be moved to assets.
- sample_dmps: contains sample dmps for the data organization page; could probably be moved to assets.

