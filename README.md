# Expo Image Component: Silent Failure on Invalid URI

This repository demonstrates a subtle bug in Expo's `Image` component where it fails silently when provided with an invalid or inaccessible image URI. The component renders nothing or shows a broken image icon without providing a helpful error message in the console.

## Problem

When using the `Image` component with a URI that's incorrect, missing, or points to a resource the app can't access, the error handling is not robust.  There's no clear indication in the console or on the UI about why the image isn't loading.

## Solution

The solution involves implementing a more robust error-handling mechanism using a combination of techniques including checking the URI before loading, monitoring the image loading status with the `onLoad` and `onError` callbacks, and providing fallback mechanisms.