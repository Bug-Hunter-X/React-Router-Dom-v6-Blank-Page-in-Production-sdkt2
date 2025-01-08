# React Router Dom v6 Blank Page in Production

This repository demonstrates a common issue with React Router Dom v6 where the application renders a blank page in a production environment.  The application works as expected in development, but when built for production, no components are rendered.

The issue arises from a mismatch between the React Router configuration and how the application is built and served.  The solution involves ensuring the application's base URL correctly reflects the deployment path.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start` (to see the working development version).
4. Run `npm run build`.
5. Serve the `build` directory using a production-ready web server (Nginx, Apache, etc.).
6. Observe that the production build renders a blank page.  

## Solution

The solution involves correctly configuring the `BrowserRouter`'s `basename` prop to match the production deployment path.   This can often be done by checking environment variables to determine where the app is served.