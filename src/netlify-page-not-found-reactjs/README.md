# Page Not Found Error on Netlify Reactjs React Router


### How did the error occur?

React Router handles routing on the client-side (browser) so when you visit the non-root page (e.g. `https://yoursite.netlify.com/login`), Netlify (server-side) does not know how to handle the route.

(As your routes are set up in the root level).

And the error occurring on Netlify when you go to `https://<netlify domain>/route directly`.

![Page not found](https://res.cloudinary.com/practicaldev/image/fetch/s--gLNPgLKP--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://rajeshroyal.com/wp-content/uploads/2020/06/netlify-page-not-found-error-react-router-after-deploy.png)

### Fixing
So to fix the issue, we need to create a file named `_redirects` to the root of our site **[public folder of App]** with the following content.

`/* /index.html 200`

![Fixing](https://res.cloudinary.com/practicaldev/image/fetch/s--kNaXAE66--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://rajeshroyal.com/wp-content/uploads/2020/06/redirects-file-content-netlify-page-not-found-spa-error-solved.jpg)



Source: [Page Not Found Error on Netlify Reactjs](https://dev.to/rajeshroyal/page-not-found-error-on-netlify-reactjs-react-router-solved-43oa)
