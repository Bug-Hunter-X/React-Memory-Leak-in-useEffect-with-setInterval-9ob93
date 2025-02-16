# React Memory Leak Bug

This repository demonstrates a common bug in React applications involving memory leaks caused by improper use of `setInterval` within the `useEffect` hook.  The `bug.js` file contains the faulty code, while `bugSolution.js` provides the corrected implementation.

**Problem:**

The `setInterval` function inside the `useEffect` hook in `bug.js` is not cleared when the component unmounts. This leads to the interval continuing to run, consuming resources and causing a memory leak.

**Solution:**

The `bugSolution.js` file demonstrates the proper way to handle `setInterval` within `useEffect` by clearing the interval using `clearInterval` before the component unmounts.  This ensures that resources are released when the component is no longer needed.