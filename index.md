---
layout: default
title: Home
---

# Project Template

This is meant to be a documentation branch of a project.  I'll keep it in `~/Dropbox/ProjectDocs/projname`

## Steps to setup a the code etc

1. Make a [new repository](https://help.github.com/articles/create-a-repo) on [github](github.org)
2. fetch to local

    cd ~/
    # or whereever we are putting the repository.  
    git clone https://github.com/jklymak/newrepo.git
    cd newrepo/

3. edit a file
4. add the file

    git add newfile

5. Commit:

    git commit -a -m "My new commit"

6. Upload:

    git push origin master

## Steps to setup the doc directory

For whatever reason github makes you create a special branch 'gh-pages' of your repository for your code to live in.  This has to be somewhere else than your code directory, which I think is a bit silly.  

    cd ~/Dropbox/ProjectDocs
    git clone https://github.com/jklymak/newrepo.git
    # clone the code directory
    cd newrepo/
    git checkout --orphan gh-pages
    git rm -rf .
    # remove everything.
    rm '.gitignore'
    # now get some content for the now empty docs directoyr
    cd ~/downloads
    git clone -b gh-pages https://github.com/jklymak/projtemplate.git
    cp -r projecttemplate/* ~/Dropbox/ProjectDocs/newrepo
    cd ~/Dropbox/ProjectDocs/newrepo
    git commit -a -m "First pages commit"
    git push origin gh-pages

