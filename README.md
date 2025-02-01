# React Router v6 Catch-all Route Issue

This repository demonstrates a common issue encountered when using the catch-all route (`/*`) in React Router v6.  The catch-all route unintentionally intercepts all routes, preventing other routes from working correctly.

## Problem

The provided code uses `react-router-dom` v6. The `/*` route meant to handle 404 errors is always matched and overrides other routes in the app, even if other routes should match before it. This causes the application to always show the 404 page instead of other specific routes.

## Solution

The solution involves re-ordering routes.  The catch-all route (`/*`) should always be placed at the end of the routes list to ensure it only matches if no other routes match first.