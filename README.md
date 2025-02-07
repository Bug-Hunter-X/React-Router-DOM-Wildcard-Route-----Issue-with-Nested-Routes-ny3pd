# React Router DOM Wildcard Route Issue

This repository demonstrates a common issue encountered when using wildcard routes ("* ") in React Router DOM, specifically how it conflicts with nested routes. The wildcard route unintentionally overrides other routes, leading to incorrect rendering. The solution showcases a workaround to solve the problem.

## Problem
The wildcard route in `App.js` is designed to catch any unmatched routes. However, it also intercepts requests meant for nested routes, even if a specific route is available. This is because the wildcard route is a catch-all, taking precedence over other routes.

## Solution
The solution in `AppSolution.js` moves the wildcard route to be the last route in the route definitions. This ensures that the wildcard route only takes effect when all specific routes have been checked and none match the URL.  By correctly ordering your routes, React Router DOM can properly resolve paths and render the correct components.