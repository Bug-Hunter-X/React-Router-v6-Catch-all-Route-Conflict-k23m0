# React Router v6 Catch-all Route Conflict

This repository demonstrates a common issue in React Router v6 involving catch-all routes ('/*').  When a catch-all route is placed before other routes, it can unexpectedly match URLs that should be handled by other, more specific routes, leading to incorrect rendering or unexpected behavior.

The `App.js` file shows the problematic code, while `AppSolution.js` provides the corrected version.

## Problem

The issue arises from the order of routes defined within the `Routes` component.  If a catch-all route (`/*`) is defined before other routes, it will always match, regardless of whether other routes could have matched more specifically.

## Solution

The solution is to place the catch-all route at the end of the route definitions within the `Routes` component.  This ensures that it only matches when no other route matches the URL.