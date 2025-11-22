Here is a 2-week, day-by-day Cypress roadmap that takes you from beginner → intermediate → PRO level, focused on real-world apps, independent of any UI framework (React, Vue, Angular, Next.js — doesn’t matter).

This plan is intense but achievable.
You’ll learn every core concept used by senior QA engineers + frontend devs testing real apps.


---

🚀 Cypress 2-Weeks Roadmap — Beginner to Pro (Real-World App Focused)

No UI library dependency (AntD, Material UI, Tailwind, etc — doesn't matter).


---

⭐ WEEK 1 — FOUNDATIONS + REAL E2E BASICS

Goal → Understand Cypress fully, test a real app, and build strong fundamentals.


---

📅 Day 1 — Environment Setup + First Test

What you learn

✔ Install Cypress
✔ Folder structure
✔ Run first spec

Tasks

Install Cypress (npm install cypress@latest)

Run npx cypress open

Understand:

e2e/

fixtures/

support/

cypress.config.js


Write your first test:


describe("Smoke test", () => {
  it("opens the homepage", () => {
    cy.visit("/")
    cy.contains("Home")
  })
})


---

📅 Day 2 — Master Basic Commands

What you learn

✔ cy.get
✔ cy.contains
✔ .type(), .click(), .should()
✔ Using selectors properly

Tasks

Practice selecting elements using:

data-test attributes

cy.contains()

cy.get()


Write tests for:

Login page

Simple form

Submit button




---

📅 Day 3 — Assertions & Retry Logic

What you learn

✔ Implicit waits (Cypress magic)
✔ Assertions
✔ Retry pattern

Tasks

Test UI components that load asynchronously

Practice:


cy.get("h1").should("be.visible")
cy.get(".card").should("contain", "Name")


---

📅 Day 4 — Network Intercepts (Core for Real Apps)

What you learn

✔ cy.intercept()
✔ Mock backend
✔ Wait for API calls

Tasks

Test real API calls:


cy.intercept("GET", "/api/users").as("users")
cy.wait("@users")

Mock API responses using fixtures

Test UI rendering based on response


👉 You now know how modern E2E testing actually works.


---

📅 Day 5 — Fixtures + Test Data Strategy

What you learn

✔ Using fixtures
✔ Dynamic test data
✔ Creating reusable data patterns

Tasks

Create fixtures/users.json

Load it in tests:


cy.fixture("users").then(data => {...})

Understand static vs dynamic data



---

📅 Day 6 — Real Login Flow (UI + API Login)

What you learn

✔ UI login testing
✔ API login testing
✔ Storing tokens in localStorage

Tasks

Test login via UI

Create a custom command:


Cypress.Commands.add("loginViaApi", () => {
  cy.request("POST", "/api/login", { email, password })
    .then(res => localStorage.setItem("token", res.body.token))
})

Visit a protected page

Validate user session



---

📅 Day 7 — Mid-Week Mini Project

Build tests for a real module (e.g. Users Management):

✔ Visit
✔ Load data
✔ Search
✔ Pagination
✔ Table validations

No UI framework specifics — all selectors through data-test.


---

⭐ WEEK 2 — PRO LEVEL (POM, MOCKING, COMPONENT TESTING, CI/CD)

Goal → Build a real-world testing framework with POM + mocks + commands.


---

📅 Day 8 — Page Object Model (POM)

What you learn

✔ Structuring real automation framework
✔ Reusability
✔ Clean code

Tasks

Create pages/ folder

Build:

loginPage.js

usersPage.js


Write tests using POM:


loginPage.login("admin@test.com", "123456")
usersPage.search("Ashfaq")


---

📅 Day 9 — Custom Cypress Commands

What you learn

✔ Cleaner tests
✔ Reusability
✔ Encapsulating patterns

Tasks

Build commands:

cy.login()

cy.getByTest()

cy.createUser()

cy.resetDb() (if backend allows)



---

📅 Day 10 — Advanced Intercepts + Test Isolation

What you learn

✔ Full network mocking
✔ Fail network calls intentionally
✔ Test edge cases
✔ Stubbing partial APIs

Tasks

Mock multiple API states:

success

empty data

error


Test UI behavior for each API state

Handle loading skeletons


This is REAL QA work.


---

📅 Day 11 — Advanced Real-World UI Testing

What you learn

✔ Pagination
✔ Sorting
✔ Filters
✔ Modals
✔ Toasts
✔ Async UI

Tasks

Test:

Table page

Pagination

Filter

Sort

Modal open/close

Toast visibility


All independent of UI library.


---

📅 Day 12 — Component Testing (React/Vue/Angular/Any)

Even though you said independent of framework, component testing logic stays SAME.

What you learn

✔ Test components in isolation
✔ Stub backend
✔ Mount components (framework agnostic)

Skills:

test form validation

test tables

test modals

test loading states



---

📅 Day 13 — CI/CD + Parallel Testing

What you learn

✔ Headless mode
✔ GitHub Actions
✔ Parallel tests
✔ Cypress Dashboard

Tasks:

Run tests headless:


npx cypress run

Configure GitHub Actions pipeline

Integrate artifacts/screenshots



---

📅 Day 14 — Final Project

Build a complete real-world test suite for a sample app:

Modules:

Login

Dashboard

Users list

User create

User edit

User delete

Filters

Pagination

API mocks

POM structure

Custom commands


Deliverables:

Clean code

Fully modular Cypress framework

Runs in CI/CD pipeline


After this → you’re Cypress Pro Level.


---

🎁 BONUS (If you want)

I can prepare:

🔥 A complete Cypress project template (folder structure + commands + POM)
🔥 Real Users module tests (pagination, filters, API stubs)
🔥 A daily checklist for each day
🔥 Notes like QA engineers use
🔥 Exercises + challenges for each day

Just tell me.
