# Nx and Angular Playground

## What

A Movies DB demo app based on the amazing [The Movie DB](https://www.themoviedb.org/) to play with the newest [Nx](https://nx.dev) and [Angular](https://angular.io) _'best practices'_ like [Standalone Components](https://angular.io/guide/standalone-components), `Inject()` and plenty more. While following Semantic HTML and newest CSS solutions.

And providing the best [VSCode settings](.vscode/settings.json), [VSCode extensions](.vscode/extensions.json) and [ESLint](.eslintrc.json) settings.

Using tools like: [Cypress](https://cypress.io), [MSWjs](https://mswjs.io), [Zod](https://zod.dev/?id=introduction), [Testing Library Angular](https://testing-library.com/docs/angular-testing-library/intro/) and others.

Trying to provide a good base for both a learning and as a starter repository.

**N.B**

- We Set the `"target": "ES2022"`, which means the `"useDefineForClassFields": true` is automatically set to `true`. And Angular will not set it to `false`.
  We do this to force the use of `inject()` instead of using the `constructor` and be [future proof](https://angular.schule/blog/2022-11-use-define-for-class-fields) and avoid future breaking changes.

## Why

## Screenshots

[TODO]

## Tech / Tools used

- [Nx](https://nx.dev)
- [Angular](https://angular.io)
- [Cypress](https://cypress.io)
  - [Cypress Testing Library](https://github.com/testing-library/cypress-testing-library) - for end to end test assertions
- [Jest](https://jestjs.io) - for running unit tests
  - [Testing Library Angular](https://testing-library.com/docs/angular-testing-library/intro/) - for unit test assertions
- [MSWjs](https://mswjs.io)
- [Zod](https://zod.dev/?id=introduction)

## Setup

```
# ------------------------------------------------------------------
# Enable pnpm
# ------------------------------------------------------------------
❯ corepack enable

# ------------------------------------------------------------------
# Install dependencies
# ------------------------------------------------------------------
❯ pnpm install

```

## Run

```
# ------------------------------------------------------------------
# Start dev server with MSW mocking at localhost:4200
# ------------------------------------------------------------------
❯ pnpm start:msw movie-db

# OR

❯ nx mock movie-db

# ------------------------------------------------------------------
# OR RUN WITH LIVE DATA, but you first have to add your TMDB BEARER token
# to `apps/movie-db/.env.serve`
# See: https://developers.themoviedb.org/3/getting-started/authentication#bearer-token
# ------------------------------------------------------------------

❯ nx serve movie-db
```

### E2E

```
❯ pnpm e2e:msw

# OR

❯ nx e2e movie-db-e2e [--watch --browser=chrome]
```

## Credits / Resources / Thanks / Shout-outs

- Data provided by [The Movie DB](https://www.themoviedb.org)
- [Netanel Basal](https://netbasal.medium.com/)
  - Amazing (short) blogposts
  - Creator of [ngneat](https://github.com/ngneat) with great tools like: [Elf](ngneat.github.io/elf/), [Transloco](ngneat.github.io/transloco/), [until-destroy](https://github.com/ngneat/until-destroy) and plenty more.
- [Tim Deschryver](https://timdeschryver.dev/blog/getting-the-most-value-out-of-your-angular-component-tests)
  - Great blogposts about Angular, Testing, and plenty more.
- [Kent C. Dodds](https://kentcdodds.com/blog?q=testing)
  - Creator of Testing Library
  - Testing Jedi
- And of course the amazing teams and community of [@Angular](https://www.angular.io) and [Nx](https://nx.dev)!
- [Movies App](https://tastejs.com/movies/) - Amazing sample applications for different frameworks.
- [Nuxt Movies](https://github.com/nuxt/movies) - TMDB example app with Nuxt and VueJs
- [Versatile Angular - Younes Jaaidi](https://marmicode.io/blog/versatile-angular) - Angular (SFC) with Vite
- [Analogjs](https://github.com/analogjs/analog) - Amazing all in one framework for Angular by Brandon Roberts. Using Vite
- [Unnecessary VSCode Extensions](https://javascript.plainenglish.io/unnecessary-vscode-extensions-e72cb637f1cf) - See [VSCode Extension Settings](/.vscode/extensions.json) and [VSCode workspace settings](.vscode/settings.json)

## Things I would like to add

- [ ] Do not use image url's while testing (add images to mock assets)
- [ ] [@ngrx/component-store](https://ngrx.io/guide/component-store) or [@ngneat/elf](https://ngneat.github.io/elf/)
- [ ] [Playwright tests](https://playwright.dev/)
- [ ] New App with [GraphQL Yoga](https://the-guild.dev/graphql/yoga-server) and TypedDocumentNode
- [ ] Separate branches / forks (Or.. since it is a mono-repo in the same repo) for:
  - [ ] Build with ESBuild
  - [ ] Vite
  - [ ] [Rome](https://rome.tools/)
- [ ] Create an app with [SvelteKit](https://kit.svelte.dev/)
