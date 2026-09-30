# GAA League Manager (Angular + Express)

A web app for the GAA National Football League: teams, players, results, league tables and stats. The front end is Angular and it talks to an Express REST API backed by MySQL.

## Features

- **Teams:** a sortable table with links to each team's Wikipedia page.
- **Players:** sorted by team and name, with a team filter.
- **Results:** match results by round, with round navigation and a team filter.
- **Tables:** Division 1 standings (points, wins, draws, losses, goal difference) calculated in the app.
- **Stats:** d3.js charts of team form and match scores (scatter plots and bar charts).
- **Login and admin:** after login the navbar updates, and admins can edit and delete match results by round.

## Tech stack

**Frontend:** Angular 17, Bootstrap 5, d3.js
**Backend:** Node.js, Express, MySQL

## API

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/teams` | All teams |
| GET | `/players` | All players |
| GET | `/results` | All match results |
| GET | `/results/:round` | Results for one round |
| POST | `/login` | Log in |
| POST | `/results/update` | Edit a result (admin) |
| DELETE | `/results/:id` | Delete a result (admin) |

## Getting started

Needs Node.js, the Angular CLI and a MySQL database set up with the provided script.

```bash
# REST API
cd "Web Framework Code/a2restapi_"
npm install
node index.js

# Angular app, in a second terminal (http://localhost:4200)
cd "Web Framework Code/a2ng_"
npm install
ng serve
```

## Screenshots

![Screenshot 1](https://github.com/user-attachments/assets/fcf4072f-830f-4510-9e68-594d749fc2a9)
![Screenshot 2](https://github.com/user-attachments/assets/5d8ec0c9-9408-4e51-a154-bd3bb5266a6e)
![Screenshot 3](https://github.com/user-attachments/assets/9903c61a-2f77-4485-afec-6f964100fa2b)
![Screenshot 4](https://github.com/user-attachments/assets/a3ba54bd-4985-4f26-98ff-d4175b3eef49)
![Screenshot 5](https://github.com/user-attachments/assets/c4dc2cf6-5a0e-44b2-be14-823dd22a037c)
![Screenshot 6](https://github.com/user-attachments/assets/d0148508-fabd-42ce-9b7a-251ef37672f0)
![Screenshot 7](https://github.com/user-attachments/assets/bab388ab-3570-43d3-bc09-734734bd6a3c)

## Project structure

```
Web Framework Code/
├── a2ng_/          # Angular front end (components: teams, players, results, tables, stats, login, admin)
└── a2restapi_/     # Express REST API
Web Framework Submission Docs/   # submission checklist + cover sheet
```

## Context

Web Framework Development module (2024).
