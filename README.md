# React 19 useEffect Empty Dependency Array Issue

This repository demonstrates a common misunderstanding of the `useEffect` hook in React 19 (and earlier versions).  The example shows how using an empty dependency array `[]` leads to the effect running only once on component mount, preventing expected updates.

## Problem
The provided code intends to log the `count` value every time it changes. However, due to the empty dependency array, the `console.log` statement only executes once when the component initially renders. Subsequent changes to the `count` state will not trigger the effect.

## Solution
To fix this, include `count` in the dependency array, causing the effect to re-run whenever `count` changes.