---
title: How to use git subtree
layout: post
tags: git
---

[https://segmentfault.com/a/1190000012002151](https://segmentfault.com/a/1190000012002151)

1.  Add parent and child branch.
2.  Add subtree dir on parent branch, using
```
git subtree add --prefix <dir name>  <repository>  <ref>
```
3. Push dir to child branch, using
```
git subtree push --prefix <dir name>  <repository>  <ref>
```
4. If conflict, using 
```
git subtree pull  --prefix <dir name>  <repository>  <ref>
```

done.