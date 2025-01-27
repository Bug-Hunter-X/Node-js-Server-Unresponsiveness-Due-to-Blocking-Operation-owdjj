# Node.js Server Unresponsiveness Bug

This repository demonstrates a common Node.js issue: server unresponsiveness caused by a long-running synchronous operation within the request handler.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides a corrected version using asynchronous operations to prevent blocking.

**Problem:** The synchronous loop in `bug.js` blocks the event loop, making the server unresponsive to new requests until the loop completes. This can lead to poor performance and even crashes under heavy load.

**Solution:**  The `bugSolution.js` demonstrates the solution using asynchronous operations (e.g., `setTimeout` in this simplified example, or promises/async/await for more complex scenarios) to allow other events to be processed while the long operation runs in the background.