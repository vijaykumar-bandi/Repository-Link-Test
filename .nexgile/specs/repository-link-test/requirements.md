# Requirements: Repository Link Test

## Requirement 1: Show the text on the home page

**User Story:** As the owner, I want to open the app in a browser and see the text "Repository Link Test" on the home page, so that I know the repository link works.

_Source: G1, W1, F1, F2_

### Acceptance Criteria

1. WHEN the owner opens the app at `/` THE SYSTEM SHALL respond with a home page that displays the text "Repository Link Test".
2. THE SYSTEM SHALL display the text "Repository Link Test" exactly once on the home page, with the same spelling and capitalisation.
3. THE SYSTEM SHALL serve the home page as an HTML document with a `200` status.
4. THE SYSTEM SHALL display the text "Repository Link Test" as the page's main heading in a semantic HTML heading element.
5. THE SYSTEM SHALL display the text "Repository Link Test" as readable text in the page's body, in English.

## Requirement 2: Start the app on the owner's computer

**User Story:** As the owner, I want to start the app with `npm start` and open it at `http://localhost:3000`, so that I can check the repository link on my own computer.

_Source: S5, F4, F7, A18_

### Acceptance Criteria

1. WHEN the owner runs `npm start` THE SYSTEM SHALL start an Express server that listens on port `3000` by default.
2. WHEN the `PORT` environment variable is set THE SYSTEM SHALL listen on the port it names instead of `3000`.
3. WHEN the server is running THE SYSTEM SHALL answer a request to `/` within 2 seconds.
4. IF a request is made to a path other than `/` THEN THE SYSTEM SHALL respond with a `404` status.
5. THE SYSTEM SHALL serve the home page without a database, a login, or any integration with another system.

## Requirement 3: Recover when the page does not load

**User Story:** As the owner, I want to reload the page or restart the app when it fails, so that I can still check the repository link.

_Source: W1, X1, A17, A23, A25_

### Acceptance Criteria

1. IF the server is not running THEN THE SYSTEM SHALL fail the request to `/` rather than serve a page without the text.
2. WHEN the owner reloads the home page THE SYSTEM SHALL respond with the same home page displaying the text "Repository Link Test".
3. WHEN the owner restarts the app with `npm start` THE SYSTEM SHALL serve the home page displaying the text "Repository Link Test" again.

## Later releases

- S1 No database.
- S2 No login.
- S3 No deployment.
- S4 No integrations.
- S6 Nothing else beyond the one home page.

## Assumptions

- The home page is the only screen, and `/` is where the app starts for the owner.
- The owner is the only person who uses the app, so there are no roles and no screen per role after signing in.
- The page is in English with basic accessibility (semantic HTML, readable text), as settled in A3.
- The page works in any modern browser on desktop and phone, as settled in A4.
- The home page loads in under 2 seconds on the owner's computer, as settled in A16.
- The app keeps no records, so there is nothing to store, report on or audit, as settled in A2, A11 and A20.
- The app runs on the owner's computer only, with no deployment, as settled in F4 and S3.
