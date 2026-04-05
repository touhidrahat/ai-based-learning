# SkillStreet - Interactive Learning Platform

## Deploying to Render

### What You'll Need

- An active Render account at https://render.com
- A MongoDB Atlas database ready to use
- Your codebase pushed to a GitHub repository

### Required Environment Variables

Configure these variables in your Render dashboard:

```
MONGODB_URI=mongodb+srv://username:password@cluster0.example.mongodb.net/database
JWT_SECRET=your_jwt_secret_key_here
REFRESH_TOKEN_SECRET=your_refresh_token_secret_here
ACCESS_TOKEN_EXPIRY=15m
REFRESH_TOKEN_EXPIRY=7d
NODE_ENV=production
```

### Deployment Steps

#### Method 1: Blueprint Deployment (Recommended)

1. Ensure the `render.yaml` file exists in your repository
2. Sign in to Render
3. Navigate to Dashboard and select "New" > "Blueprint"
4. Link your GitHub and choose the repo
5. Render automatically picks up the `render.yaml` configuration
6. Hit "Apply" to kick off the deployment
7. Fill in the environment variables through the Render dashboard

#### Method 2: Manual Configuration

1. Sign in to Render
2. Head to Dashboard and select "New" > "Web Service"
3. Link your GitHub and pick your repository
4. Set up the service details:
   - Name: `skillstreet` (or whatever you prefer)
   - Environment: `Node`
   - Build Command: `pnpm install && pnpm run build`
   - Start Command: `pnpm start`
5. Input all necessary environment variables
6. Hit "Create Web Service" to launch

### After Deployment

Once deployed:

1. Allow the build process to finish
2. Access your live application via the Render URL
3. Update `NEXT_PUBLIC_API_URL` and `NEXT_PUBLIC_SOCKET_URL` with your new Render endpoint if necessary

## Running Locally

1. Clone this repository
2. Install all dependencies: `pnpm install`
3. Duplicate `.env.sample` to `.env` and populate your values
4. Start the development server: `pnpm dev`

Your local app will run on `http://localhost:3000`.

This project was bootstrapped using [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app) and built on [Next.js](https://nextjs.org).

## Getting Started

Launch the development server with one of these commands:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Navigate to [http://localhost:3000](http://localhost:3000) in your browser to view the application.

Edits to `app/page.tsx` will automatically reflect in the browser without requiring a refresh.

The project leverages [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) for automatic optimization and loading of [Geist](https://vercel.com/font).

## Additional Resources

Expand your Next.js knowledge with these resources:

- [Next.js Documentation](https://nextjs.org/docs) - comprehensive guide to features and APIs
- [Learn Next.js](https://nextjs.org/learn) - hands-on tutorial experience

Visit [the Next.js GitHub repository](https://github.com/vercel/next.js) to explore the source code and contribute feedback.

## Vercel Deployment

For the smoothest deployment experience, check out the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme), built by the Next.js team.

More detailed deployment steps can be found in the [Next.js deployment docs](https://nextjs.org/docs/app/building-your-application/deploying).
# skill-street
# ai-based-learning
