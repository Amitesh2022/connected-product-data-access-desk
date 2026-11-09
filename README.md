# Connected Product Data Access Desk

## One-sentence benefit

Give connected-product users practical control over generated data with accountable access workflows.

## Live demo

[Watch the workflow](docs/demo.webm).

## Screenshots

![Connected product data access dashboard](docs/screenshot.png)

## Main features

- Search and sort data requests across products and organisations.
- Create a new access request through the Java service.
- Advance draft and review cases toward approval.
- View delivery guidance on a separate route.
- Handle loading, empty, error and success states responsively.

## Technology used

Vue 3, TypeScript, Pinia, Vue Router, Vite, Spring Boot and Java 21.

## Installation instructions

Install Node.js 22 and Java 21. Run `npm install`, then start the backend with `cd backend && mvn spring-boot:run`. In another terminal run `npm run dev`.

## Commercial licensing/contact

Commercial licensing and integration support are available. Use the repository contact options to discuss deployment.

## Business problem and users

Connected-product users, manufacturers, data holders and SMEs need to coordinate machine-readable access, third-party sharing and fair contract terms.

## Key workflows

Find a product dataset, add an access request, review its owner and priority, advance delivery status and consult the guidance page.

## Vue framework highlights

Pinia provides reactive API state and computed metrics, Vue Router separates operational and guidance views, and Vue templates expose accessible live updates.

## Java backend highlights

Spring Boot supplies validated list, search, create and update APIs, consistent error responses, a health endpoint and tested service rules.

## Architecture and state flow

Vue actions call `/api/items` through the development proxy. The Java controller validates requests, the service owns workflow state and responses update the Pinia store.

## Accessibility and responsive behaviour

The interface uses labelled search, semantic navigation, keyboard controls, readable status text and layouts that collapse cleanly on small screens.

## Verification commands

Run `npm test`, `npm run build`, `cd backend && mvn test` and `cd backend && mvn package`.

## Structure

`src` holds the Vue routes and store, `backend` holds the Java API, and `docs` holds inspected media.

## Tradeoffs

The sample uses in-memory records for a fast local setup. A production service should add identity, persistence and partner data exchange.

## Roadmap

Add dataset catalogues, trade-secret safeguards, export monitoring and third-party authorisations.
