# React UseEffect setInterval Memory Leak
This repository demonstrates a common error in React applications involving memory leaks caused by the improper use of `setInterval` within the `useEffect` hook.  The `bug.js` file shows the flawed code, and `bugSolution.js` provides the corrected version.

**Problem:** The initial implementation fails to clear the interval when the component unmounts, leading to a memory leak.  This is a frequent issue that can cause performance degradation over time, especially with multiple components using `setInterval` without proper cleanup.

**Solution:** The corrected version uses a cleanup function within the `useEffect` hook's return value.  This ensures that `clearInterval` is called when the component unmounts or when the dependency array changes, preventing the memory leak. 

This example highlights the importance of careful resource management in React to maintain application stability and prevent performance problems.