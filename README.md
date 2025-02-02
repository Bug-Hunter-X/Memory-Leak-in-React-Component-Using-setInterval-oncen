# React setInterval Memory Leak

This repository demonstrates a common error in React components: using `setInterval` without proper cleanup.  This leads to memory leaks because the interval continues to run even after the component is unmounted.

The `bug.js` file contains the faulty code. The `bugSolution.js` file provides the corrected version.

**How to reproduce:**
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the count increasing in the component. Unmounting the component will not stop the counter.

**Solution:**
The solution involves using the cleanup function provided by the `useEffect` hook to stop the interval before the component is unmounted.