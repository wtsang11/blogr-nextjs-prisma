# Fullstack Authentication Example with Next.js and NextAuth.js

This is the starter project for the fullstack tutorial with Next.js and Prisma. You can find the final version of this project in the [`final`](https://github.com/prisma/blogr-nextjs-prisma/tree/final) branch of this repo.

## Bootstraping the Project

- Guide of this project https://vercel.com/guides/nextjs-prisma-postgres
- Clone the initial project
- Create a repository blogr-nextjs-prisma in github, and push initial project to github.
- import github repository to vercel to create a new project, create a postgres database in vercel project.
- install vercel locally: npm i -g vercel@latest
- pull latest environment variables from vercel: vercel env pull .env
  - Error: Your codebase isn’t linked to a project on Vercel. Run `vercel link` to begin.
  - Indeed, vercel link command will prompt for the github project. Select github from william.k.tsang@gmail.com (not the static organization), select the project. Project successfully linked to github repository of the project.

## Setup Prisma and Create Database Schema (Step 3)

- npm i -D prisma
- Create prisma/schema.prisma with two models
- npx prisma db push
- npx prisma studio : add some dummy data

## Install and Generate Prisma Client

- npm i @prisma/client
- Generate a client based on the project schema: npx prisma generate
- Create a script file to ensure the use of a single instance of client: mkdir lib && touch lib/prisma.ts

## Using Next-Auth

- Installation error solution:
  - npm install next-auth@4.1.2
  - npm install --legacy-peer-deps @next-auth/prisma-adapter
