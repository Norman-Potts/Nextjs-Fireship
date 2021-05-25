 
NEXT.js
 
 
Create fast SEO react apps with zero configuration.
A tradition react app is rendered client side. Drawbacks of this is bots cannot read them, and it is slower to load.
NEXTjs allows you to render the content on the server, then send a fully rendered html. After receiving this initial page, the client side takes over.
This provides html content for bots to index and interactive content for users.
Inside a nextjs project you have a page’s directory. Each JavaScript file defined here exports a react component that represents a route in the application. The file structure in pages directory mirrors the actual URLs the user will navigate to. Nextjs provide its own router to make routing seem less.
Nextjs can provide multiple server routing strategies from a single server project.
Static generation (pre-rendering) allows you to render your pages at build time.
Each page or component can implement get static props, it might fetch data from a cloud data base then return props and use props to render html locally, then uploaded to a storage bucked then cached by a CDN.
Works great for any sort of app that doesn’t change often like a blog.
If the data does change often, you can implement server-side rendering which builds the html page each time its requested by the user.
You would do this with getServerSideProps function to implement the data fetching and server-side rendering for the component. This function runs at request time so that data is fetched each time the client requests.
Another option is incremental static regeneration, by simply adding a 'revalidate' to get static props nextjs can re-generate a page when ever a new request comes in within a certain time interval.
 
 

npx create-next-app nextjs-fireship