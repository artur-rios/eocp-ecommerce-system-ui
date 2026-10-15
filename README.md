# E-commerce System UI

> [!IMPORTANT]
> **This repository is archived and no longer receives updates.** It is kept as a
> record of an academic project. Issues and pull requests are not accepted, and the
> dependencies are outdated and should not be used in production.

User interface of the e-commerce system built as the end-of-course project for the
Bachelor's Degree in Information Systems at the University of Mogi das Cruzes (UMC).

## Purpose

This repository holds the Angular front-end of a multi-store e-commerce platform.
Customers use it to browse products, fill a cart and place orders. Store owners and
administrators use it to manage stores, products, orders and users, and to follow
revenue in the management dashboards. All data comes from the
[API](https://github.com/artur-rios/eocp-ecommerce-system-api).

## The e-commerce system

| Repository | Purpose |
|------------|---------|
| [eocp-ecommerce-system-api](https://github.com/artur-rios/eocp-ecommerce-system-api) | Back-end REST API |
| **eocp-ecommerce-system-ui** (this one) | Angular front-end |
| [eocp-ecommerce-system-email-templates](https://github.com/artur-rios/eocp-ecommerce-system-email-templates) | Transactional e-mail templates |

## Technology stack

- Angular 16 and Angular Material
- Bootstrap 4 and ngx-bootstrap
- ngx-mask for input masks
- [ViaCEP](https://viacep.com.br) for Brazilian postal code lookup
- Karma and Jasmine (unit tests), Protractor (end-to-end tests)

The project was created with Angular 10 and later upgraded, one major version at a
time, to Angular 16.

## Features

- **Authentication**: login, password reset request and new password registration
- **Store front**: product list and detail, cart, shipping, payment method, order
  conclusion and order detail
- **Registration**: user, address, telephone, password, store and product
  registration, product update, user profile and order history
- **Management**: dashboard, store profile and tables of orders, products, revenue,
  stores and users

## Project structure

```
docs/                    Front-end modules and components map (XMind)
src/app/
  core/                  Guards, HTTP interceptors, loader and services
  pages/
    authentication/      Login and password recovery
    store/               Shopping flow
    registration/        Account, store and product forms
    management/          Dashboards and management tables
  shared/                Navbar, footer, modals, table and cart components
  utils/                 Enums, lists, models, pipes and validators
src/environments/        API and ViaCEP URLs
```

## Running locally

Requires Node.js and the Angular CLI version used by the project.

```bash
npm install
```

```bash
npm start
```

The app opens at `http://localhost:4200/` and expects the API at
`http://localhost:8080/api`. Change `API_URL` in `src/environments/environment.ts`
to point it elsewhere.

Other scripts: `npm run build`, `npm test`, `npm run lint` and `npm run e2e`.

## Branches

- `main`: final state of the code, upgraded to Angular 16 after the delivery.
- `end-of-course-version`: the version delivered for the end-of-course project, before the later changes on `main`.

## License

Licensed under the [Artur Rios Attribution License](LICENSE).
