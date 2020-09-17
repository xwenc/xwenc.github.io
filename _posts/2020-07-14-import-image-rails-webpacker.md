---
title: Importing images with Webpacker
layout: post
tags: rails
---

```
  /** application.js **/
	require.context('../images', true)
```

```
  /**page.html.erb**/
	<img src="<%= asset_pack_path 'media/images/logo.svg' %>" />
```

refs: [https://rossta.net/blog/importing-images-with-webpacker.html](https://rossta.net/blog/importing-images-with-webpacker.html)