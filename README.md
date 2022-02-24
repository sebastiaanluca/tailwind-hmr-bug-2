# Tailwind HMR bug example repository

## Setup

```
composer run-script valet

// Or

composer run-script sail
```

```
npm run hot
```

## Issue

HMR reloads, but Tailwind CSS JIT did not generate the new classes (like as if it didn't scan the files or did not find the new classes). Using already generated classes works fine.

You can test this by running `npm run hot`, opening the project in your browser (depends on your setup), going to e.g. `resources/js/Pages/Admin/Clients/Index.vue`, and changing `bg-blue-600` to `bg-red-600` (or using any unused class). The button background will turn white.
