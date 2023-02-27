# Angular Clean Architecture Template

This repository is intended to serve as a template for developing an Angular project with clean architecture.

This architecture allows you to keep the business logic separate, so you can use this idea for use with other frameworks just by extracting the "lib" folder from it.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Dependencies

This projects is built with `pnpm` and is configured using this depedencies to ensure good practices:

- jest
- eslint
- husky
- commit-lint

## `pnpm run` commands

```
start: "ng serve",
build: "ng build",
watch: "ng build --watch --configuration development",
test: "ng lint && jest",
test:watch: "ng lint && jest --watch",
tests:functional: "ng lint && jest --coverage=false --testTimeout=60000 tests/functional --maxWorkers=50%",
tests:integration: "ng lint && jest --coverage=false tests/integration --maxWorkers=50%",
tests:unit: "ng lint && IS_UNIT=true jest --coverage=false tests/unit --maxWorkers=50%",
tests:unit:coverage: "ng lint && IS_UNIT=true jest --coverage=true --ci tests/unit",
lint: "ng lint",
prepare: "husky install"
```
