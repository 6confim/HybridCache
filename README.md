## Hybrid Cache 方案

随着应用开发的发展对APP性能要求越来越高，越来越多的方案出现，比如React Native，Weex等优秀的方案，在性能上有有了巨大的提升，如果想要切换成React Native或者Weex往往需要很大的成本和风险。如果项目是从头开始做起可能会比较好，但是如果现有应用迁移的话，就要面临诸如稳定性和成本的问题。当然迁移完成后对后续的成本会有大降低。在实际项目中往往嵌入Html页面或者打开一个web页面也是不能消除的，原因很简单，虽然使用React Native可以实现远程更新代码，但是面对一些更新非常频繁的页面也无济于事，在项目需求不清晰的情况下，就更难说了。所以在html页面不能完全消除的情况下。需要一个相对能接受的方式来让html页面更快的渲染。    
基于此也有很多cache方案，大多数是基于http协议的，思路是跟进http header的etag 和 状态码来实现的，这种情况会有一个问题就是同一个页面在app和web都试用的情况下，就很难处理了，在web大多数情况下html页面一般是不会进行本地cache的，即使cache也是使用etag 配合 status来进行，总得来说还是要发一个http请求来检查页面是否需要重新下载的。这种方案一般情况下是没问题的，但是网络总是很难预料的即使一个空内容的请求也可能会偶尔慢一下。这种问题怎么解决的呢？    

### 面临的问题

1. 同一个页面app内部和Web上同时能够使用
2. app


### 问题

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/dshaobin/HybridCache/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
