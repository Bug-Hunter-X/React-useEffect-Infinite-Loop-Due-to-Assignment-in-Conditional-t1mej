# React useEffect Infinite Loop Bug

This repository demonstrates a common yet subtle error in React's `useEffect` hook: using an assignment (`=`) instead of a comparison (`===`) in the conditional statement. This leads to an infinite loop because the condition is always true, causing the effect to run repeatedly.

## Bug Description
The `useEffect` hook's dependency array includes `count`. The conditional statement inside `useEffect` incorrectly uses `count = 0`, which assigns 0 to `count` instead of comparing if `count` equals 0.  This assignment triggers a re-render, causing the effect to run again and again.

## Bug Solution
The solution involves using the correct comparison operator (`===`) to check if `count` is equal to 0.