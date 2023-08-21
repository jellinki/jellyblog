---
layout: post
title: Aspirations and Motivations
subtitle: Katelyn Gelle
cover-img: /assets/img/akkalabotw.gif
thumbnail-img: /assets/img/waitingzelda.jpg
share-img: /assets/img/waitingzelda.jpg
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [test]
comments: true
---

{: .box-success}
I joined Computer Science because, even though I'm planning on majoring in biology-related fields, I feel that having at least some background in computer science is very helpful, especially in today's digital age.  
This year, I hope to be able to gain a lot more experience and knowledge in coding, since I didn't really know anything about it before. I'll keep working hard and trying new things!

<!--Here's a table:

| Number | Next number | Previous number |
| :------ |:--- | :--- |
| Five | Six | Four |
| Ten | Eleven | Nine |
| Seven | Eight | Six |
| Two | Three | One |

How about a yummy crepe?

![Crepe](https://beautifuljekyll.com/assets/img/crepe.jpg)

It can also be centered!

![Crepe](https://beautifuljekyll.com/assets/img/crepe.jpg){: .mx-auto.d-block :}

Here's a code chunk:

~~~
var foo = function(x) {
  return(x + 5);
}
foo(3)
~~~

And here is the same code with syntax highlighting:

```javascript
var foo = function(x) {
  return(x + 5);
}
foo(3)
```

And here is the same code yet again but with line numbers:

{% highlight javascript linenos %}
var foo = function(x) {
  return(x + 5);
}
foo(3)
{% endhighlight %}

## Boxes
You can add notification, warning and error boxes like this:

### Notification

{: .box-note}
**Note:** This is a notification box.

### Warning

{: .box-warning}
**Warning:** This is a warning box.

### Error

{: .box-error}
**Error:** This is an error box.

## Local URLs in project sites {#local-urls}

When hosting a *project site* on GitHub Pages (for example, `https://USERNAME.github.io/MyProject`), URLs that begin with `/` and refer to local files may not work correctly due to how the root URL (`/`) is interpreted by GitHub Pages. You can read more about it [in the FAQ](https://beautifuljekyll.com/faq/#links-in-project-page). To demonstrate the issue, the following local image will be broken **if your site is a project site:**

![Crepe](/assets/img/crepe.jpg)

If the above image is broken, then you'll need to follow the instructions [in the FAQ](https://beautifuljekyll.com/faq/#links-in-project-page). Here is proof that it can be fixed:

![Crepe]({{ '/assets/img/crepe.jpg' | relative_url }})
