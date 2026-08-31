 # React & Next.js Interview Questions & Answers — Complete Set

A bilingual (English + বাংলা) collection of React and Next.js interview questions, with brief explanations, detailed answers, and real-world examples.

---

## Table of Contents

### 🟦 React
1. [How does reconciliation decide when and what to render?](#1-how-does-reconciliation-decide-when-and-what-to-render)
2. [State vs Props](#2-state-vs-props)
3. [Controlled and Uncontrolled Components](#3-controlled-and-uncontrolled-components)
4. [useEffect Dependency Array](#4-useeffect-dependency-array)
5. [How to Optimize List Rendering in React? How Do We Use Keys in a Map?](#5-how-to-optimize-list-rendering-in-react-how-do-we-use-keys-in-a-map)
6. [Tell Me About React Fiber](#6-tell-me-about-react-fiber)
7. [React Lifecycle Phases](#7-react-lifecycle-phases)
8. [How Does the useEffect Array Work Internally?](#8-how-does-the-useeffect-array-work-internally)
9. [How to Find Re-render Issues in React and Next.js?](#9-how-to-find-re-render-issues-in-react-and-nextjs)
10. [When Should We Lift State Up and When Should We Avoid It?](#10-when-should-we-lift-state-up-and-when-should-we-avoid-it)
11. [Difference Between useMemo and useCallback](#11-difference-between-usememo-and-usecallback)
12. [After Submitting a Form, It Resets. How Do We Solve It?](#12-after-submitting-a-form-it-resets-how-do-we-solve-it)

### 🟦 Next.js
13. [CSR, SSR, SSG, ISR](#13-csr-ssr-ssg-isr)
14. [Explain File-Based Routing](#14-explain-file-based-routing)
15. [What Is the Best Case to Use ISR?](#15-what-is-the-best-case-to-use-isr)
16. [Small Data But Component Is Loading Slowly. Why?](#16-small-data-but-component-is-loading-slowly-why)
17. [What Happens When I Fetch Data Directly Inside a Server Component?](#17-what-happens-when-i-fetch-data-directly-inside-a-server-component)
18. [How Does Next.js Cache Server Data?](#18-how-does-nextjs-cache-server-data)
19. [How to Optimize a Heavy Chart in Next.js?](#19-how-to-optimize-a-heavy-chart-in-nextjs)
20. [How to Optimize the Same API Call in Next.js?](#20-how-to-optimize-the-same-api-call-in-nextjs)
21. [How Does Nested Routing Work in Next.js?](#21-how-does-nested-routing-work-in-nextjs)
22. [What Is a Server Component and How Is It Different from a Client Component?](#22-what-is-a-server-component-and-how-is-it-different-from-a-client-component)
23. [How Does Dynamic Routing Work in Next.js?](#23-how-does-dynamic-routing-work-in-nextjs)
24. [Tell Me About Route Grouping](#24-tell-me-about-route-grouping)
25. [How Do We Maintain a Protected Route?](#25-how-do-we-maintain-a-protected-route)
26. [Nested Route Not Working — How Will You Find and Fix It?](#26-nested-route-not-working--how-will-you-find-and-fix-it)
27. [How Do We Set Client-Side and Server-Side Cookies?](#27-how-do-we-set-client-side-and-server-side-cookies)
28. [How to Securely Handle a Form from User Input?](#28-how-to-securely-handle-a-form-from-user-input)
29. [What Is Middleware in Next.js / Discuss proxy.ts](#29-what-is-middleware-in-nextjs--discuss-proxyts)
30. [How Do We Handle Authentication in Server Components?](#30-how-do-we-handle-authentication-in-server-components)
31. [How Do We Structure a Large-Scale Project in React/Next.js?](#31-how-do-we-structure-a-large-scale-project-in-reactnextjs)
32. [How Do We Handle Global Error Handling?](#32-how-do-we-handle-global-error-handling)
33. [How Do We Implement Caching in Next.js?](#33-how-do-we-implement-caching-in-nextjs)
34. [What Are the Issues with Using a Heavy Server Component?](#34-what-are-the-issues-with-using-a-heavy-server-component)
35. [How Can We Maintain a Large Number of Pages in Next.js?](#35-how-can-we-maintain-a-large-number-of-pages-in-nextjs)
36. [If We Have a Large Dataset, How Can We Solve the Issue?](#36-if-we-have-a-large-dataset-how-can-we-solve-the-issue)

[⚡ Final Quick Revision](#-final-quick-revision)

---
<!--

# 🟦 REACT

## 1. How does reconciliation decide when and what to render?

### 🔹 Brief Explanation

Reconciliation হলো React-এর process যেখানে React previous UI এবং new UI compare করে দেখে কী change হয়েছে। তারপর প্রয়োজনীয় অংশ update করে।

### 🇧🇩 বাংলা — Interview Answer

Reconciliation হলো React-এর একটি process যেখানে React নতুন Virtual DOM-এর সাথে আগের Virtual DOM compare করে কোন অংশ পরিবর্তন হয়েছে তা খুঁজে বের করে। এরপর প্রয়োজনীয় UI অংশ update করে।

### 🇬🇧 English — Interview Answer

Reconciliation is the process React uses to compare the previous UI with the new UI and determine what has changed. React then updates the necessary parts of the UI.

### 💡 Real Case Example

ধরো একটি product list-এ ১০টি product আছে। একটি product-এর price change হলে React পুরো list নতুন করে না বানিয়ে প্রয়োজনীয় অংশ update করার চেষ্টা করে।

---

## 2. State vs Props

### 🔹 Brief Explanation

**State** হলো component-এর নিজের পরিবর্তনশীল data।
**Props** হলো parent থেকে child-এ পাঠানো data।

### 🇧🇩 বাংলা — Interview Answer

State হলো component-এর নিজস্ব এবং পরিবর্তনশীল data, যা component manage করতে পারে। State change হলে component re-render হতে পারে।

Props হলো parent component থেকে child component-এ পাঠানো data। Child component সরাসরি props পরিবর্তন করতে পারে না।

### 🇬🇧 English — Interview Answer

State is data managed by a component itself, and when it changes, the component may re-render.

Props are data passed from a parent component to a child component, and the child should not directly modify them.

### 💡 Real Case Example

Product name parent থেকে আসছে → **Props**।
Like button-এর clicked status → **State**।

---

## 3. Controlled and Uncontrolled Components

### 🔹 Brief Explanation

Controlled input-এর value React state control করে।
Uncontrolled input-এর value DOM নিজে manage করে।

### 🇧🇩 বাংলা — Interview Answer

Controlled component-এ input-এর value React state দ্বারা control করা হয়। Uncontrolled component-এ input-এর value DOM নিজে manage করে এবং প্রয়োজন হলে ref দিয়ে value নেওয়া হয়।

### 🇬🇧 English — Interview Answer

In a controlled component, the input value is managed by React state. In an uncontrolled component, the DOM manages the input value, and we can access it using a ref.

### 💡 Real Case Example

Login form-এর email এবং password React state দিয়ে manage করলে সেটি controlled component।

---

## 4. useEffect Dependency Array

### 🔹 Brief Explanation

Dependency array বলে দেয় `useEffect` কখন run বা re-run করবে।

* No dependency array → প্রতিটি render-এর পরে
* `[]` → initial render-এর পরে একবার
* `[count]` → initial render এবং count change হলে

### 🇧🇩 বাংলা — Interview Answer

`useEffect`-এর dependency array বলে দেয় effect কখন run করবে। Dependency array না দিলে প্রতিটি render-এর পরে run করে। Empty array দিলে initial render-এর পরে একবার run করে। আর dependency দিলে initial render-এর পরে এবং dependency change হলে আবার run করে।

### 🇬🇧 English — Interview Answer

The dependency array controls when a `useEffect` runs or re-runs. Without an array, it runs after every render. With an empty array, it runs once after the initial render. With dependencies, it runs initially and whenever those dependencies change.

### 💡 Real Case Example

`productId` change হলে নতুন product fetch করতে `[productId]` dependency ব্যবহার করা যায়।

---

## 5. How to Optimize List Rendering in React? How Do We Use Keys in a Map?

### 🔹 Brief Explanation

List-এর প্রতিটি item-এর জন্য **unique এবং stable key** ব্যবহার করা উচিত। এতে React বুঝতে পারে কোন item change, add বা remove হয়েছে।

### 🇧🇩 বাংলা — Interview Answer

List rendering optimize করার জন্য প্রতিটি item-এ unique এবং stable key ব্যবহার করি। Key React-কে identify করতে সাহায্য করে কোন item পরিবর্তন হয়েছে, যোগ হয়েছে বা remove হয়েছে।

### 🇬🇧 English — Interview Answer

To optimize list rendering, we should use a unique and stable key for each item. Keys help React identify which items have changed, been added, or removed.

### 💡 Real Case Example

Database থেকে product list এলে product-এর unique ID key হিসেবে ব্যবহার করা ভালো।

### Short Answer

> Use a unique and stable ID as the key whenever possible.

---

## 6. Tell Me About React Fiber

### 🔹 Brief Explanation

React Fiber হলো React-এর **internal rendering architecture**। এটি React-কে rendering কাজকে ছোট ছোট অংশে ভাগ করে efficiently manage করতে সাহায্য করে।

### 🇧🇩 বাংলা — Interview Answer

React Fiber হলো React-এর internal reconciliation এবং rendering architecture। এটি rendering কাজকে ছোট ছোট unit-এ ভাগ করে priority অনুযায়ী কাজ করতে সাহায্য করে। এর ফলে React গুরুত্বপূর্ণ UI update আগে handle করতে পারে এবং application-এর responsiveness improve হয়।

### 🇬🇧 English — Interview Answer

React Fiber is React's internal reconciliation and rendering architecture. It breaks rendering work into smaller units and allows React to prioritize updates, which helps improve responsiveness.

### 💡 Real Case Example

ধরো user একটি input field-এ type করছে এবং একই সময়ে অনেক complex UI update হচ্ছে। Fiber React-কে more important UI updates prioritize করতে সাহায্য করে।

---

## 7. React Lifecycle Phases

### 🔹 Brief Explanation

React component-এর lifecycle-এর ৩টি main phase:

**Mounting → Updating → Unmounting**

### 🇧🇩 বাংলা — Interview Answer

React component lifecycle মূলত তিনটি phase নিয়ে গঠিত: Mounting, Updating এবং Unmounting।

Mounting হলো component প্রথমবার UI-তে আসা। Updating হলো state বা props change হওয়ার কারণে component update হওয়া। Unmounting হলো component UI থেকে remove হয়ে যাওয়া।

### 🇬🇧 English — Interview Answer

The React component lifecycle has three main phases: Mounting, Updating, and Unmounting.

Mounting happens when the component is created and added to the UI. Updating happens when state or props change. Unmounting happens when the component is removed from the UI.

### 💡 Real Case Example

Counter প্রথমবার screen-এ আসে → Mounting।
Count change হয় → Updating।
Page change করে Counter remove হয় → Unmounting।

---

## 8. How Does the useEffect Array Work Internally?

### 🔹 Brief Explanation

React current render-এর dependency এবং previous render-এর dependency compare করে। React এই comparison-এর জন্য `Object.is` ব্যবহার করে।

### 🇧🇩 বাংলা — Interview Answer

React প্রতিটি render-এর সময় current dependency values-কে previous render-এর dependency values-এর সাথে compare করে। যদি কোনো dependency change হয়, তাহলে effect আবার run করে। Dependency change না হলে effect skip করে।

### 🇬🇧 English — Interview Answer

React compares the current dependency values with the previous render's dependency values. It uses `Object.is` for the comparison. If a dependency changes, the effect runs again; otherwise, it is skipped.

### 💡 Real Case Example

`[userId]` dependency থাকলে `userId` 10 থেকে 20 হলে effect আবার run করবে।

---

## 9. How to Find Re-render Issues in React and Next.js?

### 🔹 Brief Explanation

React DevTools Profiler ব্যবহার করে দেখা যায় কোন component unnecessarily re-render হচ্ছে।

### 🇧🇩 বাংলা — Interview Answer

Re-render issue খুঁজে বের করার জন্য আমি React DevTools Profiler ব্যবহার করি। এছাড়া console log দিয়ে render frequency check করতে পারি। তারপর state change, props change, parent re-render, context update বা changing references-এর কারণে unnecessary re-render হচ্ছে কিনা দেখি।

### 🇬🇧 English — Interview Answer

I use React DevTools Profiler to identify which components are re-rendering and why. I can also use console logs to check render frequency. Then I check state changes, prop changes, parent re-renders, context updates, and changing references.

### 💡 Real Case Example

Parent component-এর state change হওয়ার কারণে child unnecessarily re-render করলে Profiler দিয়ে সেটা identify করা যায়।

---

## 10. When Should We Lift State Up and When Should We Avoid It?

### 🔹 Brief Explanation

একাধিক component-এর একই state দরকার হলে state common parent-এ নেওয়া হয়। শুধু একটি component-এর দরকার হলে local রাখা ভালো।

### 🇧🇩 বাংলা — Interview Answer

যখন একাধিক component-এর একই state দরকার হয়, তখন state-কে তাদের closest common parent-এ lift করা উচিত। কিন্তু state যদি শুধু একটি component-এর দরকার হয়, তাহলে সেটাকে local রাখা ভালো।

### 🇬🇧 English — Interview Answer

We should lift state up when multiple components need to share the same state. If only one component needs the state, it is better to keep it local.

### 💡 Real Case Example

Search input এবং ProductList একই search value ব্যবহার করলে search state common parent-এ রাখা যায়।

---

## 11. Difference Between useMemo and useCallback

### 🔹 Brief Explanation

`useMemo` → calculated value/result memoize করে।
`useCallback` → function reference memoize করে।

### 🇧🇩 বাংলা — Interview Answer

`useMemo` expensive calculation-এর result memoize করে। Dependency change না হলে আগের result reuse করা যায়।

`useCallback` একটি function-এর reference memoize করে। Dependency change না হলে একই function reference reuse করা যায়।

### 🇬🇧 English — Interview Answer

`useMemo` memoizes the result of a calculation, while `useCallback` memoizes a function reference.

### 💡 Real Case Example

১০,০০০ users filter করার expensive calculation থাকলে `useMemo` ব্যবহার করা যেতে পারে।

Child component-এ callback পাঠানোর সময় unnecessary function reference changes কমাতে `useCallback` ব্যবহার করা যেতে পারে।

### Short Answer

> useMemo memoizes a value; useCallback memoizes a function reference.

---

## 12. After Submitting a Form, It Resets. How Do We Solve It?

### 🔹 Brief Explanation

Form submit করলে browser-এর default behavior page reload করতে পারে। তাই React state reset হয়ে যেতে পারে।

### 🇧🇩 বাংলা — Interview Answer

Form submit করার পর page reload হয়ে reset হলে `preventDefault()` ব্যবহার করে browser-এর default submission বন্ধ করি। এরপর form submission API বা প্রয়োজনীয় logic দিয়ে handle করি।

### 🇬🇧 English — Interview Answer

If a form resets because the browser reloads the page after submission, I use `preventDefault()` to stop the default form submission and then handle the submission using my own logic or API request.

### 💡 Real Case Example

Login form submit করার পর page reload হয়ে গেলে `preventDefault()` ব্যবহার করে API request করা যায়।

---

# 🟦 NEXT.JS

## 13. CSR, SSR, SSG, ISR

### 🔹 Brief Explanation

* **CSR** → Browser-এ rendering
* **SSR** → Request-এর সময় server-এ rendering
* **SSG** → Build time-এ page তৈরি
* **ISR** → Static page + পরে revalidation

### 🇧🇩 বাংলা — Interview Answer

CSR-এ browser-side-এ UI render হয়। SSR-এ request আসার সময় server HTML তৈরি করে। SSG-এ build time-এ page generate হয়। ISR static page তৈরি করে এবং প্রয়োজন অনুযায়ী পরে revalidate বা update করতে পারে।

### 🇬🇧 English — Interview Answer

CSR renders mainly on the client. SSR generates HTML on the server for a request. SSG generates pages at build time. ISR generates static pages and allows them to be updated through revalidation.

### 💡 Real Case Example

Blog বা product page-এর content যদি মাঝে মাঝে change হয়, ISR ভালো option হতে পারে।

---

## 14. Explain File-Based Routing

### 🔹 Brief Explanation

Next.js-এ folder এবং file structure-এর উপর ভিত্তি করে automatically routes তৈরি হয়।

### 🇧🇩 বাংলা — Interview Answer

File-based routing হলো এমন একটি routing system যেখানে folder এবং file structure-এর ভিত্তিতে automatically route তৈরি হয়। তাই প্রতিটি route manually configure করার প্রয়োজন হয় না।

### 🇬🇧 English — Interview Answer

File-based routing is a routing system where routes are automatically created based on the folder and file structure.

### 💡 Real Case Example

`app/products/page.tsx` → `/products`

---

## 15. What Is the Best Case to Use ISR?

### 🔹 Brief Explanation

যে data মাঝে মাঝে change হয় কিন্তু প্রতিটি request-এ fresh page generate করার দরকার নেই, সেখানে ISR ভালো।

### 🇧🇩 বাংলা — Interview Answer

ISR এমন page-এর জন্য ভালো যেখানে content periodically change হয় কিন্তু প্রতিটি request-এর সময় server-side rendering করার প্রয়োজন নেই।

### 🇬🇧 English — Interview Answer

ISR is best for pages where content changes periodically but does not need to be regenerated on every request.

### 💡 Real Case Example

Product details, blog posts, hotel listings বা category pages।

---

## 16. Small Data But Component Is Loading Slowly. Why?

### 🔹 Brief Explanation

Data ছোট হলেই component fast হবে এমন নয়। API, network, rendering বা fetching logic slow হতে পারে।

### 🇧🇩 বাংলা — Interview Answer

Small data হলেও component slow হতে পারে। কারণ হতে পারে slow API response, network latency, unnecessary re-render, parent re-render, repeated API calls বা inefficient data fetching logic।

### 🇬🇧 English — Interview Answer

Even with small data, a component can be slow because of slow API responses, network latency, unnecessary re-renders, parent re-renders, repeated API calls, or inefficient data fetching logic.

### 💡 Real Case Example

Component শুধু ৫টি user fetch করছে, কিন্তু API response আসতে ৩ seconds লাগছে। এখানে problem data size নয়, API/network।

---

## 17. What Happens When I Fetch Data Directly Inside a Server Component?

### 🔹 Brief Explanation

Server Component থেকে data fetch করলে fetching **server-এ execute হয়**।

### 🇧🇩 বাংলা — Interview Answer

Server Component-এর ভিতরে data fetch করলে fetching server-এ execute হয়। Server API বা database থেকে data নিয়ে component render করে এবং rendered result client-এ পাঠায়।

### 🇬🇧 English — Interview Answer

When we fetch data directly inside a Server Component, the data fetching runs on the server. The server gets the data, renders the component, and sends the result to the client.

### 💡 Real Case Example

Product Server Component সরাসরি database থেকে product data fetch করে server-এ render করতে পারে।

---

## 18. How Does Next.js Cache Server Data?

### 🔹 Brief Explanation

Caching মানে fetched data কিছু সময়ের জন্য reuse করা, যাতে unnecessaryভাবে আবার fetch করতে না হয়।

### 🇧🇩 বাংলা — Interview Answer

Next.js server-side data caching এবং revalidation support করে। Current Next.js-এ প্রতিটি `fetch()` automatically cached হবে এমন ধরে নেওয়া উচিত নয়। প্রয়োজন অনুযায়ী caching বা revalidation configure করা যায়।

### 🇬🇧 English — Interview Answer

Next.js supports server-side data caching and revalidation. In current Next.js versions, we should not assume that every `fetch()` request is automatically cached. We can configure caching or revalidation when needed.

### 💡 Real Case Example

Product data frequently change না করলে cache করে রাখা এবং নির্দিষ্ট সময় পর revalidate করা যায়।

---

## 19. How to Optimize a Heavy Chart in Next.js?

### 🔹 Brief Explanation

Heavy chart page load এবং rendering slow করতে পারে। তাই chart lazy-load করা এবং unnecessary data কমানো ভালো।

### 🇧🇩 বাংলা — Interview Answer

Heavy chart optimize করার জন্য chart-কে আলাদা Client Component করে dynamic import বা lazy loading ব্যবহার করতে পারি। এছাড়া unnecessary re-render কমাতে এবং large dataset হলে data reduce বা aggregate করতে পারি।

### 🇬🇧 English — Interview Answer

To optimize a heavy chart, I can separate it into a Client Component and use dynamic import or lazy loading. I can also reduce unnecessary re-renders and reduce or aggregate the data when the dataset is large.

### 💡 Real Case Example

Dashboard-এর chart-এ ৫০,০০০ data points থাকলে সব একসাথে render না করে data aggregate করে chart lazy-load করা যায়।

---

## 20. How to Optimize the Same API Call in Next.js?

### 🔹 Brief Explanation

একই data-এর জন্য একই API বারবার call করা unnecessary। Caching এবং request deduplication ব্যবহার করা যায়।

### 🇧🇩 বাংলা — Interview Answer

একই API call optimize করার জন্য প্রথমে দেখি একই data বারবার fetch হচ্ছে কিনা। Caching এবং request deduplication ব্যবহার করে duplicate requests কমানো যায়। Client-side shared data-এর জন্য SWR বা TanStack Query-এর মতো library ব্যবহার করা যেতে পারে।

### 🇬🇧 English — Interview Answer

To optimize the same API call, I first check whether the same data is being fetched multiple times. I can use caching and request deduplication to reduce duplicate requests. For shared client-side data, libraries such as SWR or TanStack Query can also be used.

### 💡 Real Case Example

Dashboard-এর তিনটি component একই user data চাইলে তিনবার request না করে shared/cached data ব্যবহার করা যায়।

---

## 21. How Does Nested Routing Work in Next.js?

### 🔹 Brief Explanation

Nested routing মানে একটি route-এর ভিতরে আরেকটি route থাকা। Next.js-এ folder-এর ভিতরে folder তৈরি করে nested route করা যায়।

### 🇧🇩 বাংলা — Interview Answer

Next.js App Router-এ folder structure ব্যবহার করে nested routing তৈরি করা হয়। একটি folder-এর ভিতরে আরেকটি folder এবং তার মধ্যে `page.tsx` রাখলে nested URL তৈরি হয়।

### 🇬🇧 English — Interview Answer

In the Next.js App Router, nested routes are created using nested folders. A folder inside another route folder creates a nested URL.

### 💡 Real Case Example

`app/dashboard/settings/page.tsx` → `/dashboard/settings`

---

## 22. What Is a Server Component and How Is It Different from a Client Component?

### 🔹 Brief Explanation

**Server Component** server-এ render হয় এবং server-side data access করতে পারে।

**Client Component** browser-এ interactive behavior-এর জন্য ব্যবহার হয় এবং `"use client"` প্রয়োজন হয়।

### 🇧🇩 বাংলা — Interview Answer

Server Component server-এ render হয় এবং server-side data fetching ও database access-এর মতো কাজ করতে পারে। Client Component browser-এ run করে এবং state, event handling ও browser APIs-এর মতো interactive features ব্যবহার করতে পারে।

### 🇬🇧 English — Interview Answer

Server Components render on the server and can perform server-side data fetching or access server-side resources. Client Components run on the browser and are used for interactivity, state, event handling, and browser APIs.

### 💡 Real Case Example

Product information display → Server Component।
Add-to-cart button with interactive state → Client Component।

---

## 23. How Does Dynamic Routing Work in Next.js?

### 🔹 Brief Explanation

Dynamic routing ব্যবহার করলে একই page structure দিয়ে different dynamic values-এর জন্য route তৈরি করা যায়।

### 🇧🇩 বাংলা — Interview Answer

Next.js-এ dynamic routing-এর জন্য square brackets ব্যবহার করা হয়। যেমন `[id]`। এতে একই page বিভিন্ন dynamic value-এর জন্য ব্যবহার করা যায়।

### 🇬🇧 English — Interview Answer

Dynamic routing in Next.js uses square brackets such as `[id]` to create routes with dynamic values. The same page can then handle different values.

### 💡 Real Case Example

`products/[id]/page.tsx`

এর মাধ্যমে:

`/products/101`
`/products/102`
`/products/103`

একই dynamic page দিয়ে handle করা যায়।

---

## 24. Tell Me About Route Grouping

### 🔹 Brief Explanation

Route Grouping related routes organize করে কিন্তু group-এর নাম URL-এ আসে না।

### 🇧🇩 বাংলা — Interview Answer

Route Grouping হলো Next.js App Router-এর feature যেখানে parentheses ব্যবহার করে related routes group করা যায়। Group name URL-এর অংশ হয় না। এটি routes organize এবং shared layout ব্যবহার করার জন্য useful।

### 🇬🇧 English — Interview Answer

Route grouping allows us to organize related routes using parentheses without including the group name in the URL. It is useful for organizing routes and sharing layouts.

### 💡 Real Case Example

`(auth)/login/page.tsx` → `/login`

`(auth)` URL-এর মধ্যে থাকবে না।

---

## 25. How Do We Maintain a Protected Route?

### 🔹 Brief Explanation

Protected route শুধু authenticated বা authorized user-এর জন্য accessible।

### 🇧🇩 বাংলা — Interview Answer

Protected route maintain করার জন্য user authenticated এবং প্রয়োজন হলে authorized কিনা check করি। Authentication না থাকলে login page-এ redirect করি। Authorized হলে requested page access করতে দিই।

### 🇬🇧 English — Interview Answer

To maintain a protected route, I check whether the user is authenticated and, when required, authorized. If not, I redirect them to the login page. Otherwise, I allow access.

### 💡 Real Case Example

`/dashboard` শুধু logged-in users-এর জন্য। Logged-out user `/dashboard` visit করলে `/login`-এ redirect হবে।

---

## 26. Nested Route Not Working — How Will You Find and Fix It?

### 🔹 Brief Explanation

প্রথমে folder structure, `page.tsx`, URL এবং dynamic segments check করতে হবে।

### 🇧🇩 বাংলা — Interview Answer

Nested route কাজ না করলে প্রথমে folder structure এবং URL path check করব। সঠিক জায়গায় `page.tsx` আছে কিনা দেখব। এরপর dynamic route, layout, route group এবং route conflict check করব। তারপর browser URL এবং Next.js error message দেখে problem fix করব।

### 🇬🇧 English — Interview Answer

If a nested route is not working, I first check the folder structure and URL path. Then I check `page.tsx`, dynamic segments, layouts, route groups, and route conflicts. Finally, I check the browser URL and Next.js error messages.

### 💡 Real Case Example

`/dashboard/settings` কাজ না করলে `app/dashboard/settings/page.tsx` ঠিক আছে কিনা check করব।

---

## 27. How Do We Set Client-Side and Server-Side Cookies?

### 🔹 Brief Explanation

Client-side cookie browser JavaScript দিয়ে set করা যায়। Server-side cookie server থেকে set করা যায়।

### 🇧🇩 বাংলা — Interview Answer

Client-side cookie set করার জন্য `document.cookie` ব্যবহার করা যায়। Server-side cookie-এর জন্য Next.js-এর `cookies()` API বা `Set-Cookie` header ব্যবহার করা যায়।

Authentication-এর জন্য HttpOnly এবং Secure cookie ব্যবহার করা বেশি নিরাপদ।

### 🇬🇧 English — Interview Answer

For client-side cookies, we can use `document.cookie`. For server-side cookies, we can use the `cookies()` API or the `Set-Cookie` header.

For authentication, HttpOnly and Secure cookies are generally preferred.

### 💡 Real Case Example

Login করার পরে server একটি HttpOnly authentication cookie set করতে পারে। Browser পরবর্তী request-এ cookie পাঠাবে।

---

## 28. How to Securely Handle a Form from User Input?

### 🔹 Brief Explanation

User input কখনো trust করা যাবে না। Server-side validation অবশ্যই করতে হবে।

### 🇧🇩 বাংলা — Interview Answer

User input securely handle করার জন্য client-side এবং server-side validation করি। তবে security-এর জন্য server-side validation সবচেয়ে গুরুত্বপূর্ণ। প্রয়োজন অনুযায়ী input sanitize করি, secure database queries ব্যবহার করি, password hash করি এবং XSS ও CSRF-এর মতো attacks থেকে protection রাখি।

### 🇬🇧 English — Interview Answer

To securely handle user input, I validate it on both the client and server, but I never trust client-side input. I use secure database queries, hash passwords, and protect against common attacks such as XSS and CSRF.

### 💡 Real Case Example

Registration form frontend-এ email valid হলেও server আবার validation করবে।

---

## 29. What Is Middleware in Next.js / Discuss proxy.ts

### 🔹 Brief Explanation

Proxy request page-এ পৌঁছানোর আগে request process করতে পারে।

### 🇧🇩 বাংলা — Interview Answer

Next.js-এ Proxy হলো request processing layer যা request page বা route-এ পৌঁছানোর আগে run করতে পারে। এটি authentication, authorization, redirect এবং route protection-এর মতো কাজে ব্যবহার করা যায়।

বর্তমান Next.js versions-এ `proxy.ts` convention ব্যবহার করা হচ্ছে।

### 🇬🇧 English — Interview Answer

In Next.js, Proxy is a request processing layer that can run before a request reaches a page or route. It can be used for authentication, authorization, redirects, and route protection.

In current Next.js versions, `proxy.ts` is used for this purpose.

### 💡 Real Case Example

User `/dashboard` visit করলে Proxy আগে authentication check করতে পারে। Logged out হলে `/login`-এ redirect করতে পারে।

---

## 30. How Do We Handle Authentication in Server Components?

### 🔹 Brief Explanation

Server Component-এ authentication **server-side-এ** check করা হয়।

### 🇧🇩 বাংলা — Interview Answer

Server Component-এ authentication handle করার জন্য server-side-এ user's session বা authentication cookie verify করি। User authenticated হলে protected data fetch করে component render করি। Authentication না থাকলে login page-এ redirect করি।

### 🇬🇧 English — Interview Answer

To handle authentication in a Server Component, I verify the user's session or authentication cookie on the server. If authenticated, I fetch protected data and render the component. Otherwise, I redirect to the login page.

### 💡 Real Case Example

`/dashboard` Server Component session check করে। Valid session থাকলে user's private dashboard data fetch করে।

### Important Difference

> **Proxy → Route protect করে**
> **Server Component → Data and rendering protect করে**

---

## 31. How Do We Structure a Large-Scale Project in React/Next.js?

### 🔹 Brief Explanation

Large project-এ code feature এবং responsibility অনুযায়ী ভাগ করা হয়।

### 🇧🇩 বাংলা — Interview Answer

Large-scale React/Next.js project-এ আমি feature-based architecture ব্যবহার করতে পছন্দ করি। Related components, hooks, API logic এবং types একই feature-এর মধ্যে রাখি। Shared components এবং utilities আলাদা রাখি।

এতে separation of concerns বজায় থাকে এবং project maintain ও scale করা সহজ হয়।

### 🇬🇧 English — Interview Answer

For a large-scale React/Next.js project, I prefer a feature-based architecture. I keep related components, hooks, API logic, and types together within each feature. Shared components and utilities are kept separately.

This provides separation of concerns and makes the project easier to maintain and scale.

### 💡 Real Case Example

E-commerce project:

* `products`
* `cart`
* `auth`
* `checkout`

প্রতিটি feature-এর নিজের components, hooks এবং API logic থাকতে পারে।

---

## 32. How Do We Handle Global Error Handling?

### 🔹 Brief Explanation

Global error handling মানে application-এর error centralizedভাবে handle করা।

### 🇧🇩 বাংলা — Interview Answer

Global error handling-এর জন্য centralized approach ব্যবহার করি। Next.js-এ UI rendering error-এর জন্য `error.tsx` বা Error Boundary ব্যবহার করা যায়। API/server errors centralizedভাবে handle করি এবং unexpected errors logging বা monitoring system-এ track করি।

### 🇬🇧 English — Interview Answer

For global error handling, I use a centralized approach. In Next.js, `error.tsx` or Error Boundaries can handle UI rendering errors. API and server errors can be handled centrally, while unexpected errors can be tracked using logging or monitoring.

### 💡 Real Case Example

Dashboard-এর কোনো component crash করলে `error.tsx` user-friendly error UI দেখাতে পারে।

---

## 33. How Do We Implement Caching in Next.js?

### 🔹 Brief Explanation

Caching করলে একই data বারবার fetch না করে cached data reuse করা যায়।

### 🇧🇩 বাংলা — Interview Answer

Next.js-এ server-side caching এবং revalidation ব্যবহার করতে পারি। প্রয়োজন অনুযায়ী data cache করি এবং নির্দিষ্ট সময় পর revalidate করে নতুন data আনি। Client-side shared data-এর জন্য client-side caching solution ব্যবহার করা যায়।

### 🇬🇧 English — Interview Answer

In Next.js, we can implement caching using server-side caching and revalidation. We cache data when appropriate and revalidate it when it needs to be refreshed. For shared client-side data, we can also use client-side caching solutions.

### 💡 Real Case Example

Product catalog frequently change না করলে cached data ব্যবহার করা যায় এবং পরে revalidate করা যায়।

---

## 34. What Are the Issues with Using a Heavy Server Component?

### 🔹 Brief Explanation

Heavy Server Component বেশি computation বা data fetching করলে server response slow হতে পারে।

### 🇧🇩 বাংলা — Interview Answer

Heavy Server Component-এ বেশি computation বা data fetching থাকলে server processing time, response time এবং server load বেড়ে যেতে পারে। তাই unnecessary work কমানো, data fetching optimize করা এবং caching ব্যবহার করা উচিত।

### 🇬🇧 English — Interview Answer

A heavy Server Component can perform too much computation or data fetching, which can increase server processing time, response time, and server load. I would reduce unnecessary work, optimize data fetching, and use caching where appropriate.

### 💡 Real Case Example

একটি Server Component একসাথে অনেক API call এবং complex calculation করলে page response slow হতে পারে।

---

## 35. How Can We Maintain a Large Number of Pages in Next.js?

### 🔹 Brief Explanation

অনেক page হলে duplicate code না লিখে dynamic routes, layouts এবং reusable components ব্যবহার করা উচিত।

### 🇧🇩 বাংলা — Interview Answer

Large number of pages maintain করার জন্য clear folder structure, dynamic routes, shared layouts এবং reusable components ব্যবহার করি। Similar pages-এর জন্য dynamic routing ব্যবহার করি যাতে duplicate pages তৈরি করতে না হয়।

### 🇬🇧 English — Interview Answer

To maintain a large number of pages, I use a clear folder structure, dynamic routes, shared layouts, and reusable components. For similar pages, I use dynamic routing instead of creating duplicated pages.

### 💡 Real Case Example

১০০টি product-এর জন্য ১০০টি আলাদা page না বানিয়ে একটি dynamic `[id]` route ব্যবহার করা যায়।

---

## 36. If We Have a Large Dataset, How Can We Solve the Issue?

### 🔹 Brief Explanation

একসাথে হাজার হাজার data fetch এবং render করা উচিত নয়। Data ছোট অংশে load করা উচিত।

### 🇧🇩 বাংলা — Interview Answer

Large dataset হলে একসাথে সব data fetch বা render করি না। Server-side pagination, filtering এবং searching ব্যবহার করে প্রয়োজনীয় data fetch করি। অনেক বড় list browser-এ render করতে হলে virtualization বা infinite scrolling ব্যবহার করতে পারি।

### 🇬🇧 English — Interview Answer

For a large dataset, I avoid fetching and rendering everything at once. I use server-side pagination, filtering, and searching to fetch only the required data. For very large lists, I can also use virtualization or infinite scrolling.

### 💡 Real Case Example

Database-এ যদি ১ লাখ users থাকে, তাহলে একবারে ১ লাখ user browser-এ না পাঠিয়ে প্রতি page-এ ২০–৫০টি user পাঠানো যায়।

### Short Answer

> Use pagination, server-side filtering/searching, and virtualization to handle large datasets efficiently.

---

# ⚡ FINAL QUICK REVISION

## React

1. **Reconciliation** → Previous UI vs new UI compare করে necessary update।
2. **State vs Props** → State is internal; props come from parent.
3. **Controlled** → React controls input.
4. **Uncontrolled** → DOM controls input.
5. **useEffect `[]`** → Initial render-এর পরে একবার.
6. **useEffect `[dep]`** → Initial + dependency change.
7. **No dependency array** → Every render-এর পরে.
8. **Keys** → Unique and stable key.
9. **Fiber** → React-এর internal rendering/reconciliation architecture.
10. **Lifecycle** → Mount → Update → Unmount.
11. **Re-render debugging** → React DevTools Profiler.
12. **Lift state** → Multiple components একই state চাইলে.
13. **useMemo** → Memoize value/result.
14. **useCallback** → Memoize function reference.
15. **Form reset** → Prevent default submission.

## Next.js

16. **CSR** → Client.
17. **SSR** → Request time server rendering.
18. **SSG** → Build time generation.
19. **ISR** → Static + revalidation.
20. **File-based routing** → Folder/file creates route.
21. **Nested routing** → Nested folders create nested URLs.
22. **Dynamic routing** → `[id]`, `[slug]`.
23. **Route grouping** → `(group)` URL-এ আসে না।
24. **Server Component** → Server-side rendering/data access.
25. **Client Component** → Interactivity/state/browser APIs.
26. **Protected route** → Authentication/authorization check.
27. **Proxy** → Request-এর আগে processing.
28. **Server authentication** → Verify session/cookie on server.
29. **Cookies** → Client: `document.cookie`; Server: `cookies()`/`Set-Cookie`.
30. **Secure forms** → Validate server-side, protect sensitive data.
31. **Caching** → Cache + revalidation when needed.
32. **Same API optimization** → Caching + request deduplication.
33. **Heavy chart** → Lazy load + reduce data + prevent re-render.
34. **Heavy Server Component** → Can increase server processing/response time.
35. **Large project** → Feature-based architecture.
36. **Many pages** → Dynamic routes + layouts + reusable components.
37. **Large dataset** → Pagination + filtering + searching + virtualization.
38. **Global errors** → `error.tsx`/Error Boundary + centralized server/API handling. -->