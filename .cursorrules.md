# Cursor Rules

## Code Style and Structure

- Write concise, technical TypeScript code using functional and declarative programming patterns.
- Avoid classes; prefer iteration and modularization over code duplication.
- Use descriptive variable names with auxiliary verbs (e.g., `isLoading`, `hasError`).
- Structure files into: exported component, subcomponents, helpers, static content, and types.
- Avoid external libraries unless absolutely necessary for light-weight and performance benefits.
- Use Prettier with specific configuration:
  {
  "endOfLine": "lf",
  "semi": true,
  "singleQuote": false,
  "printWidth": 120,
  "tabWidth": 2,
  "trailingComma": "es5",
  "importOrder": [
  "^(react/(._)$)|^(react$)",
  "^(next/(._)$)|^(next$)",
  "",
  "<THIRD*PARTY_MODULES>",
  "^types$",
      "",
      "^@/app/(.*)$",
  "^@/hooks/(.*)$",
  "^@/components/(._)$",
  "^@/components/ui/(._)$",
  "",
  "^@/styles/(._)$",
  "",
  "^@/types/(.\_)$",
  "^@/layouts/(._)$",
  "^@/lib/(._)$",
  "^@/providers/(._)$",
      "^@/config/(.*)$",
  "^@/utils/(._)$",
  "^@/lib/(._)$",
  "",
  "^[./]"
  ],
  "plugins": ["@ianvs/prettier-plugin-sort-imports", "prettier-plugin-tailwindcss"]
  }

## Creating a component

- You always use `export function` without "default" or named export.
- You always use an object "props" as the first argument of your component, and add type directly in the object.

## Naming Conventions

- Use lowercase with dashes for directories (e.g., `components/auth-wizard`).
- Favor named exports for components.

## Syntax and Formatting

- Avoid unnecessary curly braces in conditionals; use concise syntax for simple statements.
- Write declarative JSX.

## React/Next.js Specific Rules

- Use functional components with TypeScript interfaces.
- Implement responsive design using Tailwind CSS.
- Favor server components and Next.js SSR.
- Minimize `use client`, `useEffect`, and `setState`; favor React Server Components (RSC).
- Avoid using React hooks within server components.

## Vue.js/Nuxt Specific Rules

- Use Vue Composition API for script setups.
- Implement responsive design using Tailwind CSS.
- Optimize Vue framework's performance using VueUse functions.
- Always use TypeScript for all code; prefer interfaces over types.

## Performance Optimization

- Wrap client components in `Suspense` with fallback and create it's Skeleton when possible
- Use dynamic loading for non-critical components.
- Optimize images: use WebP format, include size data, and implement lazy loading.
