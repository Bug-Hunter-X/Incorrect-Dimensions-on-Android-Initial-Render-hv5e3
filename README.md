# React Native Dimensions API - Initial Dimensions Issue on Android

This repository demonstrates a common issue encountered when using the `Dimensions` API in React Native on Android. The problem is that `Dimensions.get('window')` can return inaccurate dimensions during the initial render, causing layout inconsistencies.

The `DimensionsBug.js` file shows the problem: using the dimensions immediately to render UI elements leads to wrong measurements.

The solution, in `DimensionsBugSolution.js`, uses `Dimensions.addEventListener` to get notified when the dimensions change and only update after the correct dimensions are available.