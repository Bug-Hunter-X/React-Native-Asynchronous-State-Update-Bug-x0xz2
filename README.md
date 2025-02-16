# React Native Asynchronous State Update Bug

This repository demonstrates a common bug in React Native applications involving asynchronous operations and state updates.  The example uses `fetch` to retrieve data, but the state is not updated correctly due to the asynchronous nature of the `fetch` call. The solution shows how to correctly handle this using either `setState` with a callback or `async/await`.

## Bug Description

The bug occurs because the state is updated directly after initiating the `fetch` request, before the request has completed and the data has been retrieved.  This leads to the state not reflecting the actual fetched data.  The component may render with the previous state, or worse, an error may occur.