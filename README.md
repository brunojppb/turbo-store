# Turbo Store

This is a TypeScript monorepo created to demo [Turborepo](https://turborepo.org/),
a high-performance build system for JavaScript and typeScript codebases.

## What's inside?

This turborepo uses [pnpm](https://pnpm.io) as a package manager. It includes the following packages/apps:

### Apps and Packages

- `shop`: a [Next.js](https://nextjs.org) app as a customer-facing online shop
- `admin`: another [Next.js](https://nextjs.org) app as a back office application
- `ui`: a React component library shared by both `shop` and `admin` applications
- `eslint-config-custom`: `eslint` configurations (includes `eslint-config-next` and `eslint-config-prettier`)
- `tsconfig`: `tsconfig.json`s used throughout the monorepo

Each package/app is 100% [TypeScript](https://www.typescriptlang.org/).

### Utilities

This turborepo has some additional tools already setup for you:

- [TypeScript](https://www.typescriptlang.org/) for static type checking
- [ESLint](https://eslint.org/) for code linting
- [Prettier](https://prettier.io) for code formatting

### Build

To build all apps and packages, run the following command:

```
cd turbo-store
pnpm build
```

### Develop

To develop all apps and packages, run the following command:

```
cd turbo-store
pnpm dev
```

### Remote Caching

Turborepo can use a technique known as [Remote Caching](https://turborepo.org/docs/core-concepts/remote-caching) to share cache artifacts across machines, enabling you to share build caches with your team and CI/CD pipelines.

By default, Turborepo will cache locally. To enable Remote Caching you will need an account with Vercel. If you don't have an account you can [create one](https://vercel.com/signup), then enter the following commands:

```
cd turbo-store
pnpm dlx turbo login
```

This will authenticate the Turborepo CLI with your [Vercel account](https://vercel.com/docs/concepts/personal-accounts/overview).

Next, you can link your Turborepo to your Remote Cache by running the following command from the root of your turborepo:

```
pnpm dlx turbo link
```
### Remote caching with a self-hosted cache server

If you are not using Vercel's own infrastructure, you can self-host your own turborepo cache server. I've created an open-source version
of it and it's available here: https://github.com/brunojppb/turbo-racer

> **Note**  
> This project was created based on the templates provided by the awesome Turborepo folks [here](https://github.com/vercel/turborepo)

## Useful Links

Learn more about the power of Turborepo:

- [Pipelines](https://turborepo.org/docs/core-concepts/pipelines)
- [Caching](https://turborepo.org/docs/core-concepts/caching)
- [Remote Caching](https://turborepo.org/docs/core-concepts/remote-caching)
- [Scoped Tasks](https://turborepo.org/docs/core-concepts/scopes)
- [Configuration Options](https://turborepo.org/docs/reference/configuration)
- [CLI Usage](https://turborepo.org/docs/reference/command-line-reference)
