# 📱 FlipShip Mobile — Logistic-Mobile

The mobile app for **FlipShip**, an intercity cargo shipping service built on top of passenger bus routes. Built with [Expo](https://expo.dev/) and [React Native](https://reactnative.dev/), using file-based routing via [Expo Router](https://expo.github.io/router/).

The app serves multiple user roles — **Customers**, **Drivers**, and **Companies** — covering order placement, package tracking, real-time chat, ratings, and payments.

---

## ✨ Features

- 🔐 **Authentication** — login, registration, secure token storage
- 🔎 **Search & route lookup** — search by single point or two-point (origin/destination)
- 📦 **Package management** — create, update, and view package/order details
- 🚚 **Driver tools** — delivery flow, trip actions, profile
- 🏢 **Company view** — dedicated company dashboard
- 📍 **Maps & tracking** — real-time location and route visualization (Goong Maps / MapLibre / react-native-maps)
- 💬 **In-app chat** — real-time messaging via Socket.IO
- 🔔 **Notifications** — in-app notification center
- ⭐ **Ratings** — rate trips/drivers
- 💳 **Payments** — payment flow and confirmation screens
- 👤 **Profile management** — view and edit user profile
- 🌗 **Light/Dark theme** with themed components

---

## 🛠 Tech Stack

| Category | Technology |
| --- | --- |
| Framework | [Expo](https://expo.dev/) (SDK 52), [React Native](https://reactnative.dev/) 0.76 |
| Routing | [Expo Router](https://expo.github.io/router/) (file-based) |
| Language | TypeScript |
| State management | [Redux Toolkit](https://redux-toolkit.js.org/) |
| Styling | [NativeWind](https://www.nativewind.dev/) (Tailwind CSS for React Native) |
| Forms & validation | [React Hook Form](https://react-hook-form.com/), [Zod](https://zod.dev/) |
| Maps | [react-native-maps](https://github.com/react-native-maps/react-native-maps), [MapLibre](https://maplibre.org/), Goong Maps |
| Real-time | [Socket.IO Client](https://socket.io/) |
| Storage | [Expo Secure Store](https://docs.expo.dev/versions/latest/sdk/securestore/), [AsyncStorage](https://react-native-async-storage.github.io/async-storage/) |
| Testing | [Jest](https://jestjs.io/) + jest-expo |

---

## 📁 Project Structure

```
.
├── app/                          # Expo Router routes (file-based)
│   ├── (auth)/                   # Login, register, onboarding
│   ├── (tabs)/                   # Main bottom-tab navigation (home, order, package, profile)
│   ├── (search)/                 # Route search (single point / two-point)
│   ├── (package)/                # Package create / detail / update
│   ├── (order)/                  # Order detail
│   ├── (delivery)/                # Driver delivery flow
│   ├── (driver)/                   # Driver-specific screens
│   ├── (company)/                   # Company view
│   ├── (chat)/                       # Chat list & conversation
│   ├── (notification)/                # Notification center
│   ├── (payment)/                       # Payment & confirmation
│   ├── (profile)/                        # Profile view & edit
│   ├── (rating)/                          # Ratings
│   └── _layout.tsx, index.tsx, provider.tsx
├── components/                    # Reusable UI components (tabs, chat, driver, themed views, etc.)
├── libs/
│   ├── stores/                    # Redux slices & thunks (auth, order, package, route, trip, rating, chat)
│   ├── services/                  # API service definitions per domain
│   ├── hooks/                     # Custom hooks (useAuthen, useOrder, useChat, ...)
│   ├── context/                   # AuthContext
│   ├── thirdParty/socket/          # Socket.IO setup & event handlers
│   ├── types/                       # Shared TypeScript types
│   └── utils/                        # Auth & shared utilities
├── hooks/                          # Theme & color scheme hooks
├── constants/                       # Color constants
├── assets/                            # Images, icons, fonts
├── app.json                            # Expo app configuration
├── babel.config.js
└── tailwind.config.js
```

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) 18+
- [Expo CLI](https://docs.expo.dev/more/expo-cli/) (`npx expo`)
- Expo Go app or a development build for testing on a device/emulator

### Installation

```bash
git clone https://github.com/Logistic-Flipship/Logistic-Mobile.git
cd Logistic-Mobile
npm install
```

### Environment Variables

Create a `.env` file in the project root with the following variables:

```env
EXPO_PUBLIC_BASE_URL=
EXPO_PUBLIC_GOONG_MAPS_API_KEY=
```

### Run the app

```bash
npx expo start
```

From the Expo CLI output, you can open the app in:

- A [development build](https://docs.expo.dev/develop/development-builds/introduction/)
- An [Android emulator](https://docs.expo.dev/workflow/android-studio-emulator/)
- An [iOS simulator](https://docs.expo.dev/workflow/ios-simulator/)
- [Expo Go](https://expo.dev/go) for quick testing

### Available Scripts

| Command | Action |
| --- | --- |
| `npm run start` | Start the Expo dev server (dev client) |
| `npm run android` | Build and run on Android |
| `npm run ios` | Build and run on iOS |
| `npm run web` | Run in the browser |
| `npm run test` | Run Jest tests in watch mode |
| `npm run lint` | Run Expo lint |
| `npm run reset-project` | Reset to a blank starter project |

---

## 📄 License

This project belongs to FlipShip / Logistic-Flipship.
