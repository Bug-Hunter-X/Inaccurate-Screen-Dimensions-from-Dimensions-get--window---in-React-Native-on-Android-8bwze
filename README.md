# React Native Dimensions Bug: Inaccurate Screen Dimensions on Android

This repository demonstrates a common issue encountered when using the `Dimensions` API in React Native to obtain screen dimensions, specifically on Android. The `Dimensions.get('window')` method may return incorrect values, particularly after orientation changes or during initial app rendering. This can result in layout issues where components are misaligned or clipped.

The `DimensionsBug.js` file showcases the incorrect implementation, and `DimensionsBugSolution.js` demonstrates a robust solution using the `useEffect` hook and state to reliably capture updated dimensions.

## Problem:
The `Dimensions` API's asynchronous nature and occasional delays in updating can lead to dimensions being captured before they accurately reflect the screen's size, especially after orientation changes.

## Solution:
Using the `useEffect` hook, we can ensure that dimensions are fetched and updated correctly after the component mounts and when the window dimensions change.  This provides a more accurate and reliable way to use the `Dimensions` API.