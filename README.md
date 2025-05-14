# SpotLight

## Human Rights Violation Reporting Platform

## About The Project
The Human Rights Violation Reporting Platform is a web-based application designed to empower individuals to report and document human rights violations. It provides tools for users to describe incidents, categorize them, and tag locations, facilitating community involvement and official oversight.

### Key Features
- **Personal Profiles:** Users can view and manage their reported issues and comments.
- **Issue Reporting:** A detailed form allows users to describe incidents, select categories, and tag locations.
- **Community Engagement:** Users can comment on and upvote issues to increase visibility.

## Getting Started
To get a local copy up and running follow these simple steps.

### Prerequisites
This project uses npm as a package manager. You need to install npm if you haven't yet.
```bash
npm install npm@latest -g
```

### Installation

1. Clone the repo
```bash
git clone https://github.com/mtkarnik99/Spotlight.git
```
2. nstall NPM packages
```bash
npm install
```
3. Set up your environment variables
```
edit .env
```
4. Run the application
```
npm start
```

## Usage
Landing Page
<img width="953" alt="home_page" src="https://github.com/user-attachments/assets/162907ab-418b-42fa-bc14-2d260353ba6f" />

Issue Page
![issue_page](https://github.com/user-attachments/assets/30d8df11-3256-4482-b159-610cb40ccb7d)


Authorities Page
![authorities_page](https://github.com/user-attachments/assets/69668174-9c85-4c2c-9716-418a81a7d42f)

User Profile Page
![user_profile](https://github.com/user-attachments/assets/1e8def72-2ee4-431c-8689-5707e9c709ed)

Issue Form
![form_page](https://github.com/user-attachments/assets/92ff9d02-a2b2-4f0a-9d07-ee872c221daf)


## Authors : Meet Karnik

## Acknowledgments
- [MongoDB](https://www.mongodb.com/)
- [Express](https://expressjs.com/)
- [React](https://reactjs.org/)
- [Node.js](https://nodejs.org/)

Mermaid code for Object Model

# Object Model

```mermaid
---
Object Model for Spotlight

---
classDiagram

  class User{
    -int id
    -String username
    -String firstName
    -String lastName
    -String email
    -String password
  }

  class Issue{
    -int issueId
    -int  userId
    -String title
    -String content
  }
  class Interaction{
    -int issueId
    -String interactionType
    -int userId
  }
  class Comment{
    -int issueId
    -int userId
    -String content
  }

    User <|--PublicAuthority
    User <|--Admin

    User "1"*--"0..*" Issue
    Issue "1" *--"0..*" Comment
    Comment "1" *--"1" Interaction
    Issue "1" *-- "1" Interaction
    Comment "1" *-- "0..*" Comment

```
