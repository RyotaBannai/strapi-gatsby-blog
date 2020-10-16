# Strapi Starter Gatsby Blog

## How to do?

- First Add article on the strapi!
- Second, build the strapi
- Then, run `yarn develop` on frontend(gatsby), which does fetch data from strapi.

Gatsby starter for creating a blog with Strapi.

![screenshot image](/screenshot.png)

This starter allows you to try Strapi with Gatsby with the example of a simple blog. It is fully customizable and due to the fact that it is open source, fully open to contributions. So do not hesitate to add new features and report bugs!

## Features

- 2 Content types: Article, Category
- 2 Created articles
- 3 Created categories
- Responsive design using UIkit
- SEO and social media friendly

Pages:

- "/" to display every articles
- "/article/:id" to display one article
- "/category/:id" display articles depending on the category

## Getting started

The easiest way to try this starter is to run it locally on your computer.

First, you'll need to create your own copy of this starter. You can do so by clicking [the "Use this template" button](https://github.com/strapi/strapi-starter-gatsby-blog/generate) on GitHub, and filling the [form](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template)

### Backend

Create a Strapi project named `backend` using the [blog template](https://github.com/strapi/strapi-template-blog):

```
# Using Yarn
yarn create strapi-app backend --template https://github.com/strapi/strapi-template-blog

# Or using NPM
npx create-strapi-app backend --template https://github.com/strapi/strapi-template-blog
```

The Strapi server will automatically start and import sample seed data.

### Frontend

Leave the Strapi backend running in the background. Open another terminal tab, and make sure you're in the `frontend` directory:

```bash
cd frontend
```

Install dependencies and start the Gatsby server:

```bash
# Using yarn
yarn install
yarn develop

# Using npm
npm install
npm run develop
```

If you want to change the default environment variables, create a `.env` file like this:

```sh
cp .env.example .env
```

The Gatsby server will run here => [http://localhost:3000](http://localhost:3000)

Enjoy this starter!

### Gatsby Memos
#### How to creat Route in Gatsby
- [reference](https://www.gatsbyjs.com/docs/routing/)
- In your site’s `gatsby-node.js` by implementing the API createPages
  - `context Object`: Context data for this page. Passed as props to the component `this.props.pageContext` as well as to the graphql query as `graphql` arguments.
- Gatsby core automatically turns React components in `src/pages` into pages
  - Pages defined in `src/pages`: For example, `contact.js` will be found at `yoursite.com/contact`
  - If `contact.js` is moved to a directory called information, located inside `src/pages`, the page will now be found at `yoursite.com/information/contact`
  - The exception to this rule is any file named `index.js`
- Plugins can also implement createPages and create pages for you
