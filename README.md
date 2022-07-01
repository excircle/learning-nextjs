# Rendering Approaches

NextJS supports 4 rendering approaches. NextJS allows you to choose rendering types per page.

| Rendering Options | Description | Use Case |
| - | - | - |
| Static Rendering | Process for rendering static conent (such as HTML and Images)  which are assembled on build. Great for blogs, docs, corporate sites. | <ul><li>Providing same content for all users</li><li>Page rarely changes</li><li>Can redeploy when page changes are required</li></ul> |
| Incremental Static Regeneration | Allows for paginated retrieval of static content. Great for products page on a large site. | <ul><li>Too many pages to render at once</li><li>Frequent Page Changes</li></ul> |
| Server-side Rendering | Ability to convert files on the server into a fully rendered page for the client to download. Great for user account pages, or search results  | <ul><li>Different content for each user</li><li>SEO is important</li>Content shown on each load</ul> |
| Client-side Rendering | Downloads the apps JS, parses, then it renders HTML. Great for user-specific data, data shown "on-scroll."  | <ul><li>Portion of unique user content</li><li>Lazy load a portion of the page</li><li>Don't care about SEO</li></ul> |

# Appendix