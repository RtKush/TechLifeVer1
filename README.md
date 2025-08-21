<img width="1920" height="1080" alt="Screenshot (785)" src="https://github.com/user-attachments/assets/1cbae240-fd6a-443d-88ba-cd0059c7a150" />
<img width="1750" height="911" alt="Screenshot 2025-07-22 005820" src="https://github.com/user-attachments/assets/5b4e8692-4614-4edf-8ee2-fec3e5fb5527" />
<img width="1920" height="1080" alt="Screenshot (787)" src="https://github.com/user-attachments/assets/6748842f-9a58-45be-a69c-61cebed9819d" />
<img width="1920" height="1080" alt="Screenshot (821)" src="https://github.com/user-attachments/assets/54836f1b-eab1-4d6c-891f-862efc67bead" />
<img width="1920" height="1080" alt="Screenshot (778)" src="https://github.com/user-attachments/assets/51ed36c9-67c8-4fc2-86dd-459f18cae921" />
<img width="1920" height="1080" alt="Screenshot (788)" src="https://github.com/user-attachments/assets/fb30daaf-7603-4911-9ba3-ee543dd2c134" />




# 🚀 TechLife - Blogging Webside

A modern platform built with **Next.js 15**, **TypeScript**, **Tailwind CSS**, **Redux Toolkit**, and **MongoDB** to manage internships, events, and student applications.

## 🚀 Getting Started
```bash
git clone https://github.com/RtKush/TechLifeWorking
cd TechLifeWorking
npm install
npm run dev


## 📦 Tech Stack

- **Frontend**: Next.js 15 (App Router), React 19, Tailwind CSS, Shadcn, Aceternity UI, Lucide Icons
- **State Management**: Redux Toolkit + RTK Query
- **Authentication**: NextAuth (Credential + Google OAuth-ready)
- **Database**: MongoDB (via Mongoose)
- **Editor**: TipTap (Rich Text Editor)
- **Media Upload**: ImageKit (image & video CDN)
- **Deployment**: Vercel

---

## 📊 Features

### 🌐 Core Architecture

- ✅ Next.js 15 with the new App Router
- ✅ TypeScript support across the entire codebase
- ✅ Modular project structure: app/, components/, features/, lib/, model/, etc.
- ✅ Tailwind CSS for modern utility-first UI styling
- ✅ Public asset management via /public
- ✅ Centralized middleware.ts with route protection logic

### 🔐 Authentication & Access Control

- ✅ NextAuth.js integration with credentials provider
- ✅ JWT-based route protection via middleware
- ✅ Public Routes:
  - /, /blog, /reels, /auth/login, /auth/register, /blog/[slug]
- ✅ Protected Routes (authentication required):
  - /create-blog, /add-reel, dashboard, user actions, etc.

### 📄 Blogging System

- ✅ Blog creation page: /create-blog
- ✅ Blog listing page: /blog
- ✅ Dynamic blog detail pages: /blog/[slug]
- ✅ Recent blog sidebar with latest posts
- ✅ Modular blog card components
- ✅ Comment section placeholder included
- ✅ Public read access for all blogs

### 📡 API & State Management

- ✅ RTK Query for efficient API communication
- ✅ Redux Toolkit for global state management
- ✅ Organized features/ folder: auth/, blogs/, comments/, reels/
- ✅ Modular API routes inside app/api/

### 📱 Responsive & Accessible UI

- ✅ Fully responsive navbar with mobile hamburger menu and auth-aware navigation
- ✅ Reusable, scalable UI components
- ✅ Consistent design system (spacing, color, typography)

### 🖼️ Image & Media Handling

- ✅ Static assets served from /public
- ✅ ImageKit for uploading and hosting reels

##⚙️ Environment Variables
Create a .env.local file in the root and add:

env
Copy code

```bash
MONGODB_URI=
NEXTAUTH_SECRET=
NEXTAUTH_URL=

IMAGEKIT_PRIVATE_KEY=
NEXT_AUTH_IMAGEKIT_PUBLIC_KEY=
IMAGEKIT_URL_ENDPOINT="https://ik.imagekit.io/[your_userName]"

NODE_ENV="development"
NEXT_PUBLIC_AUTH_BACKEND_BASE_URL=
NEXT_PUBLIC_NEXTAUTH_URL=
```

## 🧑‍💻Run Locally

```bash
npm run dev
# or
yarn dev
```

````bash

```bash Visit: http://localhost:3000 ```
````

## 📂 Folder Structure

```bash
├── app/
│   ├── add-reel/
│   ├── api/
│   │   ├── auth/
│   │   ├── comments/
│   │   ├── imagekit-auth/
│   │   ├── post/
│   │   ├── reel/
│   │   ├── search/
│   │   └── user/
│   ├── auth/
│   ├── blog/
│   ├── create-blog/
│   ├── dashboard/
│   ├── edit-blog/
│   ├── profile/
│   ├── providers/
│   ├── reels/
│   ├── ClientLayout.tsx
│   ├── StoreProvider.tsx
│   ├── layout.tsx
│   ├── page.tsx
│   └── globals.css
├── component/                 # 3rd-party UI components (e.g., TipTap)
│   ├── tiptap-extension/
│   ├── tiptap-icons/
│   ├── tiptap-node/
│   ├── tiptap-templates/
│   ├── tiptap-ui/
│   ├── tiptap-ui-primitive/
│   └── ui/
├── components/                # Custom reusable components
│   ├── blog/
│   ├── comment/
│   ├── reel/
│   ├── skelton/
│   ├── upload/
│   ├── user/
│   ├── About.tsx
│   ├── Carousel.tsx
│   ├── CTA.tsx
│   ├── Footer.tsx
│   ├── Hero.tsx
│   ├── HomeBlog.tsx
│   ├── LikeButton.tsx
│   ├── Navbar.tsx
│   ├── Provider.tsx
│   ├── SearchBar.tsx
│   ├── SigninForm.tsx
│   ├── SignOut.tsx
│   └── Singup.tsx
├── features/                 # RTK slices and RTK Query endpoints
│   ├── auth/
│   ├── blogs/
│   ├── comments/
│   └── reels/
├── hooks/                    # Custom React hooks
├── lib/                      # Utilities, DB, Auth, Store
│   ├── auth.lib.ts
│   ├── Backend-helperFn.ts
│   ├── db.lib.ts
│   ├── hooks.ts
│   ├── store.ts
│   ├── tiptap-utils.ts
│   └── utils.ts
├── model/                    # Mongoose schemas
│   ├── blog.model.ts
│   ├── comment.model.ts
│   ├── reels.model.ts
│   └── user.model.ts
├── public/                   # Static assets
├── styles/                   # Tailwind and custom styles
├── types/                    # TypeScript types
├── middleware.ts
├── next-env.d.ts
├── next.config.ts
├── postcss.config.mjs
├── tsconfig.json
├── package.json
├── package-lock.json
├── eslint.config.mjs
├── components.json
└── README.md



<!-- Trigger redeploy -->
