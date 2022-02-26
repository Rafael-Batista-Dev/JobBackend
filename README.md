# JobFrontBackend

# On the frontend just put the login to work. Ready-made frameworks can be used.

# Job Posting - Backend

A service that helps you publish miles and find the most suitable sellers among advertisers.

## 🛠 Technologies

The following tools must be used in the construction of the project:

- [Node.js](https://nodejs.org/en/)
- [React](https://reactjs.org)
- [AWS](https://aws.amazon.com/)
- [Mysql](https://www.mysql.com/)

## 🚦 Endpoints

### Admin

Use `/admins` before every mentioned endpoint.

- signup: `POST: /`
- login: `POST: /login`
- logout: `POST: /logout`
- logout of multiple sessions: `POST: /logoutAll`
- Fetch Personal details: `GET: /me`
- Update personal details. `PATCH: /me`
- Fetch mile posts: `GET: /miles`
- Post a mile. `POST: /miles`
- Update mile details: `PATCH: /miles`
- Get particular mile details: `/miles/:mile_id`
- Update Particular mile details: `PATCH: /miles/:mile_id`
- Reject or accept a advertiser: `POST: /miles/:mile_id/:advertisers_id/:outcome`

### Advertisers.

Use `/advertisers` before every mentioned endpoint.

- signup: `POST: /`
- login: `POST: /login`
- logout: `POST: /logout`
- logout of multiple sessions: `POST: /logoutAll`
- Fetch Personal details: `GET: /me`
- Update personal details. `PATCH: /me`
- Fetch mile applications: `GET: /applications`
- Apply for a mile. `POST: /applications/:mile_id`
- Delete mile application: `DELETE: /applications/:mile_id`
- Fetch all drafts: `/drafts`
- Save as draft: `PATCH: /drafts/:mile_id`
- Delete or publish draft: `POST: /drafts/:mile_id/:option`

### 📩 Mails

Mails are sent when an advertiser makes their miles available and when an admin accepts/rejects the advertiser.. nodemailer is used for the purpose and mails are sent via smtp but if you have your own domain conside OAuth.

## ⚙️ Config

You need a `dev.env` file to run in development environment.

You're required to create you'r own config folder with `dev.env` file containing

- PORT
- JWT_SECRET
- MailId
- MailPassword

## 📱 📲 cloning and starting application

- Clone:

  ```bash
  git clone <repo>
  cd <repo_name>
  ```

- install packages and dev-dependencies:

  ```
  npm install
  ```

- create `config` folder and file as mentioned above.
- start development server

  ```
  npm run dev
  ```
