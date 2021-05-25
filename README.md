 
# NEXT.js example
## Built from Fireship Youtube Channel tutorial
This app allows you to changes the image of a car baseed on the url. App runs on localhost: localhost:3000.  Route options are:
* /cars/ford
* /cars/lambo
* /cars/tesla
* /Hello



### About Next.js
 Allows you to create fast SEO ***React*** apps with zero configuration.
A tradition react app is rendered client side. Drawbacks of this is that bots cannot read them, and it is slower to load.
Next.js allows you to render the content on the server, then send a fully rendered HTML. After receiving this initial page, the client side takes over.
This provides HTML content for bots to index and, interactive content for users.

A Nextjs project has a page directory. Each JavaScript file defined here exports a react component that represents a route in the application. The file structure in pages directory mirrors the actual URLs the user will navigate to. Nextjs provide it's own router to make routing seem less.
Nextjs can provide multiple server routing strategies from a single server project.

Static generation (pre-rendering) allows you to render your pages at build time. Each page or component can implement ***getstaticprops()*** function. The component migh have to fetch data from a cloud database then return props and use the props to render HTML locally. Then upload the HTML to a storage bucked and, be cached by a CDN. Works great for any sort of app that doesn’t change often like a blog.

If the data does change often, you can implement server-side rendering. This builds the HTML page each time it's requested by the user.
You would do this with ***getServerSideProps()*** function to implement the data fetching and, server-side rendering for the component. This function runs at request time so that data is fetched each time the client requests.

Another option is incremental static regeneration, by simply adding a 'revalidate' to get static props Nextjs can re-generate a page when ever a new request comes in within a certain time interval.
 
 



To initialize a nextjs app:
- npx create-next-app [project-name]
