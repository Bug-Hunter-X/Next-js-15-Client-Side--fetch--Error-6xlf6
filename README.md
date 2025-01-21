# Next.js 15 Client-Side Fetch Error

This repository demonstrates a common error encountered in Next.js 15 applications when using `fetch` within client components. The `fetch` call in `pages/about.js` attempts to retrieve data from an API route, but fails because it's executed on the client-side before the component has mounted fully, leading to issues with the `await` keyword. 

**Steps to Reproduce:**

1. Clone this repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Navigate to `/about`.
5. Observe the error in your browser's console.

**Solution:**

The provided solution demonstrates a proper way to handle client-side `fetch` requests in Next.js, using either the `useEffect` hook or other suitable approaches to ensure the `fetch` call occurs after the component has mounted.