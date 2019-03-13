## Quickstart on local

``` bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev
```

Tips:
- Make sure you are running on http://localhost:3000. If not sanity and snipcart will fail due to CORS origins.
- Vue.js requires a recent Node version so if it fails on startup you might need an upgrade.

## Using your own sanity.io data

- Install Sanity CLI: `npm install -g @sanity/cli`.
- Initialize a new project: `sanity init`.
- Select the e-commerce schema.
- Start local Sanity studio: `sanity start`.
- From `sanity.json` in the root directory of where your Sanity project is located, copy the `projectId` and `dataset` values. 
- In `sanity.js` in the root directory of this app, change the `projectId` and `dataset` values to the ones you copied above.
- Remember to add CORS manage.sanity.io (ex. http://localhost:3000 to run locally).
- Use `sanity deploy` to share your editor with others.
- [Sanity homepage](https://sanity.io)

## Install your own snipcart
- Go to http://snipcart.com
- Register and copy your API-key from Snipcart
- In `nuxt.config.js` paste it into `data-api-key` 
- Remember to add your domain/url in your Snicart settings (https://app.snipcart.com/dashboard/account/domains)

## Build production server or static project
``` bash
# build for production and launch server
$ npm run build
$ npm start

# generate static project
$ npm run generate
```

If you want to host this on Netlify, as a static build, follow [these steps](https://www.sanity.io/blog/tutorial-host-your-sanity-based-next-js-project-on-netlify#3-deploy-your-blog-on-netlify) while switching out the `generate` command above and changing the output directory from `out` to `dist`. Note: Nuxt is intended to run as a universal/isomorphic app and will make calls to the Sanity CDN.

The queries are by default limited to 100 items. This project is just an example, but
it is possible to expand it with pagination or forever-scroll. To get more items, 
just add ex [0..1000] to the end of your query ([more details](https://www.sanity.io/docs/data-store/query-cheat-sheet#slice-operations)).