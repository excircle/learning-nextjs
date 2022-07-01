# Routing Features

React has no built in routing so NextJS offers built-in routing.

# What Routing Features Are Offered In Next.JS 

NextJS offers the following routing features

| Route Feature | Description |
| - | - |
| File-based routes | NextJS projects come with a `pages` folder. Each page of the site gets a `page.js` file within this folder. |
| Dynamic routes | NextJS allows app developers to pass dynamic routes by putting route place holder data in the file name under the `pages` folder. |
| Automatic lazy loading | NextJS only loads the page that is requested by default. |
| Internationalization support | International tags and redirects can be specified in the `next.config.js` file |
| Redirects | Redirects are handled in the `next.config.js` file. |
| Middleware | Middileware code can be added to a `_middleware.js` |

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

# API Routes

If you wish, you can also take advantage of NextJS built-in API routes. Like the `pages` folder, NextJS utilizes a folder called `api` to store API route definitions.

If you are using NextJS's built-in API routes, they will become accessible once you create a coresponding API file, and call for the file at `/api` in your URL requests.

##### Example Code

```jsx
export deafault function handler(req, res) : void {
    const products = [
        {id: 1, name: "Pencil"},
        {id: 1, name: "Pen"}
    ];
    res.status(200).json(products);
}
```

<b>HOW TO RENDER: </b> `www.example.com/api/products`

Simply save the above code into a file called `products.js` underneath the directory `api`.

```
api
├── products.js
```

Visiting the above URL will return the following payload.

```json
[
    {id: 1, name: "Pencil"},
    {id: 1, name: "Pen"}
]
```

# Appendix

#### How do you create templates in NextJS?

If you're interested in creating headers or footers that will render on any page, you can do so by utilzing the `_app.js` file.