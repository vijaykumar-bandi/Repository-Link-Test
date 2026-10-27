# Tasks: Repository Link Test

- [ ] 1. Project setup
  - [ ] 1.1 Project setup
    - Create the Express skeleton: `package.json` with `start` and `dev` running `node server.js` and `test` running `node --test`, the `express` dependency and `@playwright/test` as a dev dependency; `app.js` exporting the app with a `GET /` route that sends `views/home.html` as `text/html; charset=utf-8` with status `200` and a `404` plain-text handler for any other path; `server.js` listening on `process.env.PORT` or `3000`; `views/home.html` with `<html lang="en">`, a `<title>` of `Repository Link Test`, a `<main>` holding one `<h1>` whose text is exactly `Repository Link Test`, and a link to `/static/styles.css`; `public/styles.css`; `README.md` with the commands of Build and run; `.gitignore` including `.env`; `e2e/.gitkeep`; and `test/home.test.js` starting the exported app on port `0` and checking the `200`, the content type and the exact heading text.
    - _Requirements: 1.1, 1.2, 1.3, 1.4, 1.5, 2.1, 2.2, 2.3, 2.4, 2.5_
    - _Files: package.json, package-lock.json, app.js, server.js, views/home.html, public/styles.css, README.md, .gitignore, e2e/.gitkeep, test/home.test.js_
    - _Verify: npm install_
    - _Verify: npm test_
    - _Area: setup_
- [ ] 2. Home page styles
  - [ ] 2.1 Style the home page
    - Centre the heading, set a readable base font size and line height, and keep the text legible on narrow screens, with no layout framework and no external font; add `test/styles.test.js` checking that `/static/styles.css` answers `200` with `text/css` and that the home page links to it.
    - _Requirements: 1.5_
    - _Depends: 1.1_
    - _Files: public/styles.css, test/styles.test.js_
    - _Verify: npm test -- styles_
    - _Area: ui_
- [ ] 3. Route and recovery tests
  - [ ] 3.1 Test the 404, the port and the reload
    - Add `test/routes.test.js`: a request to a path other than `/` answers `404`; the server listens on the port named by `PORT`; a second request to `/` after the first answers the same page with the text; and a fresh process started with `npm start` on a free `PORT` answers `/` with the text, then is stopped.
    - _Requirements: 2.2, 2.4, 3.1, 3.2, 3.3_
    - _Depends: 1.1_
    - _Files: test/routes.test.js_
    - _Verify: npm test -- routes_
    - _Area: api_
- [ ]* 4. End-to-end journey
  - [ ]* 4.1 Journey: check the repository link
    - Save a Playwright journey in `e2e/check-repository-link.spec.js` that opens `/`, reads the heading `Repository Link Test`, reloads the page and reads it again, plus `playwright.config.js` pointing at the app's `PORT`.
    - _Requirements: 1.1, 1.2, 1.4, 3.2_
    - _Depends: 1.1_
    - _Files: e2e/check-repository-link.spec.js, playwright.config.js_
    - _Verify: npx playwright test --list_
    - _Area: ui_

## Assumptions

- The app has no database, login, integration or deployment, so there is no seed script, no `.env.example` and no Deployment setup task.
- `npm test` runs `node --test`, which picks up `test/*.test.js` and leaves `e2e/` out, since those journeys need the running app.
- The end-to-end journey is optional: the route tests already cover the criteria it checks, and the journey is saved by Greenfield's Tester.
