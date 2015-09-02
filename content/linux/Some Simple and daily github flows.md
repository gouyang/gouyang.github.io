+++
date = "2015-09-02T09:56:21+08:00"
draft = true
title = "Some Simple and daily github flows"

+++

Here records some simple github workflow, all of these can be searched on github help.
Based on my personal experience so far, they looks are:
1. Syncing a fork repo from upstream
2. Send PR based on branch
3. Pull a PR to local for testing or merging.

<!--more-->

Syncing a fork
1. git remote add upstream url
2. git fetch upstream
3. git co master  // co is alias for checkout
4. git merge upsteam/master
5. git push origin master

Send PR
1. create a new branch: 

	git br new-brname

2. fetch upstream source: 

	git fetch upstream

3. merge upstream: 

	git merge upstream/master

4. push: 

	git push origin new-brname

5. compare and create pull request on github

To test or merge a PR to local
1. git fetch origin pull/ID/head:BRANCHNAME
2. git checkout BRANCHNAME

