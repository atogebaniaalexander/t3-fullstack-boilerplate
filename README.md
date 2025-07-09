# T3 Fullstack Boilerplate

A modern, full-stack web application boilerplate built with the [T3 Stack](https://create.t3.gg/). This project provides a solid foundation for building type-safe, scalable web applications with the best developer experience.

![T3 Fullstack Boilerplate](https://github.com/user-attachments/assets/39dafebf-89aa-42a3-9b52-58a7e82e6b08)

## 🚀 Tech Stack

This boilerplate includes the following technologies:

- **[Next.js](https://nextjs.org)** - React framework with App Router
- **[TypeScript](https://typescriptlang.org)** - Type safety across the entire stack
- **[tRPC](https://trpc.io)** - End-to-end typesafe APIs
- **[Prisma](https://prisma.io)** - Type-safe database ORM
- **[NextAuth.js](https://next-auth.js.org)** - Authentication for Next.js
- **[Tailwind CSS](https://tailwindcss.com)** - Utility-first CSS framework
- **[SQLite](https://sqlite.org)** - Lightweight database (easily configurable for other databases)

## ✨ Features

- 🔐 **Authentication** - Ready-to-use auth with NextAuth.js
- 🗄️ **Database** - Prisma ORM with SQLite (easily swappable)
- 🌐 **API** - Type-safe APIs with tRPC
- 🎨 **Styling** - Beautiful UI with Tailwind CSS
- 📱 **Responsive** - Mobile-first responsive design
- 🔧 **TypeScript** - Full type safety across the stack
- ⚡ **Performance** - Optimized with Next.js App Router
- 🚀 **Deploy Ready** - Ready to deploy to Vercel, Netlify, or Docker

## 🛠️ Getting Started

### Prerequisites

- Node.js 18+ 
- npm, yarn, or pnpm

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/atogebaniaalexander/t3-fullstack-boilerplate.git
   cd t3-fullstack-boilerplate
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   ```
   
   Edit `.env` and configure your environment variables:
   - `AUTH_SECRET` - Generate with `npx auth secret`
   - `DATABASE_URL` - Your database connection string
   - `AUTH_DISCORD_ID` & `AUTH_DISCORD_SECRET` - OAuth credentials (optional)

4. **Set up the database**
   ```bash
   npx prisma generate
   npx prisma db push
   ```
   
   > **Note:** If you encounter network issues with Prisma during development, you can temporarily use `SKIP_ENV_VALIDATION=1 npm run dev` to run the development server while working on the setup.

5. **Start the development server**
   ```bash
   npm run dev
   ```

Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

## 📝 Available Scripts

- `npm run dev` - Start development server with Turbopack
- `npm run build` - Build the application for production
- `npm run start` - Start the production server
- `npm run typecheck` - Run TypeScript type checking
- `npm run db:generate` - Generate Prisma client
- `npm run db:push` - Push database schema changes
- `npm run db:studio` - Open Prisma Studio

## 🗄️ Database

This boilerplate comes with a pre-configured Prisma schema that includes:

- **User management** - User accounts with profile information
- **Authentication** - Account linking and session management
- **Posts** - Example post model with user relationships

### Changing Database Provider

The project uses SQLite by default, but you can easily switch to PostgreSQL, MySQL, or other supported databases:

1. Update the `provider` in `prisma/schema.prisma`
2. Update the `DATABASE_URL` in your `.env` file
3. Run `npx prisma db push` to apply changes

## 🔐 Authentication

Authentication is handled by NextAuth.js with the following features:

- **Multiple Providers** - Discord provider included (easily extensible)
- **Database Sessions** - Secure session management with Prisma
- **Type Safety** - Full TypeScript support for auth

### Adding OAuth Providers

1. Install the provider package if needed
2. Add credentials to your `.env` file
3. Configure the provider in `src/server/auth/config.ts`

## 🌐 API Routes

The project uses tRPC for type-safe API routes:

- **Type Safety** - End-to-end type safety from client to server
- **Automatic Validation** - Input validation with Zod
- **Real-time Updates** - Built-in support for subscriptions

Example API routes are included in `src/server/api/routers/`.

## 🎨 Styling

Tailwind CSS is configured and ready to use:

- **Utility Classes** - Comprehensive utility-first CSS framework
- **Responsive Design** - Mobile-first responsive breakpoints
- **Custom Configuration** - Easily customizable design system

## 🚀 Deployment

### Vercel (Recommended)

1. Push your code to GitHub
2. Connect your repository to [Vercel](https://vercel.com)
3. Configure environment variables in Vercel dashboard
4. Deploy!

### Other Platforms

This project can be deployed to any platform that supports Node.js:

- **Netlify** - Configure build command as `npm run build`
- **Railway** - Connect your GitHub repository
- **Docker** - Use the included Docker configuration (if available)

## 📚 Learn More

- [T3 Stack Documentation](https://create.t3.gg/)
- [Next.js Documentation](https://nextjs.org/docs)
- [tRPC Documentation](https://trpc.io/docs)
- [Prisma Documentation](https://www.prisma.io/docs)
- [NextAuth.js Documentation](https://next-auth.js.org)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

Built with ❤️ using the T3 Stack
