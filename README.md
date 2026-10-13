<!-- @format -->

# Vello

Mobile app for **Vello**, a single-brand women's fashion store: everyday urban and casual clothing and shoes for women.

The store has one physical location, so the app supports **pickup only** with **prepayment** (bank card or SBP). Market — Russia, currency — RUB, UI language — Russian (architecture ready for English).

## Features (MVP)

- **Home** — popular products, sale, categories, recommendations, store info with map
- **Catalog & Search** — categories, filters (color, price, availability, on sale), sorting
- **Product Details** — color-bound image gallery, color and size selection, stock status, reviews, size guide
- **Favorites** — saved products with back-in-stock notifications
- **Cart & Checkout** — guest cart, merged into the account cart on login; single-screen checkout
- **Orders** — order history, statuses, cancellation, reviews for received items
- **Account** — registration with email verification, login, password reset, profile editing, account deletion
- **Notifications** — in-app order status and back-in-stock updates
- **Settings** — theme (System / Light / Dark), language, notification preferences

## Tech stack

| Area         | Choice                                                                              |
| ------------ | ----------------------------------------------------------------------------------- |
| Framework    | [Expo](https://expo.dev) SDK 57, React Native 0.86, React 19.2                      |
| Language     | TypeScript (strict)                                                                 |
| Navigation   | [Expo Router](https://docs.expo.dev/router/introduction) (file-based, typed routes) |
| Compiler     | React Compiler                                                                      |
| Animations   | Reanimated 4, Gesture Handler                                                       |
| Images       | expo-image                                                                          |
| Localization | i18next, react-i18next, expo-localization                                           |
| Architecture | [Feature-Sliced Design](https://fsd.how)                                            |

## Project structure

The code follows [Feature-Sliced Design](https://fsd.how).

```
src/
├── app/        # Expo Router routes — thin files that re-export pages
├── _app/       # FSD App layer: entrypoint, providers, styles, store, analytics
├── pages/      # Screens, one slice per screen
└── shared/     # Business-agnostic code: api, ui, lib, config, routes, i18n
```

## Getting started

```bash
npm install
npx expo start
```

Then open the app in [Expo Go](https://expo.dev/go), an Android emulator, an iOS simulator, or a [development build](https://docs.expo.dev/develop/development-builds/introduction/).

## Scripts

```bash
npm run start      # start the dev server
npm run android    # open on Android
npm run ios        # open on iOS
npm run web        # open in the browser
npm run lint       # lint
npx tsc --noEmit   # typecheck
```

Add dependencies with `npx expo install <package>` so versions stay compatible with the Expo SDK.
