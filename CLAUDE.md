# Troefcall Rulebook PWA

A Vite + React + TypeScript progressive web app that teaches **Troefcall**, a Dutch 4-player/2-team trick-taking card game, with a playful felt-table visual theme. It has two pillars: an illustrated rulebook (each core gameplay topic gets 3 progressively-difficult worked examples) and a glossary/reference for terminology, sanctions, and tournament structure.

## Milestones

1. ✅ Scaffold: Vite+React+TS, vite-plugin-pwa, router, framer-motion, felt/wood/gold tokens applied.
2. ✅ Visual primitives: `PlayingCard`, `FeltSurface`, `WoodPanel`, `ScoreBadge`, `SuitIcon` — verified on a throwaway kitchen-sink route.
3. ✅ Animation layer: Framer Motion flip + `layoutId` deal/trick-collect animations; respects `prefers-reduced-motion`.
4. ✅ Content engine + types + vitest tests for trick resolution logic (`src/engine/trickResolution.ts`).
5. ✅ Rulebook: Setup & Dealing (+ Caller) page with 3 authored examples (`RuleTopicLayout`/`ExampleTabs`/`ExampleStepper`).
6. ✅ Rulebook: Trick-taking and Winning a Hand pages, same pattern.
7. ⬜ Free-form interactive trick demo using the engine (click-to-play, illegal follow-suit blocked).
8. ⬜ Glossary: full Begrippenlijst + sanctions table + tournament structure, search/category filter, bidirectional links to/from rulebook pages.
9. ⬜ Home page + nav polish, mobile (375px) and tablet (1024px) check.
10. ⬜ PWA finalization: manifest icons (incl. maskable), offline test via `build && preview`, Lighthouse PWA audit.
11. ⬜ Content QA: re-check every authored example against the source rules, especially the kap tap-out-vs-forced-continue and baunie-concession edge cases.

Milestones 1–6 are pushed to `claude/troefcall-rules-pwa-wa68rp` and open as [PR #1](https://github.com/Iodine98/troef-call-rulebook/pull/1).

## Verification commands

- `npm run dev` — visually check the relevant route after each milestone (felt theme rendering, card animations, narration matching example state).
- `npm run test` — vitest unit tests for the trick-resolution engine.
- `npm run validate-content` — cross-checks every authored example's claimed trick winner against the engine, catching authoring mistakes.
- `npm run build && npm run preview` — final PWA check: manifest installable, service worker active, offline reload works (verify via Chrome DevTools Application tab + Lighthouse PWA audit).
