# Routing Features

React has no built in routing so NextJS offers built-in routing.

# What Routing Features Are Offered In Next.JS 

NextJS offers the following routing features

| Route Feature | Description |
| - | - |
| File-based routes | NextJS projects come with a `pages` folder. Each page of the site gets a `page.js` file within this folder. |
| Dynamic routes | # |
| Automatic lazy loading | # |
| Internationalization support | # |
| Redirects | # |
| Middleware | # |

# File-Based Routing

Routes of a website typically follow a route convention that is very similar to how a file system on a server would work.

NextJS honors this similarity by using directories and subfiles to define routes within your app. Again, all pages for your app reside under the `pages` directory, beneath the root dir of your NextJS project.

<b>HOW TO RENDER: </b> `www.example.com/products/support`

Starting from the root directory of your NextJS application, the above URL would be defined as so:

```
pages
├── products
│   └── support.js
```

<b>HOW TO RENDER: </b> `www.example.com/products/1`</br>
<b>HOW TO RENDER: </b> `www.example.com/products/2`</br>
<b>HOW TO RENDER: </b> `www.example.com/products/3`

NextJS allows developers to create placeholder syntax in the filename itself. To render the place holders `1`,`2`,`3` in the URLs features above, you would simply add the place holder to the file name.

```
pages
├── products
│   └── [id].js
```

In the file layout above, `[id]` would represent the numbers `1`,`2`,`3` in any URL request made to your NextJS app.

# Appendix

#### How do you create templates in NextJS?

If you're interested in creating headers or footers that will render on any page, you can do so by utilzing the `_app.js` file.