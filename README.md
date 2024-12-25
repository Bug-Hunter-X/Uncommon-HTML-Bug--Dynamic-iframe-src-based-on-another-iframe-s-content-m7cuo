# Uncommon HTML Bug: Dynamic iframe src based on another iframe's content

This repository demonstrates an uncommon bug related to dynamically setting an iframe's `src` attribute based on the content of another iframe.  The issue arises because of the asynchronous nature of iframe loading.  The solution involves using event listeners and asynchronous approaches to manage the data flow.

## Bug Description

The bug occurs when the `src` attribute of an iframe (`iframe2`) is dynamically set based on the content of another iframe (`iframe1`). If the content of `iframe1` is not loaded completely before the assignment, `iframe2` might not load correctly, leading to unexpected behavior or errors.

## Solution

The solution utilizes the `onload` event listener of the first iframe to ensure its content is available before setting the `src` attribute of the second iframe. This guarantees that the content of `iframe1` is used correctly.

## How to Reproduce

1. Clone this repository.
2. Open `bug.html` in a browser.
3. Observe the behavior. You'll see the incorrect behavior demonstrated.
4. Then, open `bugSolution.html`. You'll see the corrected behavior using the solution provided.