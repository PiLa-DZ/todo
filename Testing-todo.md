# Testing

(Test-Driven Development (TDD))
You need to implement Test-Driven Development (TDD) into your current projects.

1. Unit Testing: (What we are doing now with node:test).

2. Integration Testing:
   Testing how your API talks to your MariaDB/Prisma database
   (this is where most AI mistakes happen).

3. Mocks and Spies: How to "fake" the database so your tests are fast.

---

| Week 1 | "Unit Testing Basics (Assertions , describe, it)" | Vitest
| Week 2 | Mocking (How to fake a database so your tests stay fast) | Vitest (vi.mock)

- [ ] Spelling Check

---

## MVC (Model-View-Controller)

Model (The Data)
View (The Interface)
Controller (The Boss)

---

Nabil-ify

- Software Architecture Patterns and Design Principles.

- Separation of Concerns (SoC) It means: "Don't put your brain, your hands, and your mouth in the same file."
  - The Brain (Logic): Pure functions that calculate things (e.g., filterTasks).
  - The Hands (Infrastructure): Code that touches the disk or DB (e.g., db.read).
  - The Mouth (Interface): The CLI or Express routes that talk to the user (e.g., app.js).
- Design Patterns (specifically for Backend)
- Dependency Injection (DI)
- Clean Architecture (The Basics)

1. A "Pro" Folder Structure for your Project

```bash
.
├── src/
│   ├── index.js          # Entry point (The Mouth)
│   ├── services/         # Business Logic (The Brain)
│   │   └── taskService.js
│   ├── models/           # Data Structures
│   │   └── Task.js
│   ├── repository/       # Data Access (The Hands)
│   │   └── db.js
│   └── utils/            # Pure Helper Functions
│       └── validation.js
├── tests/                # Mirror of src/ structure
│   ├── services/
│   └── utils/
├── tasks.json
├── package.json
└── README.md
```

---

- Project Layout Patterns

## The "Standard" Professional Backend Structure

For a Node.js/TypeScript backend,
this is the layout that allows you to walk into a project months later
and immediately know where the "brain," the "hands," and the "mouth" are.

```bash
.
├── bin/                  # Executable files (if it's a CLI tool)
├── config/               # Environment variables, database credentials, logger settings
├── src/                  # ALL source code lives here
│   ├── controllers/      # THE MOUTH: Handles requests/CLI input, sends responses
│   ├── services/         # THE BRAIN: Business logic (where calculations happen)
│   ├── models/           # THE BONES: Database schemas (Prisma models/Classes)
│   ├── repository/       # THE HANDS: Direct Database/File I/O (SQL queries, fs.write)
│   ├── middlewares/      # THE FILTERS: Auth, validation, logging (for APIs)
│   ├── utils/            # THE TOOLS: Pure helpers (date formatting, math)
│   └── app.js            # The entry point that connects everything
├── tests/                # Mirror of src/ structure
│   ├── unit/             # logic tests (utils, services)
│   └── integration/      # database/API tests
├── data/                 # Local storage (JSON files, etc.)
├── .env                  # Secrets (don't push to GitHub!)
├── package.json
└── README.md
```

---

```bash
# A simple function to bootstrap a Pro Node project
bootstrap-node() {
  mkdir -p {bin,src/{controllers,services,models,repository,utils},tests/{unit,integration},data,config}
  touch src/app.js .env README.md .gitignore
  npm init -y
  echo "Project structure for $1 created."
}
```

Project Archetypes (Documentation)
"Project Guidelines" repositories. These aren't "tools" you install, but "Blueprints" you follow.

goldbergyoni/nodebestpractices: This is the "Bible" of Node.js. It has a specific section on Project Structure that aligns perfectly with the Roadmap we discussed.

---

## Domain-Driven Design (DDD) and Component-Based Architecture

```bash
.
├── components/
│   ├── expenses/
│   │   ├── expense.api.js        # The Mouth (Routes/CLI)
│   │   ├── expense.service.js    # The Brain (Logic)
│   │   ├── expense.repository.js # The Hands (DB)
│   │   └── tests/                # Component-specific tests
│   ├── auth/
│   │   ├── login.service.js
│   │   └── user.repository.js
│   └── reports/
│       ├── pdf.generator.js
│       └── stats.logic.js
├── libraries/                    # Shared code (cross-cutting)
│   ├── logger.js
│   └── validator.js
└── app.js
```
