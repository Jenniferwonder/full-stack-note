---
Title: NextJS.js
tags:
  - NextJS
Type: O
DateDo: 
DateDone: 
DateDue: 
DateStarted: 2022-11-29
DateModified: 2023-12-2106
status: 
mindmap-plugin: basic
aliases:
  - NextJS
---

# NextJS

## [S-NextJS](S-NextJS.md)

### [Learn Next.js | Next.js (nextjs.org)](https://nextjs.org/learn/dashboard-app)

### [Getting Started: Project Structure | Next.js (nextjs.org)](https://nextjs.org/docs/getting-started/project-structure)

## Intro

### [NextJS Features (Pros & Cons)](NextJS%20Features%20(Pros%20&%20Cons).md)

### Next.js is maintained by Vercel.
- https://vercel.com/

### You can deploy a Next.js app to any Node.js or serverless hosting
- https://nextjs.org/docs/app/building-your-application/deploying

### Supports a static export which doesn’t require a server
- https://nextjs.org/docs/pages/building-your-application/deploying/static-exports

## Project-Init ^a4cd9ea6-1377-f73f

### Try-next (Manual Installation)
- `npm install react@latest react-dom@latest next@latest`

### Automatic Installation
- `npx create-next-app@latest`
    - a Command Line Interface (CLI) tool that sets up a Next.js application for you
    - Dependencies
        - ![](Paste%20image%201701323825262image.png)
    - Time
        - 2 mins
- ✅ created a Next.js application using the starter example
    - `npx create-next-app@latest nextjs-dashboard --use-npm --example "https://github.com/vercel/next-learn/tree/main/dashboard/starter-example"`
- [How to start a React, NextJS and TailwindCSS project](How%20to%20start%20a%20React,%20NextJS%20and%20TailwindCSS%20project)

### Run the Dev Server
- `npm run dev`
- Visit `http://localhost:3000`

### Fast Refresh
- gives you instantaneous feedback on any edits you make
- https://nextjs.org/docs/architecture/fast-refresh

## Project Structure ^bbe1b04d-5201-6662

### `/app`
- Contains all the routes, components, and logic for your application, this is where you'll be mostly working from.
- `/app/lib`
    - Contains functions used in your application, such as reusable utility functions and data fetching functions.
    - ✅[Front-End Practice > 📌Placeholder Data](Front-End%20Practice#📌Placeholder%20Data)
        - `app/lib/placeholder-data.js`
        - you'll use this data to _seed_ your database (populate it with some initial data).
    - ✅[TypeScript](TypeScript.md)
        - `/app/lib/definitions.ts`
            - manually define the types that will be returned from the database
        - By using TypeScript, you can ensure you don't accidentally pass the wrong data format to your components or database
        - We're manually declaring the data types, but for better type-safety, we recommend [Prisma](https://www.prisma.io/)
            - automatically generates types based on your database schema.
        - Next.js also comes with a [TypeScript plugin](https://nextjs.org/docs/app/building-your-application/configuring/typescript#typescript-plugin) for your code editor, to help with auto-completion and type-safety.
- `/app/ui`
    - Contains all the UI components for your application, such as cards, tables, and forms. To save time, we've pre-styled these components for you.
- `page.tsx`
    - a special Next.js file that exports a React component, and it's required for the *route* to be accessible
    - It's the home page associated with the route `/`
- `layout.tsx`
    - was automatically created inside the app folder.
    - the main layout of your application.
    - can use it to add UI elements that are shared across all pages (e.g. navigation, footer, etc)

### `/public`
- Contains all the static assets for your application, such as images.

### `/scripts`
- Contains a seeding script that you'll use to populate your database in a later chapter.

### Config files
- `next.config.js`

## Styling ^506ec985-2310-ecac

### Traditional
- ✅Global CSS
    - `app/ui/global.css`
    - can use this file to add CSS rules to all the routes in your application
        - CSS reset rules
        - Site-wide styles for HTML elements like links
        - ...
    - can import `global.css` in any component in your application
    - But it's usually good practice to add it to your top-level component
        - In Next.js, this is `layout.tsx`, the [root layout](https://nextjs.org/docs/app/building-your-application/routing/pages-and-layouts#root-layout-required)
- ✅CSS modules
    - traditional CSS rules
    - keeping your styles separate from your JSX
    - [CSS Modules](https://nextjs.org/docs/basic-features/built-in-css-support) allow you to scope CSS to a component by automatically creating unique class names
        - Provide a way to make CSS classes locally scoped to components by default, reducing the risk of styling conflicts.
- Sass
    - CSS preprocessor that extends CSS with features like variables, nested rules, and mixins.
    - allows you to import `.css` and `.scss` files.

### CSS-in-JS
- ✅Tailwind
    - Although the CSS styles are shared globally, each class is singularly applied to each element.
        - if you add or delete an element, you don't have to worry about maintaining separate stylesheets, style collisions, or the size of your CSS bundle growing as your application scales.
    - Next.js will automatically install the necessary packages and configure Tailwind in your application.
    - A utility-first CSS framework that allows for rapid custom designs by composing utility classes.
- [styled-jsx](https://github.com/vercel/styled-jsx), [styled-components](https://github.com/vercel/next.js/tree/canary/examples/with-styled-components), and [emotion](https://github.com/vercel/next.js/tree/canary/examples/with-emotion)
- Embed CSS directly in your JavaScript components, enabling dynamic and scoped styling

### conditionally add class names with the `clsx` utility package.
- [`clsx`](https://www.npmjs.com/package/clsx) is a library that lets you toggle class names easily.

## Optimizing Fonts and Images ^0c94d204-0074-dd97

### Why
- Layout Shift
    - [Cumulative Layout Shift](https://web.dev/cls/)
        - a metric used by Google to evaluate the performance and user experience of a website
    - With fonts, layout shift happens when the browser initially renders text in a fallback or system font and then swaps it out for a custom font once it has loaded.

### Fonts
- 💡add custom fonts with `next/font`
- ✅Add a primary font
    - `app/ui/fonts.ts`
        - use this file to keep the fonts that will be used throughout your application
        - Import the `Inter` font from the `next/font/google` module - this will be your primary font.
        - specify what [subset](https://fonts.google.com/knowledge/glossary/subsetting) you'd like to load. In this case, `'latin'`
    - add the font to the `<body>` element in `/app/layout.tsx`
- ✅Add a secondary font
    - import a secondary font called `Lusitana` and pass it to the `<p>` element in your `/app/page.tsx` file
- [Optimizing: Fonts | Next.js (nextjs.org)](https://nextjs.org/docs/app/building-your-application/optimizing/fonts)
- [Web fonts - Learn web development | MDN (mozilla.org)](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Web_fonts)

### Images
- 💡add images with `next/image`
- ✅`<Image>` Component
    - an extension of the HTML `<img>` tag
    - automatic image optimization
        - Preventing layout shift automatically when images are loading
        - Resizing images to avoid shipping large images to devices with a smaller viewport
        - Lazy loading images by default (images load as they enter the viewport)
        - Serving images in modern formats, like [WebP](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types#webp) and [AVIF](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types#avif_image), when the browser supports it
    - It's good practice to set the `width` and `height` of your images to avoid layout shift
        - should be an aspect ratio identical to the source image
- Files inside `/public` can be referenced in your application.
- [Optimizing: Images | Next.js (nextjs.org)](https://nextjs.org/docs/app/building-your-application/optimizing/images)
- [Multimedia: Images - Learn web development | MDN (mozilla.org)](https://developer.mozilla.org/en-US/docs/Learn/Performance/Multimedia)

### How fonts and images are optimized in Next.js

## Routing ^f339dbff-264c-c315

### How to create nested layouts and pages using file-system routing.

### 💡Nested Routing
- Understand the role of folders and files when creating new route segments
    - folders are used to create nested routes
    - Each folder represents a route segment that maps to a URL segment
- can create separate UIs for each route using `layout.tsx` and `page.tsx` files

### ✅Create the `dashboard` routes/pages using file-system routing
- To create a nested route, you can nest folders inside each other and add *`page.tsx`* files inside them
    - ![](z-O-NextJS-nested-routing.png)

### ✅Create a nested layout that can be shared between multiple dashboard pages
- benefit of using *layouts* in Next.js
    - 💡Partial rendering
        - only the page components update while the layout won't re-render
        - [partial rendering](https://nextjs.org/docs/app/building-your-application/routing/linking-and-navigating#3-partial-rendering)
        - ![](z-O-NextJS-partial-rendering.png)

### ✅Understand root layout
- a [root layout](https://nextjs.org/docs/app/building-your-application/routing/pages-and-layouts#root-layout-required) and is required
- Any UI you add to the root layout will be shared across all pages in your application
- You can use the root layout to modify your `<html>` and `<body>` tags, and add *metadata*

## Optimizing Navigation/ Links ^fa165acf-36ff-c205

### Why optimize navigation
- traditionally use the `<a>` HTML element
    - ❌There's a full page refresh on each page navigation
- How navigation works in Next.js
    - Automatic code-splitting and prefetching
        - Next.js automatically code splits your application by route segments.
            - pages become isolated
            - If a certain page throws an error, the rest of the application will still work
            - Different from a traditional React [SPA](https://developer.mozilla.org/en-US/docs/Glossary/SPA), where the browser loads all your application code on initial load
        - whenever [`<Link>`](https://nextjs.org/docs/api-reference/next/link) components appear in the browser's viewport, Next.js automatically prefetches the code for the linked route in the background
            - this is what makes the page transition near-instant
    - [Routing: Linking and Navigating | Next.js (nextjs.org)](https://nextjs.org/docs/app/building-your-application/routing/linking-and-navigating#how-routing-and-navigation-works)

### ✅`<Link>` Component
- to link between pages in your application
- allows you to do [client-side navigation](https://nextjs.org/docs/app/building-your-application/routing/linking-and-navigating#how-routing-and-navigation-works) with JavaScript
- Use
    - Import `Link` from `next/link`
    - Replace the `<a>` tag with `<Link>`

### ✅show an active link with the `usePathname()` hook
- A common UI pattern is to show an active link to indicate to the user what page they are currently on
    - To do this, you need to get the user's current path from the URL.
    - Next.js provides a hook called [`usePathname()`](https://nextjs.org/docs/app/api-reference/functions/use-pathname) that you can use to check the path and implement this pattern
- Use
    - Add React's `"use client"` directive to the top of the file
        - Since [`usePathname()`](https://nextjs.org/docs/app/api-reference/functions/use-pathname) is a hook,
    - Import `usePathname()` from `next/navigation`
- to conditionally apply class names when the link is active
    - use the `clsx` library

        -
          ```jsx
          className={clsx(
                        'flex h-[48px] grow items-center justify-center gap-2 rounded-md bg-gray-50 p-3 text-sm font-medium hover:bg-sky-100 hover:text-blue-600 md:flex-none md:justify-start md:p-2 md:px-3',
                        {
                          'bg-sky-100 text-blue-600': pathname === link.href,
                        },
                      )}
          ```


## Deploying ^12c6e618-7039-dde4

### Set up a Vercel account and link your GitHub repo for instant previews and deployments
- Push your project to GitHub
- Visit [vercel.com/signup](https://vercel.com/signup) to create an account
- Choose the free "hobby" plan
- Select *Continue with GitHub* to connect your GitHub and Vercel accounts
- Connect and deploy your project

## Setting Up Database ^e8e304d6-5f48-7eac

### 💡Setting up a *PostgreSQL* database using `@vercel/postgres`
- PostgresSQL
    - Serverless SQL
- If you're already familiar with PostgreSQL and would prefer to use your own provider, you can skip
- Create and link your project to a Postgres database
    - [Getting Started with Vercel Postgres](https://vercel.com/docs/storage/vercel-postgres/quickstart)
- Seed the database with initial data

### Vercel Project Dashboard
- [nextjs-dashboard – Overview - Vercel](https://vercel.com/jenniferwonders-projects/nextjs-dashboard)

## Data Fetching ^bd53ae8e-c8db-2441

### 💡Approaches to fetching data: APIs, ORMs, SQL, etc

### ❓API Layers
- an intermediary layer between your application code and database
- Cases
    - using 3rd party services that provide an API
    - fetching data from the client, you want to have an API layer that runs on the server to avoid exposing your database secrets to the client
- In Next.js, you can create API endpoints using [Route Handlers](https://nextjs.org/docs/app/building-your-application/routing/route-handlers)

### ❓DB Queries
- to write logic to interact with your database
- For relational DB like Postgres
    - Use *SQL*
    - or an [ORM](https://vercel.com/docs/storage/vercel-postgres/using-an-orm#) like [Prisma](https://www.prisma.io/)
- ✅Fetch data with Server Components
    - Why
        - If you are using *React Server Components*, you can skip the API layer, and query your database directly without risking exposing your database secrets to the client
        - Server Components support *promises*, providing a simpler solution for asynchronous tasks like data fetching
            - can use *`async/await` syntax* without reaching out for `useEffect`, `useState` or data fetching libraries
        - execute on the server, so you can keep expensive data fetches and logic on the server and only send the result to the client
        - can query the database directly without an additional API layer
- ✅Fetch data using SQL
    - [Vercel Postgres SDK](https://vercel.com/docs/storage/vercel-postgres/sdk)
        - provides protection against [SQL injections](https://vercel.com/docs/storage/vercel-postgres/sdk#preventing-sql-injections)
    - Why
        - When creating your API endpoints, you need to write logic to interact with your database
        - SQL is the industry standard for querying relational databases (e.g. ORMs generate SQL under the hood)
        - SQL is versatile, allowing you to fetch and manipulate specific data
    - Go to `/app/lib/data.ts`
        - importing the [`sql`](https://vercel.com/docs/storage/vercel-postgres/sdk#sql) function from `@vercel/postgres`
            - This function allows you to query your database
        - You can call `sql` inside any Server Component
        - we've kept all the data queries in the `data.ts` file, and you can import them into the components

### Network/ Request waterfalls
- ❌The data requests are unintentionally blocking each other, creating a *request waterfall*
- A "waterfall" refers to a sequence of network requests that depend on the completion of previous requests.
    - ![](z-O-NextJS-waterfall-request.png)

### Parallel data fetching using a JavaScript Pattern
- In JavaScript, you can use the [`Promise.all()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/all) or [`Promise.allSettled()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/allSettled) functions to initiate all promises at the same time
    - Eg.
        - in `data.ts`, we're using `Promise.all()` in the `fetchCardData()` function
- Merits
    - Start executing all data fetches at the same time, which can lead to performance gains
    - Use a native JavaScript pattern that can be applied to any library or framework
- ❌Downside
    - what happens if one data request is slower than all the others

## Rendering ^81b42cce-c8f9-d5a3

### [NextJS Rendering Methods](NextJS%20Rendering%20Methods.md)

### Static Rendering
- What
    - ❌By default, Next.js *prerenders* routes to improve performance, this is called *Static Rendering*
        - if your data changes, it won't be reflected in your dashboard
    - Data fetching and rendering happens on the server at build time (when you deploy) or during [revalidation](https://nextjs.org/docs/app/building-your-application/data-fetching/fetching-caching-and-revalidating#revalidating-data)
    - The result can then be distributed and cached in a [Content Delivery Network (CDN)](https://nextjs.org/docs/app/building-your-application/rendering/server-components#static-rendering-default)
- Why
    - Faster website
    - Reduced server load
    - SEO
- Case
    - For
        - useful for UI with no data or data that is shared across users, such as a static blog post or a product page

### Dynamic Rendering
- What
    - content is rendered on the server for each user at *request time* (when the user visits the page)
- When to use
    - Real-Time Data
        - ideal for applications where data changes often
    - User-Specific Content
        - personalized content, such as dashboards or user profiles, and update the data based on user interaction
    - Request Time Information
        - to access information that can only be known at request time, such as cookies or the URL search parameters
- ✅Approaches to make your dashboard dynamic
    - By default, `@vercel/postgres` doesn't set its own caching semantics
    - ✅can use a Next.js API called `unstable_noStore` inside your Server Components or data fetching functions to opt out of static rendering
        - In your `data.ts`, import `unstable_noStore` from `next/cache`, and call it the top of your data fetching functions
        - is an experimental API and may change in the future
    - to use a stable API in your own projects, you can also use the [Segment Config Option](https://nextjs.org/docs/app/api-reference/file-conventions/route-segment-config) `export const dynamic = "force-dynamic"`
- Simulate a slow data fetch to see what happens
    - ❌With dynamic rendering, your application is only as fast as your slowest data fetch

### Streaming
- What
    - a data transfer technique that allows you to break down a route into smaller *chunks* and *progressively* stream them from the server to the client as they become ready
        - works well with React's component model, as each component can be considered a _chunk_
        - Chunks are rendered in parallel, reducing the overall load time
    - can prevent slow data requests from blocking your whole page
        - ![](z-O-NextJS-streaming.png)
- How
    - At the page level, with the `loading.tsx` file
        - ✅In the `/app/dashboard` folder, create a new file called `loading.tsx`
            - a special Next.js file built on top of Suspense
            - allows you to create fallback UI to show as a replacement while page content loads
        - ✅Loading Skeletons
            - simplified version of the UI
            - Any UI you embed into `loading.tsx` will be embedded as part of the static file, and sent first
        - ✅Route groups
            - ❌Since `loading.tsx` is a level higher, it's also applied to child pages
            - can change this with [Route Groups](https://nextjs.org/docs/app/building-your-application/routing/route-groups)
                - Create a new folder called `/(overview)` inside the dashboard folder. Then, move your `loading.tsx` and `page.tsx` files inside the folder
            - What
                - Route groups allow you to organize files into logical groups without affecting the URL path structure
                - When you create a new folder using parentheses `()`, the name won't be included in the URL path
    - ✅For specific components, with `<Suspense>`
        - *Suspense boundaries*
            - can be more granular and stream specific components using React Suspense
            - allows you to defer rendering parts of your application until some condition is met (e.g. data is loaded)
            - can wrap your dynamic components in Suspense. Then, pass it a fallback component to show while the dynamic component loads
            - to stream only the slowest data request and immediately show the rest of the page's UI
        - Use
            - move the data fetch to the component
            - import `<Suspense>` from React, and wrap it around the component
            - can pass it a fallback skeleton component
            - update the `<RevenueChart>` component to fetch its own data
        - *Group components*
            - ❌ to wrap the `<Card>` components in Suspense. You can fetch data for each individual card, but this could lead to a _popping_ effect as the cards load in, this can be visually jarring for the user
            - can use this pattern when you want multiple components to load in at the same time
        - Decide where to put Suspense boundaries
            - How you want the user to experience the page as it streams
            - What content you want to prioritize
            - If the components rely on data fetching

### Partial Prerendering
- Experimental feature

## Search and Pagination ^8dc7564e-f96e-024a

### 💡How to implement search and pagination using URL Search Params.
- Why use URL search params
    - Bookmarkable and Shareable URLs
    - Server-Side Rendering and Initial Load
    - Analytics and Tracking
        - easier to track user behavior without requiring additional client-side logic

### ✅Capture the user's input
- `<Search>` Component ("use client", a client component, which supports event listeners and hooks)

### ✅Update the URL with search params
- ⭐`useSearchParams` (from `'next/navigation'`)
    - *Next.js client hooks* that you'll use to implement the Search functionality
    - Import the `useSearchParams` hook from `'next/navigation'`, and assign it to a variable
    - the search params for this URL `/dashboard/invoices?page=1&query=pending` would look like this: `{page: '1', query: 'pending'}`
    - `const searchParams = useSearchParams()`
- Inside `handleSearch,` create a new [`URLSearchParams`](https://developer.mozilla.org/en-US/docs/Web/API/URLSearchParams) instance using your new `searchParams` variable
    - `URLSearchParams` is a Web API that provides utility methods for manipulating the URL query parameters
    - `const params = new URLSearchParams(searchParams)`
- `usePathname`
    - for the route `/dashboard/invoices`, `usePathname` would return `'/dashboard/invoices'`
    - `const pathname = usePathname();`
- `useRouter`
    - Enables navigation between routes within client components programmatically. There are [multiple methods](https://nextjs.org/docs/app/api-reference/functions/use-router#userouter) you can use
    - ` const { replace } = useRouter()`
    - `replace( `\${pathname}?\${params.toString()}\`)`
        - As the user types into the search bar, `params.toString()` translates this input into a URL-friendly format
        - updates the URL with the user's search data
- The URL is updated without reloading the page, thanks to Next.js's client-side navigation (which you learned about in the chapter on [navigating between pages](https://nextjs.org/learn/dashboard-app/navigating-between-pages)

### ✅Keep the URL and input in sync
- pass a `defaultValue` to input by reading from `searchParams`
    - To ensure the input field is in sync with the URL and will be populated when sharing
    - `defaultValue={searchParams.get('query')?.toString()`

### ✅Update the table component to reflect the search query
- ⭐Invoices page components [accept a prop called `searchParams`](https://nextjs.org/docs/app/api-reference/file-conventions/page), so you can pass the current URL params to the `<Table>` component
- Difference
    - `useSearchParams`
        - For client component
    - `searchParams`
        - For server component

### ✅Best practice: Debouncing
- To keep things simple, we'll use a library called [`use-debounce`](https://www.npmjs.com/package/use-debounce)

### ✅Add pagination
- implement pagination using URL params
- you can fetch the data on the server, and pass it to the component as a prop

## Mutating Data ^2fa1d285-83ce-23b5

### 💡adding the ability to create, update, and delete invoices
- How to work with forms and Server Components
    - `formData` object
- Revalidate the client cache
    - `revalidatePath` API
- Create dynamic route segments
    - with specific IDs
- Optimistic updates
    - React’s `useFormStatus` hook

### React Server Actions
- What
    - allow you to run *asynchronous code* directly on the server and can be invoked from your Client or Server Components
    - eliminate the need to create API endpoints to mutate your data
    - Security
        - protecting against different types of attacks, securing your data, and ensuring *authorized access*
        - Techniques
            - POST requests
            - encrypted closures
            - strict input checks
            - error message hashing
            - host restrictions
    - Use forms with Server Actions
        - In React, you can use the `action` attribute in the `<form>` element to invoke actions
        - The action will automatically receive the native [FormData](https://developer.mozilla.org/en-US/docs/Web/API/FormData) object, containing the captured data
            - ![](z-O-NextJS-server-actions.png)
        - ⚡Benefit
            - progressive enhancement - forms work even if JavaScript is disabled on the client
        - ⚡Server Actions integrated with Next.js [caching](https://nextjs.org/docs/app/building-your-application/caching)
            - can use the action to mutate data
            - can revalidate the associated cache using APIs like `revalidatePath` and `revalidateTag`
- Reference
    - [How to Think About Security in Next.js | Next.js (nextjs.org)](https://nextjs.org/blog/security-nextjs-server-components-actions)

### Create a new invoice
- ✅Create a form to capture the user's input
    - Create a new route and form
        - `/invoices/crete/page.tsx`
        - Create a `<Form>` component
            - one `<select>` (dropdown) element with a list of *customers*
            - one `<input>` element for the *amount* with `type="number"`
            - two `<input>` elements for the status with type="radio"
            - one button with `type="submit"`
- ✅Create a Server Action and invoke it from the form
    - create a Server Action that is going to be called when the form is submitted
    - `lib/actions.ts`
        - `'use server'`
        - `export async function createInvoice(formData: FormData) {}`
    - `create-form.tsx`
        - `import { createInvoice } from '@/app/lib/actions';`
        - `<form action={createInvoice}>`
    - you don't need to create API endpoints manually when using Server Actions
        - In HTML, you'd pass a URL to the `action` attribute. This URL would be the destination where your form data should be submitted (usually an API endpoint)
        - in React, the `action` attribute is considered a special prop - meaning React builds on top of it to allow actions to be invoked
        - Behind the scenes, Server Actions create a `POST` API endpoint.
- ✅Inside your Server Action, extract the data from the `formData` object
    - Methods you can use
        - [FormData: append() method - Web APIs | MDN (mozilla.org)](https://developer.mozilla.org/en-US/docs/Web/API/FormData/append)

        -
          ```ts
          const rawFormData = {
              customerId: formData.get('customerId'),
              amount: formData.get('amount'),
              status: formData.get('status'),
            };
          ```

    - Tips: forms that have many fields
        - [`entries()`](https://developer.mozilla.org/en-US/docs/Web/API/FormData/entries) method with JavaScript's [`Object.fromEntries()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/entries)
            - `const rawFormData = Object.fromEntries(formData.entries())`
- ✅Validate and prepare the data to be inserted into your database
    - use [Zod](https://zod.dev/), a TypeScript-first validation library
    - import zod
        - `import { z } from 'zod';`
    - define a schema

        -
          ```ts
          const FormSchema = z.object({
            id: z.string(),
            customerId: z.string(),
            amount: z.coerce.number(),
            status: z.enum(['pending', 'paid']),
            date: z.string(),
          });
          ```

        - `const CreateInvoice = FormSchema.omit({ id: true, date: true });`
        - The `amount` field is specifically set to coerce (change) from a string to a number while also validating its type.
    - pass your `rawFormData` to `CreateInvoice` to validate the types

        -
          ```ts
          export async function createInvoice(formData: FormData) {
            const { customerId, amount, status } = CreateInvoice.parse({
              customerId: formData.get('customerId'),
              amount: formData.get('amount'),
              status: formData.get('status'),
            });
          }
          ```

    - Store values in cents to avoid JS floating-point error
        - `const amountInCents = amount * 100;`
    - Create new dates
        - with the format "YYYY-MM-DD" for the invoice's creation date
            - `const date = new Date().toISOString().split('T')[0];`
- ✅Insert the data
    - create an SQL query to insert the new invoice into your database and pass in the variables
- handle errors
    - 📌See next chapter
- ✅Revalidate the cache and redirect the user back to invoices page
    - To revalidate
        - Why
            - Next.js has a [Client-side Router Cache](https://nextjs.org/docs/app/building-your-application/caching#router-cache) that stores the route segments in the user's browser
            - [prefetching](https://nextjs.org/docs/app/building-your-application/routing/linking-and-navigating#1-prefetching),
                - the cache ensures that users can quickly navigate between routes while reducing the number of requests made to the server
            - 💡to clear this cache and trigger a new request to the server
        - [`revalidatePath`](https://nextjs.org/docs/app/api-reference/functions/revalidatePath) function from Next.js `next/cache`
            - Once the database has been updated, the `/dashboard/invoices` path will be revalidated, and fresh data will be fetched from the server
    - to redirect the user back
        - `import { redirect } from 'next/navigation';`
        - `redirect('/dashboard/invoices');`

### Update an invoice
- 💡need to pass the invoice `id` to update the record in your database
- ✅create [Dynamic Route Segments](https://nextjs.org/docs/app/building-your-application/routing/dynamic-routes)
    - Create a new dynamic route segment with the invoice `id`
    - `invoices/[id]/edit/page.tsx`
- ✅update the `href` of the `Link` to accept the `id` prop
    - In `invoices/buttons.tsx` / `<UpdateInvoice />`
    - ``href={`/dashboard/invoices/${id}/edit`}``
- ✅Read the invoice `id` from the page `params`

    -
      ```ts
      export default async function Page({ params }: { params: { id: string } }) {
        const id = params.id;
        // ...
      }```
      
      ```

- ✅Fetch the specific invoice from your database
    - To pre-populate the form with the invoice data
    - `import { fetchInvoiceById, fetchCustomers } from '@/app/lib/data';`

    -
      ```ts
      const [invoice, customers] = await Promise.all([
          fetchInvoiceById(id),
          fetchCustomers(),
        ]);
      ```

    - The URL should also be updated with an `id` as follows: `http://localhost:3000/dashboard/invoice/uuid/edit`
    - 📌UUIDs vs. Auto-incrementing Keys
        - UUIDs eliminate the risk of ID collision, are globally unique, and reduce the risk of enumeration attacks - making them ideal for large databases
        - if you prefer cleaner URLs, you might prefer to use auto-incrementing keys
- ✅Update the invoice data in your database
    - to pass the `id` to the Server Action so you can update the right record in your database
    - can pass `id` to the Server Action using JS `bind`
        - will ensure that any values passed to the Server Action are encoded
    - in your `actions.ts` file, create a new action, `updateInvoice`

### Delete an invoice
- wrap the delete button in a `<form>` element and pass the `id` to the Server Action using `bind`
    - In `invoices/buttons.tsx` / `<DeleteInvoice />`
    - `const deleteInvoiceWithId = deleteInvoice.bind(null, id);`
    - ` <form action={deleteInvoiceWithId}> </form>`
- In `actions.ts`

    -
      ```ts
      export async function deleteInvoice(id: string) {
        await sql`DELETE FROM invoices WHERE id = ${id}`;
        revalidatePath('/dashboard/invoices');
      }
      ```

- Since this action is being called in the `/dashboard/invoices` path, you don't need to call `redirect`
    - Calling `revalidatePath` will trigger a new server request and re-render the table

## Error Handling ^146f5df6-042e-9e6f

### 💡How to handle general and `404` not found errors.
- use the special `error.tsx` file to catch errors in your route segments, and show a fallback UI to the user
- use the `notFound` function and `not-found` file to handle 404 errors (for resources that don’t exist)

### ✅Add `try-catch` to Server Actions
- `redirect` is being called outside of the `try/catch` block
    - because `redirect` works by throwing an error, which would be caught by the `catch` block

### ✅Next.js [`error.tsx`](https://nextjs.org/docs/app/api-reference/file-conventions/error) file
- Why ^658d7466-5ac6-9c42
    - to show errors to the user to avoid an abrupt failure and allow your application to continue running
    - can be used to define a UI boundary for a route segment
    - serves as a catch-all for unexpected errors
    - allows you to display a fallback UI to your users
- `"use client"`
    - `error.tsx` needs to be a Client Component
- accepts two props
    - `error`
        - an instance of JavaScript's native [`Error`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error) object
    - `reset`
        - a function to reset the error boundary
        - When executed, the function will try to re-render the route segment

### ✅Handle 404 errors with `notFound` function
- For example, visit a fake UUID that doesn't exist
    - visit [http://localhost:3000/dashboard/invoices/2e94d1ed-d220-449f-9f11-f0bbceed9645/edit](http://localhost:3000/dashboard/invoices/2e94d1ed-d220-449f-9f11-f0bbceed9645/edit)
- In `/dashboard/invoices/[id]/edit/page.tsx`
    - `import { notFound } from 'next/navigation';`

    -
      ```tsx
       if (!invoice) {
          notFound();
        }
      ```

    - `<Page>` will now throw an error if a specific invoice is not found
- To show an error UI to the user
    - Create a `not-found.tsx` file inside the `/edit` folder
- `notFound` will take precedence over `error.tsx`, so you can reach out for it when you want to handle more specific errors

### Reference
-
    - [Error Handling](https://nextjs.org/docs/app/building-your-application/routing/error-handling)
-
    - [`error.js` API Reference](https://nextjs.org/docs/app/api-reference/file-conventions/error)
-
    - [`notFound()` API Reference](https://nextjs.org/docs/app/api-reference/functions/not-found)
-
    - [`not-found.js` API Reference](https://nextjs.org/docs/app/api-reference/file-conventions/not-found)

## Accessibility ^d3b95c34-f0d8-7b05

### What
- a vast topic that covers many areas, such as keyboard navigation, semantic HTML, images, colors, videos, etc
    - recommend  [Learn Accessibility](https://web.dev/learn/accessibility/) course by [web.dev](https://web.dev/)
- features available in Next.js
    - *Server-side Form Validation*
    - use `eslint-plugin-jsx-a11y` with Next.js to implement accessibility best practices
    - use the React `useFormState` hook to handle form errors, and display them to the user

### use `eslint-plugin-jsx-a11y` with Next.js to implement accessibility best practices
- to help catch accessibility issues early
    - warns if you have images without `alt` text, use the `aria-*` and `role` attributes incorrectly, and more
- ✅Add `next lint` as a script in your `package.json` file
    - `"lint": "next lint"`
    - `npm run lint`
- `next lint` runs as part of the build process
    - If you tried to deploy your application to Vercel, the warning would also show up in the build logs

### Form Accessibility
- Semantic HTML
    - ✅Using semantic elements (`<input>`, `<option>`, etc) instead of `<div>`
    - allows assistive technologies (AT) to focus on the input elements
    - provide appropriate contextual information to the user
    - making the form easier to navigate and understand
- Labelling
    - ✅Including `<label>` and the `htmlFor` attribute
        - ensures that each form field has a descriptive text label
    - improves AT support by providing context
    - enhances usability by allowing users to click on the label to focus on the corresponding input field
- Focus Outline
    - ✅fields are properly styled to show an outline when they are in focus
    - visually indicates the active element on the page
    - helping both keyboard and screen reader users to understand where they are on the form
- ❌However, they don't address *form validation* and *errors*

### Form Validation
- To prevent sending unexpected data to the server
- Client-Side validation
    - form validation provided by the browser by adding the `required` attribute to the `<input>` and `<select>` elements in your forms
- Server-Side validation
    - Why
        - Ensure your data is in the expected format before sending it to your database
        - Reduce the risk of malicious users bypassing client-side validation
        - Have one source of truth for what is considered _valid_ data
    - ✅import the `useFormState` hook from `react-dom`
        - In your `create-form.tsx`
        - Returns two values: `[state, dispatch]` \- the form state, and a dispatch function (similar to [useReducer](https://react.dev/reference/react/useReducer))

        -
          ```tsx
          const initialState = { message: null, errors: {} };
          const [state, dispatch] = useFormState(createInvoice, initialState);
          
          return <form action={dispatch}>...</form>;
          ```

    - ✅use Zod to validate form data
        - In your `action.ts`
        - change the Zod `parse()` function to `safeParse()`
            - `safeParse()` will return an object containing either a `success` or `error` field
            - will help handle validation more gracefully without having put this logic inside the `try/catch` block
        - If `validatedFields` isn't successful, we return the function early with the error messages from Zod.

            -
              ```ts
              if (!validatedFields.success) {
                  return {
                    errors: validatedFields.error.flatten().fieldErrors,
                    message: 'Missing Fields. Failed to Create Invoice.',
                  };
                }
              ```

        - console.log `validatedFields` and submit an empty form to see the shape of it
    - ✅display the errors in your form component
        - In your `create-form.tsx: <select>`
            - `aria-describedby="customer-error"`
            - establishes a relationship between the `select` element and the error message container
            - indicates that the container with `id="customer-error"` describes the `select` element
            - Screen readers will read this description when the user interacts with the `select` box to notify them of errors

        -
          ```tsx
          <div id="customer-error" aria-live="polite" aria-atomic="true">
              {state.errors?.customerId &&
                state.errors.customerId.map((error: string) => (
                      <p className="mt-2 text-sm text-red-500" key={error}>
                        {error}
                      </p>
               ))}
          </div>
          ```

        - You can console.log `state` inside your component and check if everything is wired correctly
        - The screen reader should politely notify the user when the error inside the `div` is updated
            - When the content changes (e.g. when a user corrects an error), the screen reader will announce these changes, but only when the user is idle so as not to interrupt them
    - run `npm run lint` to check if you're using the aria labels correctly

## 📌[Authentication](Authentication.md) ^73d022d2-4f12-e67c

### 💡How to add authentication to your application using [`NextAuth.js`](https://next-auth.js.org/) and Middleware.

### Intro
- Ways to check identity
    - 2-factor authentication (2FA)
        - send a verification code to your device or use an external app like Google Authenticator
- Authentication
    - proving your identity with something you have like a username and password
    - checks who you are
- Authorization
    - decides what parts of the application they are allowed to use
    - determines what you can do or access in the application

### Create the login route
- creating a new route in your application called `/login`

### 📌 [NextAuth.js](https://nextjs.authjs.dev/) ^2b01d5fc-daa3-694b
- abstracts away much of the complexity involved in managing *sessions, sign-in and sign-out*, and other aspects of authentication
- Set up
    - `npm install next-auth@beta`
    - `openssl rand -base64 32`
        - generate a secret key for your application
        - used to encrypt cookies, ensuring the security of user sessions
    - In `.env`
        - `AUTH_SECRET=your-secret-key`
        - add your generated key to the `AUTH_SECRET` variable
    - add environment variables on Vercel
        - [guide](https://vercel.com/docs/projects/environment-variables)
- Create an `auth.config.ts` file at the root of our project
    - contain the configuration options for NextAuth.js

    -
      ```ts
      import type { NextAuthConfig } from 'next-auth';
      
      
      export const authConfig = {
        pages: {
          signIn: '/login',
        },
      };
      ```

    - can use the `pages` option to specify the route for custom sign-in, sign-out, and error pages
        - not required
        - but by adding `signIn: '/login'` into our `pages` option, user will be redirected to our custom login page, rather than the NextAuth.js default page
    - `authorized` callback is used to verify if the request is authorized to access a page
        - called before a request is completed
        - receives an object with the `auth` and `request` properties
            - The `auth` property contains the user's session
            - the `request` property contains the incoming request
    - `providers` option is an array where you list different login options.
        - For now, it's an empty array to satisfy NextAuth config.
        - [Learn Next.js: Adding Authentication | Next.js (nextjs.org)](https://nextjs.org/learn/dashboard-app/adding-authentication#adding-the-credentials-provider)
- Protect routes with [Next.js Middleware](https://nextjs.org/docs/app/building-your-application/routing/middleware)
    - Why
        - 💡prevent users from accessing the dashboard pages unless they are logged in
        - the protected routes will not even start rendering until the Middleware verifies the authentication
    - In the root of your project, create a file called `middleware.ts`
        - import the `authConfig` object into a Middleware file
        - initializing NextAuth.js with the `authConfig` object
        - exporting the `auth` property

        -
          ```ts
          import NextAuth from 'next-auth';
          import { authConfig } from './auth.config';
          export default NextAuth(authConfig).auth;
          ```

        - using the `matcher` option from Middleware to specify that it should run on specific paths

            -
              ```ts
              export const config = {
                matcher: ['/((?!api|_next/static|_next/image|.*\\.png$).*)'],
              };
              ```

- Password Hashing
    - hash passwords before storing them in a database
        - converts a password into a fixed-length string of characters
        - appears random, providing a layer of security even if the user's data is exposed
    - `bcrypt` package in `seed.js`
        - to compare that the password entered by the user matches the one in the database
    - Create a new file called `auth.ts`
        - Why
            - need to create a separate file for the `bcrypt` package
            - because `bcrypt` relies on Node.js APIs not available in Next.js Middleware
        - spreads your `authConfig` object

            -
              ```ts
              import NextAuth from 'next-auth';
              import { authConfig } from './auth.config';
              
              
              export const { auth, signIn, signOut } = NextAuth({
                ...authConfig,
              });
              ```

        - Add the Credentials provider
            - `providers` is an array where you list different login options such as Google or GitHub
            - For this course, we will focus on using the [Credentials provider](https://authjs.dev/getting-started/providers/credentials-tutorial) only.
                - allows users to log in with a username and a password
            - ⚡recommended to use alternative providers such as [OAuth](https://authjs.dev/getting-started/providers/oauth-tutorial) or [email](https://authjs.dev/getting-started/providers/email-tutorial) providers
                - See the [NextAuth.js docs](https://authjs.dev/getting-started/providers) for a full list of options
        - Add the sign in functionality
            - use the `authorize` function to handle the authentication logic
            - can use `zod` to validate the email and password before checking if the user exists in the database
- Update the login form
    - connect the auth logic with your login form
    - In your `actions.ts` file
    - in your `login-form.tsx` component
        - use React's `useFormState` to call the server action and handle form errors
        - use `useFormStatus` to handle the pending state of the form
- Add logout functionality
    - 💡to add the logout functionality to `<SideNav />`
    - call the `signOut` function from `auth.ts` in your `<form>` element

## Metadata ^53e648c7-712b-77f4

### How to add metadata and prepare your application for social sharing.

### What
- provides additional details about a webpage
- works behind the scenes, embedded within the page's HTML, usually within the `<head>` element

### Why
- enhancing a webpage's SEO, making it more accessible and understandable for search engines and social media platforms
- Proper metadata helps search engines effectively index webpages, improving their ranking in search results
- metadata like Open Graph improves the appearance of shared links on social media, making the content more appealing and informative for users

### Types
- Title
    - for the title of a webpage that is displayed on the browser tab
    - crucial for SEO as it helps search engines understand what the webpage is about
    - `<title>Page Title</title>`
- Description
    - provides a brief overview of the webpage content and is often displayed in search engine results
    - `<meta name="description" content="A brief description of the page content." />`
- Keyword
    - includes the keywords related to the webpage content, helping search engines index the page
    - `<meta name="keywords" content="keyword1, keyword2, keyword3" />`
- Open Graph
    - enhances the way a webpage is represented when shared on social media platforms, providing information such as the title, description, and preview image

    -
      ```html
      <meta property="og:title" content="Title Here" />
      <meta property="og:description" content="Description Here" />
      <meta property="og:image" content="image_url_here" />
      ```

- Favicon
    - links the favicon (a small icon) to the webpage, displayed in the browser's address bar or tab
    - `<link rel="icon" href="path/to/favicon.ico" />`

### Metadata API
- to define your application metadata
    - to use these files for static metadata, or you can generate them programmatically within your project
    - With both these options, Next.js will automatically generate the relevant `<head>` elements for your pages
- 2 ways
    - Config-based
        - Export a [static `metadata` object](https://nextjs.org/docs/app/api-reference/functions/generate-metadata#metadata-object) or a dynamic [`generateMetadata` function](https://nextjs.org/docs/app/api-reference/functions/generate-metadata#generatemetadata-function) in a `layout.js` or `page.js` file
    - File-based
        -
            - `favicon.ico`, `apple-icon.jpg`, and `icon.jpg`: Utilized for favicons and icons
        -
            - `opengraph-image.jpg` and `twitter-image.jpg`: Employed for social media images
        -
            - `robots.txt`: Provides instructions for search engine crawling
        -
            - `sitemap.xml`: Offers information about the website's structure
- Favicon and Open Graph Image
    - Move these images (`favicon.ico`, `opengraph-image.jpeg`) to the root of your `/app` folder
    - After doing this, Next.js will automatically identify and use these files as your favicon and OG image
    - can verify this by checking the `<head>` element of your application in dev tools
    - can also create dynamic OG images using the [`ImageResponse`](https://nextjs.org/docs/app/api-reference/functions/image-response) constructor.
- Page title and descriptions
    - can also include a [`metadata` object](https://nextjs.org/docs/app/api-reference/functions/generate-metadata#metadata-fields) from any `layout.js` or `page.js` file to add additional page information like title and description
    - Any metadata in root `layout.js` will be inherited by all pages that use it

        -
          ```tsx
          import { Metadata } from 'next';
          
          
          export const metadata: Metadata = {
            title: 'Acme Dashboard',
            description: 'The official Next.js Course Dashboard, built with App Router.',
            metadataBase: new URL('https://next-learn-dashboard.vercel.sh'),
          };
          ```

    - add a custom title for a specific page
        - adding a `metadata` object to the page itself
        - Metadata in nested pages will override the metadata in the parent
        - To avoid repetition
            - use the `title.template` field in the `metadata` object
                - to define a template for your page titles
                - can include the page title, and any other information you want to include

## Configuring ^c2531177-992d-064b

### Environment Variables
- [Basic Features: Environment Variables | Next.js](https://nextjs.org/docs/basic-features/environment-variables)

## 🐛[BugPack_NextJS](BugPack_NextJS)