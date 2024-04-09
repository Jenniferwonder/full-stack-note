---
DateStarted: 2023-11-30
DateModified: 2023-12-01
---
### Get Sanity Data in Next.js

#### 1. Libraries needed to get data

```jsx
// Libraries needed to get data
import type { NextPage } from "next";
import Head from "next/head";
import Image from "next/image";
import Link from "next/link";
import { useRouter } from "next/router";

// Sanity Library From Medium-Clone
import { sanityClient, urlFor } from "../sanity";

// Sanity Library From Tutorials
import { getClient, usePreviewSubscription } from "@lib/sanity";
import { groq } from "next-sanity";
```

#### 2. Functions used to get data

- getStaticProps
- useRouter
- usePreviewSubscription
- const query = groq`...`
- getClient().fetch()
- sanityClient.fetch()