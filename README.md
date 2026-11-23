# 🍳 Recipe Book

A responsive recipe browsing app built with **Vue 3 + TypeScript**. Search and filter recipes, view step-by-step instructions, log in, and save your favourites to a personal bookmarks page. Includes light and dark modes.

<!-- Add a live demo link and 2–3 screenshots here, e.g. ![Home](docs/screenshots/home.png) -->

---

## ✨ Features

- **Browse recipes** fetched from the [DummyJSON Recipes API](https://dummyjson.com/docs/recipes)
- **Live search** by recipe name, plus a **cuisine filter** built from the loaded data
- **Recipe details**: prep and cook time, servings, rating, ingredients and numbered instructions
- **Authentication** with DummyJSON's login endpoint, storing the token for the session
- **Protected routes**: the Bookmarks page needs a login (Vue Router navigation guard)
- **Bookmarks / favourites** managed with Pinia and saved in `localStorage`
- **Dark mode** toggle that remembers your preference
- Glassmorphism navbar with active-route highlighting; responsive Tailwind CSS layout

## 🛠 Tech Stack

| Category | Tools |
|---|---|
| Framework | Vue 3 (Composition API, `<script setup>`) |
| Language | TypeScript |
| State management | Pinia |
| Routing | Vue Router (lazy-loaded routes, auth guard) |
| Styling | Tailwind CSS, Heroicons |
| Build tool | Vite |
| Code quality | ESLint, Oxlint, Prettier, `vue-tsc` type checking |

## 🗺 Pages

| Route | Page | Auth required |
|---|---|---|
| `/` | Home: search, filter and recipe grid | – |
| `/recipe/:id` | Recipe details | – |
| `/login` | Login | – |
| `/bookmarks` | Saved recipes | ✅ |

## 📁 Project Structure

```text
src/
├── api/recipes.ts          # API calls to DummyJSON
├── components/             # NavBar, RecipeCard
├── composables/useTheme.ts # Dark/light mode logic
├── router/index.ts         # Routes + auth navigation guard
├── stores/                 # Pinia stores: auth, favorites
├── types/Recipe.ts         # Recipe TypeScript interface
└── views/                  # Home, RecipeDetail, Bookmarks, Login
```

## 🚀 Getting Started

**Prerequisites:** Node.js 20.19+ or 22.12+

```bash
git clone https://github.com/amandi-konara/Recipe-Book.git
cd Recipe-Book
npm install
npm run dev
```

Then open http://localhost:5173.

**Demo login:** DummyJSON provides test users, for example username `emilys` and password `emilyspass` (see the [DummyJSON users list](https://dummyjson.com/users)).

### Other scripts

```bash
npm run build     # type-check + production build
npm run preview   # preview the production build
npm run lint      # Oxlint + ESLint
npm run format    # Prettier
```

## 💡 What I Learned

- Structuring a Vue 3 app with the Composition API and TypeScript interfaces
- Global state with Pinia and persisting it to `localStorage`
- Protecting routes with Vue Router navigation guards
- Building reusable components and a theme composable

## 🔮 Future Improvements

- [ ] Sync bookmarks to a backend so they work across devices
- [ ] Filter by meal type, difficulty and cooking time
- [ ] Loading skeletons and better error states
- [ ] Unit tests with Vitest

---

Built by [Amandi Konara](https://github.com/amandi-konara)
