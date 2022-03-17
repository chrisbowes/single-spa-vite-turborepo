# Single-Spa Vite & Turborepo starter

This is a barebones starter for a monorepo of single-spas using turborepo to manage taskrunning and monorepo management, with Vite implemented to run dev and build workflows.

## What's inside?

This turborepo uses [Yarn](https://classic.yarnpkg.com/lang/en/) as a package manager. It is originally bbased on the Turborepo starter package available [here](https://github.com/vercel/turborepo/tree/main/examples/basic) It includes the following packages/apps:

### Apps and Packages

- `react-app-1`: a react application wrapped as a single-spa app
- `react-app-2`: a duplicate react application wrapped as a single-spa app
- `vue-app-1`: a vue application wrapped as a single-spa-app
- `root-config`: a single-spa root-config for rendering and testing single-spa's in local development. Based on: https://github.com/joeldenning/vite-single-spa-root-config
- `config`: `eslint` configurations (includes `eslint-config-next` and `eslint-config-prettier`)
- `tsconfig`: `tsconfig.json`s used throughout the monorepo

Each package/app is 100% [TypeScript](https://www.typescriptlang.org/). With the exception of the root-config. This is pure JS due to currently unresolved issues rendering vite es6 modules in a 100% typescript environment

### Utilities

This turborepo has some additional tools already setup for you:

- [TypeScript](https://www.typescriptlang.org/) for static type checking
- [ESLint](https://eslint.org/) for code linting
- [Prettier](https://prettier.io) for code formatting

## Setup

Clone and run `yarn` to install deps

### Build

To build all apps and packages, run the following command:

```
yarn run build
```

### Develop

To develop all apps and packages, run the following command:

```
yarn run dev
```

### Remote Caching

Turborepo can use a technique known as [Remote Caching (Beta)](https://turborepo.org/docs/features/remote-caching) to share cache artifacts across machines, enabling you to share build caches with your team and CI/CD pipelines.

By default, Turborepo will cache locally. To enable Remote Caching (Beta) you will need an account with Vercel. If you don't have an account you can [create one](https://vercel.com/signup), then enter the following commands:

```
npx turbo login
```

This will authenticate the Turborepo CLI with your [Vercel account](https://vercel.com/docs/concepts/personal-accounts/overview).

Next, you can link your Turborepo to your Remote Cache by running the following command from the root of your turborepo:

```
npx turbo link
```

## Useful Links

Learn more about the power of Turborepo:

- [Pipelines](https://turborepo.org/docs/features/pipelines)
- [Caching](https://turborepo.org/docs/features/caching)
- [Remote Caching (Beta)](https://turborepo.org/docs/features/remote-caching)
- [Scoped Tasks](https://turborepo.org/docs/features/scopes)
- [Configuration Options](https://turborepo.org/docs/reference/configuration)
- [CLI Usage](https://turborepo.org/docs/reference/command-line-reference)
