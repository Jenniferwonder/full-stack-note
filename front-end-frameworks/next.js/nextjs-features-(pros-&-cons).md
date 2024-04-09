---
Title: NextJS Features (Pros & Cons)
Type: 
tags: 
DateDo: 
DateDone: 
DateDue: 
status: 
DateStarted: 2023-11-30
DateModified: 2023-12-01
mindmap-plugin: basic
---

# NextJS Features (Pros & Cons)

## Why Next.js?

### Next.js is a popular, lightweight framework for static and server‑rendered applications❓ built with React.
- Next.js is a solution for running react application server side.

### Only with React, developers need to spend time configuring tools and reinventing solutions for common application requirements.

### Next.js is what you would almost call the official React framework

## Downsides

### Many features are inspired by Remix. One thing Next is missing is a way to write data similar to Remix forms.

### There's no way to write *API routes* in the new app directory which seems like a sloppy loose end, as *data fetching* looks amazing but *mutations* are an entirely different story on which the team says they are working on a new *RFC* for mutating data.

### Currently, you would use a client-side component `"use client"` , write your mutation logic and then pass in a callback function of `refresh` to update any data on that route after the mutation is complete, which is similar to React query `useRouter().refresh`

### Major changes- hard to migrate code

### 90 KB baseline of client-side JS (just for warm-up)
- Other framework that can ship 0 JS app: Astro, Quick