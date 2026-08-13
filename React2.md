# React Interview Questions & Answers (Q46–Q60)

A bilingual (English + বাংলা) collection of React interview questions with natural, speakable answers — great for interview prep.

---
## Q46. What is the `useReducer` hook and when is it preferred over `useState`?

🔑 **Keywords:**
- complex state logic
- reducer function
- current state + action
- new state
- multiple related updates

**🇬🇧 English**

useReducer is a React hook that I use to manage complex state logic. It works with a reducer function that takes the current state and an action and returns a new state. I prefer useReducer over useState when I have multiple related state updates or complex state logic.

**🇧🇩 বাংলা**

useReducer হলো React-এর একটি hook, যেটা আমি complex state logic manage করার জন্য ব্যবহার করি। এটি একটি reducer function-এর সাথে কাজ করে, যেটা current state এবং একটি action নেয় এবং একটি new state return করে। যখন আমার multiple related state updates বা complex state logic থাকে, তখন আমি useState-এর পরিবর্তে useReducer পছন্দ করি।

---

## Q47. Explain the `useMemo` hook and give a use case.

🔑 **Keywords:**
- memoize value
- store result
- recalculate on dependency change
- expensive calculation

**🇬🇧 English**

useMemo is a React hook that I use to memoize a calculated value. React stores the result and recalculates it only when its dependencies change. I use it when a calculation takes a lot of time and I want to avoid unnecessary recalculations.

**🇧🇩 বাংলা**

useMemo হলো React-এর একটি hook, যেটা আমি একটি calculated value memoize করার জন্য ব্যবহার করি। React result-টি store করে রাখে এবং শুধুমাত্র dependencies পরিবর্তন হলে আবার calculate করে। যখন কোনো calculation অনেক সময় নেয় এবং আমি অপ্রয়োজনীয় recalculation এড়াতে চাই, তখন আমি এটি ব্যবহার করি।

---

<!-- ## Q48. What is the `useCallback` hook and when do you use it?

🔑 **Keywords:**
- memoize function
- same reference
- dependencies change
- memoized child / dependency array

**🇬🇧 English**

useCallback is a React hook that I use to memoize a function. It keeps the same function reference between renders until its dependencies change. I mainly use it when I pass a function to a memoized child component or when a function appears in another hook's dependency array.

**🇧🇩 বাংলা**

useCallback হলো React-এর একটি hook, যেটা আমি একটি function memoize করার জন্য ব্যবহার করি। Dependencies পরিবর্তন না হওয়া পর্যন্ত এটি renders-এর মধ্যে একই function reference ধরে রাখে। যখন আমি একটি function-কে memoized child component-এ pass করি অথবা কোনো function অন্য hook-এর dependency array-তে থাকে, তখন আমি মূলত useCallback ব্যবহার করি।

---

## Q49. What is React Router and how do you set up client-side routing?

🔑 **Keywords:**
- navigation/routing library
- routes
- map to URLs
- `/`, `/about`, `/contact`

**🇬🇧 English**

React Router is a library that I use to manage navigation and routing in React applications. I create routes for different components and map them to different URLs. For example, I can create routes like `/`, `/about`, and `/contact` and render different components for each route.

**🇧🇩 বাংলা**

React Router হলো একটি library, যেটা আমি React application-এ navigation এবং routing manage করার জন্য ব্যবহার করি। আমি বিভিন্ন component-এর জন্য route তৈরি করি এবং সেগুলোকে বিভিন্ন URL-এর সাথে map করি। যেমন, আমি `/`, `/about`, এবং `/contact`-এর মতো route তৈরি করতে পারি এবং প্রতিটি route-এর জন্য আলাদা component render করতে পারি।

---

## Q50. What is the difference between `useNavigate` and `Link` in React Router?

🔑 **Keywords:**
- Link = click navigation
- useNavigate = programmatic navigation
- e.g. after login redirect

**🇬🇧 English**

I use Link when I want users to navigate by clicking a link. I use useNavigate when I want to navigate programmatically based on some logic or an event. For example, after a successful login, I can use useNavigate to redirect the user to the dashboard.

**🇧🇩 বাংলা**

আমি Link ব্যবহার করি যখন আমি চাই user কোনো link-এ click করে navigate করুক। আমি useNavigate ব্যবহার করি যখন আমি কোনো logic বা event-এর ভিত্তিতে programmatically navigate করতে চাই। যেমন, successful login-এর পর আমি user-কে dashboard-এ redirect করার জন্য useNavigate ব্যবহার করতে পারি।

---

## Q51. What are custom hooks in React? Write a simple example.

🔑 **Keywords:**
- reusable function
- share stateful logic
- starts with `use`
- e.g. useFetch

**🇬🇧 English**

Custom hooks are reusable functions that I create to share stateful logic between components. A custom hook usually starts with the word `use`. For example, I can create a `useFetch` hook to handle API requests and reuse it in multiple components.

**🇧🇩 বাংলা**

Custom hook হলো এমন reusable function, যেটা আমি বিভিন্ন component-এর মধ্যে stateful logic share করার জন্য তৈরি করি। একটি custom hook সাধারণত `use` শব্দ দিয়ে শুরু হয়। যেমন, API request handle করার জন্য আমি একটি `useFetch` hook তৈরি করতে পারি এবং সেটি একাধিক component-এ পুনরায় ব্যবহার করতে পারি।

---

## Q52. What is lazy loading in React and how is it implemented?

🔑 **Keywords:**
- load on demand
- React.lazy() + Suspense
- reduce initial bundle
- improve load time

**🇬🇧 English**

Lazy loading means loading a component only when I need it instead of loading everything at the beginning. I can implement lazy loading with `React.lazy()` and `Suspense`. It helps reduce the initial bundle size and improves the initial loading performance.

**🇧🇩 বাংলা**

Lazy loading মানে হলো শুরুতেই সবকিছু load না করে, যখন আমার একটি component দরকার হয় তখনই সেটি load করা। আমি `React.lazy()` এবং `Suspense` দিয়ে lazy loading implement করতে পারি। এটি initial bundle size কমাতে সাহায্য করে এবং initial loading performance উন্নত করে।

---

## Q53. What are React error boundaries and why are they useful?

🔑 **Keywords:**
- catch JS errors
- component tree
- fallback UI
- prevent app crash

**🇬🇧 English**

Error boundaries help me catch JavaScript errors in a component tree and show a fallback UI instead of breaking the entire application. I can use them around important parts of my application to improve error handling and user experience.

**🇧🇩 বাংলা**

Error boundaries আমাকে একটি component tree-তে JavaScript error catch করতে এবং পুরো application ভেঙে না গিয়ে একটি fallback UI দেখাতে সাহায্য করে। আমি আমার application-এর গুরুত্বপূর্ণ অংশগুলোর চারপাশে এগুলো ব্যবহার করে error handling এবং user experience উন্নত করতে পারি।

---

## Q54. What is the Context API and when should you use Redux instead?

🔑 **Keywords:**
- Context = share data, no prop drilling
- theme/auth/language
- Redux = large/complex global state
- predictable/centralized management

**🇬🇧 English**

The Context API helps me share data between components without passing props through every level. I use it for things like themes, authentication information, or language settings.

I choose Redux when my application has large and complex global state, many state updates, or when I need predictable and centralized state management.

**🇧🇩 বাংলা**

Context API আমাকে প্রতিটি level দিয়ে props pass না করেই component-গুলোর মধ্যে data share করতে সাহায্য করে। আমি এটি theme, authentication information, বা language settings-এর মতো বিষয়গুলোর জন্য ব্যবহার করি।

আমি Redux বেছে নিই যখন আমার application-এ বড় এবং complex global state থাকে, অনেক state update থাকে, অথবা আমার predictable এবং centralized state management দরকার হয়।

---

## Q55. Explain the concept of reconciliation in React.

🔑 **Keywords:**
- compare old vs new Virtual DOM
- identify changes
- update only necessary real DOM parts

**🇬🇧 English**

Reconciliation is the process React uses to compare the previous Virtual DOM with the new Virtual DOM. React identifies what changed and updates only the necessary parts of the real DOM. This approach helps React update the UI efficiently.

**🇧🇩 বাংলা**

Reconciliation হলো সেই process, যেটা React আগের Virtual DOM-কে নতুন Virtual DOM-এর সাথে তুলনা করার জন্য ব্যবহার করে। React কী পরিবর্তন হয়েছে সেটি identify করে এবং real DOM-এর শুধুমাত্র প্রয়োজনীয় অংশগুলো update করে। এই approach React-কে efficient ভাবে UI update করতে সাহায্য করে।

---

## Q56. What is the difference between `React.Fragment` and empty tags (`<> </>`)?

🔑 **Keywords:**
- group elements, no extra DOM node
- syntax difference
- `<>` = short syntax
- Fragment = supports `key` prop

**🇬🇧 English**

Both React.Fragment and empty tags allow me to group multiple elements without adding an extra DOM element.

The main difference is syntax. I can write the short syntax as `<>...</>`, while React.Fragment gives me more options, such as using a `key` prop.

**🇧🇩 বাংলা**

React.Fragment এবং empty tags — দুটোই আমাকে অতিরিক্ত DOM element যোগ না করে একাধিক element group করতে দেয়।

মূল পার্থক্য হলো syntax-এ। আমি short syntax হিসেবে `<>...</>` লিখতে পারি, যেখানে React.Fragment আমাকে আরও বেশি option দেয়, যেমন `key` prop ব্যবহার করা।

---

## Q57. How do you handle forms in React? Explain with Formik or react-hook-form.

🔑 **Keywords:**
- manage form state/validation/errors
- `register` inputs
- `handleSubmit` submission

**🇬🇧 English**

I usually use react-hook-form to handle forms in React. It helps me manage form state, validation, errors, and submission efficiently. I register my inputs with the `register` function and handle form submission with `handleSubmit`.

**🇧🇩 বাংলা**

React-এ form handle করার জন্য আমি সাধারণত react-hook-form ব্যবহার করি। এটি form state, validation, error, এবং submission efficiently manage করতে সাহায্য করে। আমি `register` function দিয়ে আমার input-গুলো register করি এবং `handleSubmit` দিয়ে form submission handle করি।

---

## Q58. What is code splitting in React and how does it improve performance?

🔑 **Keywords:**
- split JS bundle
- smaller chunks
- load only needed code
- dynamic import / React.lazy()

**🇬🇧 English**

Code splitting means dividing my application's JavaScript bundle into smaller chunks. Instead of loading the entire application at once, I can load only the code that the user currently needs. I can implement it using dynamic imports and `React.lazy()`. This reduces the initial bundle size and improves loading performance.

**🇧🇩 বাংলা**

Code splitting মানে হলো আমার application-এর JavaScript bundle-কে ছোট ছোট chunk-এ ভাগ করা। পুরো application একসাথে load না করে, আমি শুধুমাত্র সেই code load করতে পারি যেটা user-এর বর্তমানে দরকার। আমি এটি dynamic import এবং `React.lazy()` ব্যবহার করে implement করতে পারি। এটি initial bundle size কমায় এবং loading performance উন্নত করে।

---

## Q59. What are portals in React and when are they useful?

🔑 **Keywords:**
- render outside parent DOM hierarchy
- modals/dialogs/tooltips/dropdowns
- avoid overflow/z-index issues

**🇬🇧 English**

React portals allow me to render a component into a different DOM node outside its parent component's DOM hierarchy. I commonly use portals for modals, dialogs, tooltips, and dropdowns because they can avoid CSS overflow or z-index problems.

**🇧🇩 বাংলা**

React portal আমাকে একটি component-কে তার parent component-এর DOM hierarchy-এর বাইরে একটি ভিন্ন DOM node-এ render করতে দেয়। আমি সাধারণত modal, dialog, tooltip, এবং dropdown-এর জন্য portal ব্যবহার করি, কারণ এগুলো CSS overflow বা z-index সমস্যা এড়াতে পারে।

---

## Q60. Explain the lifecycle of a React functional component with hooks.

🔑 **Keywords:**
- mounting
- updating
- unmounting
- useEffect handles side effects at each stage

**🇬🇧 English**

A functional component generally goes through three main stages: mounting, updating, and unmounting.

When React creates the component for the first time, I call it the mounting phase. When its state or props change, React updates and re-renders the component. When React removes the component from the UI, I call it the unmounting phase.

I use useEffect to handle side effects during these stages. For example, I can fetch data after mounting and clean up subscriptions or event listeners when the component unmounts.

**🇧🇩 বাংলা**

একটি functional component সাধারণত তিনটি প্রধান stage-এর মধ্য দিয়ে যায়: mounting, updating, এবং unmounting।

যখন React প্রথমবার component তৈরি করে, আমি সেটাকে mounting phase বলি। যখন এর state বা props পরিবর্তন হয়, React component update এবং re-render করে। আর যখন React component-কে UI থেকে remove করে, আমি সেটাকে unmounting phase বলি।

আমি এই stage-গুলোর সময় side effects handle করার জন্য useEffect ব্যবহার করি। যেমন, আমি mounting-এর পর data fetch করতে পারি এবং component unmount হওয়ার সময় subscription বা event listener clean up করতে পারি।

---

*Prepared for React technical interview practice — English + বাংলা, sentence-aligned for easy speaking practice.* -->