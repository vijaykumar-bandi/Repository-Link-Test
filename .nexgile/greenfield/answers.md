# Requirements brief — Repository Link Test
## Profile
A minimal Node.js Express web app with a single home page that displays the text "Repository Link Test", for the person who asked for it. · web app · software development · size: small · depth: quick
- **Has a user interface?** Yes (It serves one home page to a browser.)
- **Runs locally?** Yes (An Express app serves its page on a local port, so Greenfield can start it on the person's machine.)
## The app
A minimal Node.js Express web app with one home page that displays the text "Repository Link Test", for the owner to check the repository link works. It has no database, login, deployment or integrations, and runs on the owner's computer with npm start at http://localhost:3000.
## Goals and success
- G1 Show the text "Repository Link Test" on a home page. (description)
- M1 The owner opens the app and sees the text 'Repository Link Test' on the home page by the end of this week. (end of this week) (Q12)
## Workflows
### W1 Check the repository link (release 1) — actors: owner; trigger: The owner wants to check the repository link works; outcome: The owner has seen the text and knows the repository link works; how often: occasionally (Q6)
1. Open the app in a browser
2. See the home page with the text "Repository Link Test"
3. Check that the text is there
4. Close the app
- X1 The page fails to load or shows the wrong text. (Q13)
## Scope and constraints
- S5 Built with Node.js and Express. [constraint] (description, Q4)
## Decisions
- **Stack:** Node.js with Express (the user's choice; suggested: The description already fixes Node.js and Express, and it fits a single page with no database or login.) (Q4)
- **Deploy target:** On this computer only (the user's choice; suggested: It is the simplest way to check the repository link without extra setup.) (Q8)
- **Mock-ups of the key screens first:** No, build it directly (the user's choice; suggested: The page is one line of text, so a mock-up adds little.) (Q9)
## Assumptions
- A1 The app is used by one person, the owner, who checks the repository link works. — The description and Q2 say the one home page is for the owner alone. (assumption, Q1, Q10, Q11)
- A2 The app keeps track of nothing; it has no records. — The app only shows a fixed text on one page, so there is nothing to store. [the user was not sure] (assumption, Q7)
- A3 The page is in English with basic accessibility (semantic HTML, readable text). — No accessibility or language requirement stated: should the page meet any accessibility level or be in a specific language? [assumed] (gap)
- A4 The page works in any modern browser on desktop and phone. — No device requirement stated: should the page work on phone as well as desktop? [assumed] (gap)
- A5 Today the owner checks the repository link by opening the repository in a browser and looking for the text. — No answer describes today's way; the app replaces a manual check of the repository link. [assumed] (assumption)
- A6 No similar product is used; the closest is opening the repository page itself. — No similar product was named; the app is a one-page check. [assumed] (assumption)
- A7 The only business event is the owner opening the app; no timed events apply. — The app has one page and no records, so no timed events are needed. [assumed] (assumption)
- A8 There are no permissions: the owner is the only user and may do everything. — No login and one user, so no permission rules apply. [assumed] (assumption)
- A9 There are no business rules beyond showing the fixed text. — The app only displays one fixed text, so no business rules apply. [assumed] (assumption)
- A10 There are no notifications. — No one else uses the app and nothing needs to be announced. [assumed] (assumption)
- A11 There are no reports. — The app has no records to report on. [assumed] (assumption)
- A12 There is no administration: nothing can be changed without a developer. — The app is a fixed one-page check with no settings. [assumed] (assumption)
- A13 There is no money involved: no pricing, refunds, tax, invoices or card data. — The app is a free internal check for the owner. [assumed] (assumption)
- A14 There are no files or content beyond the fixed text on the page. — The app shows one fixed text and handles no uploads. [assumed] (assumption)
- A15 One user at a time, with at most a few page views per day; no records are stored. — The app is for the owner alone to check the link. [assumed] (assumption)
- A16 The home page loads in under 2 seconds on the owner's computer. — A one-page app should load quickly; no performance target was given. [assumed] (assumption)
- A17 There is no availability requirement beyond the owner restarting the app if it stops. — The app runs only on the owner's computer and holds no data. [assumed] (assumption)
- A18 There is no sign-in; the app is open only on the owner's computer. — No login is in scope and the app runs locally. [assumed] (assumption)
- A19 No personal data is held; the app stores nothing. — The app has no records and no login. [assumed] (assumption)
- A20 There is no audit trail; nothing needs to be provable. — The app has no records and one user. [assumed] (assumption)
- A21 There is no existing data to move into the app. — The app keeps no records and replaces no system. [assumed] (assumption)
- A22 There are no integrations with other systems. — No integrations are in scope. [assumed] (assumption)
- A23 There is no support or operations process; the owner restarts the app if needed. — The app runs locally for one person. [assumed] (assumption)
- A24 There is one organisation only; no tenancy is needed. — The app is for the owner alone. [assumed] (assumption)
- A25 The app is a small risk: if it fails, the owner reloads or restarts it. — The app is a one-page check with no data. [assumed] (assumption)
## Other facts
- F1 The app has one home page. [scope] (description)
- F2 The one home page is for the owner alone, to check the repository link works. [stakeholders] (Q2)
- F3 The app keeps track of nothing; it has no records. [entities] (Q7)
- F4 The app runs on the owner's own computer only. [hosting] (Q8)
- F5 No mock-ups are shown before building; the home page is built directly. [look] (Q9)
- F6 No one is worse off because the app exists; it is just for the owner. [stakeholders] (Q10, Q11)
- F7 The app is started with 'npm start' and opened at http://localhost:3000 in a browser. [hosting] (Q14)
## Out of scope and later releases
- S1 No database. [out of scope] (description)
- S2 No login. [out of scope] (description)
- S3 No deployment. [out of scope] (description)
- S4 No integrations. [out of scope] (description)
- S6 Nothing else beyond the one home page. [out of scope] (Q3)
- Records: not relevant, from the user's answers [out of scope]
## The interview
- Q1 [stakeholders · owner] Who will use the app, and about how many people of each kind? → Not sure (settled: The app is used by one person, the owner, who checks the repository link works.)
- Q2 [stakeholders · owner] Who is the one home page for, and what will they do with the text on it? → Just me, to check the repository link works. (Greenfield's draft, sent unchanged)
- Q3 [scope · owner] Besides the one home page, what else should the app do? → Nothing else
- Q4 [stack · owner] Which stack should the app be built with? → Node.js with Express
- Q5 [workflows · owner] Walk me through the most important task in the app, step by step. → Not sure
- Q6 [workflows · admin] When you open the app, what do you do, step by step, from opening it to finishing? → 1. Open the app in a browser 2. See the home page with the text "Repository Link Test" 3. Check that the text is there 4. Close the app
- Q7 [entities · admin] What things does the app need to keep track of? → Not sure (settled: The app keeps track of nothing; it has no records.)
- Q8 [hosting · operations] Where should the app run so you can open it? → On this computer only
- Q9 [look · operations] Should I show you mock-ups of the home page before building it? → No, build it directly
- Q10 [stakeholders · negative] Who, if anyone, could be worse off because this app exists? → No one — it is just for me. (Greenfield's draft, sent unchanged)
- Q11 [stakeholders · negative] The app is used by one person, you, and no one else signs in or is affected — is that right? → Yes, that's right
- Q12 [success · owner] How will you know the app works — what will you see or do, and by when? → I open the app and see the text 'Repository Link Test' on the home page, by the end of this week. (Greenfield's draft, sent unchanged)
- Q13 [exceptions · owner] If the page fails to load or shows the wrong text, what should happen? → Nothing special — I just reload the page or check the server is running. (Greenfield's draft, sent unchanged)
- Q14 [hosting · owner] How should you start the app on your computer — what command, and on which port? → Run 'npm start' and open http://localhost:3000 in a browser. (Greenfield's draft, sent unchanged)
