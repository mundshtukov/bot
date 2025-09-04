# Overview

This is a React-based landing page project for a Telegram channel called "Крипто в тапках 🩴" (Crypto in Slippers). The application serves as a marketing landing page to promote a cryptocurrency analysis Telegram channel, featuring a modern dark theme with glassmorphism effects. The project uses a full-stack architecture with a React frontend and Express.js backend, built with TypeScript throughout.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
The frontend is built using React 18 with TypeScript, utilizing a component-based architecture. Key architectural decisions include:

- **Component Structure**: Components are organized in a modular fashion with separate files for Navigation, Hero, Problems, Solutions, TradingBot, and FinalCTA sections
- **Styling Framework**: Uses Tailwind CSS for utility-first styling with a custom design system featuring CSS variables for theming
- **UI Components**: Leverages shadcn/ui component library built on Radix UI primitives for accessible, customizable components
- **State Management**: Uses React's built-in hooks (useState, useEffect) for local component state, with React Query for server state management
- **Routing**: Implements client-side routing with Wouter as a lightweight alternative to React Router
- **Performance Optimizations**: Components are memoized using React.memo() to prevent unnecessary re-renders

## Backend Architecture
The backend follows a minimal Express.js architecture designed for simplicity:

- **Server Framework**: Express.js with TypeScript for type safety
- **Storage Layer**: Implements an abstraction pattern with IStorage interface, currently using in-memory storage (MemStorage class)
- **Route Organization**: Centralized route registration system in routes.ts
- **Development Tools**: Integrated Vite development server for hot module replacement and fast builds
- **Error Handling**: Centralized error handling middleware for consistent API responses

## Build System
- **Bundler**: Vite for fast development and optimized production builds
- **TypeScript Configuration**: Strict TypeScript settings with path aliases for clean imports
- **Asset Pipeline**: Vite handles asset optimization, code splitting, and static asset serving
- **Production Build**: Uses esbuild for server-side bundling with ESM format

## Database Architecture
The project is configured for PostgreSQL using Drizzle ORM:

- **ORM**: Drizzle ORM with TypeScript-first approach for type-safe database operations
- **Database Provider**: Configured for Neon Database (serverless PostgreSQL)
- **Schema Management**: Centralized schema definition in shared/schema.ts with Drizzle migrations
- **Type Safety**: Uses drizzle-zod for runtime validation and type inference

## Theme and Design System
- **Design Language**: Dark theme with cyan/teal primary colors and orange accents
- **Typography**: Uses Inter for body text and Orbitron for headings/monospace elements
- **Visual Effects**: Implements glassmorphism effects with backdrop blur and subtle borders
- **Responsive Design**: Mobile-first approach with Tailwind's responsive utilities

# External Dependencies

## Core Framework Dependencies
- **@neondatabase/serverless**: Serverless PostgreSQL database driver for Neon
- **drizzle-orm**: TypeScript ORM for type-safe database operations
- **express**: Web application framework for Node.js backend
- **react**: Frontend UI library with hooks-based architecture
- **vite**: Build tool and development server with hot module replacement

## UI and Styling
- **@radix-ui/react-***: Collection of accessible, unstyled UI components
- **tailwindcss**: Utility-first CSS framework for styling
- **class-variance-authority**: Utility for creating variant-based component APIs
- **clsx**: Utility for conditionally joining classNames

## Development and Build Tools
- **typescript**: Static type checking for JavaScript
- **@tanstack/react-query**: Server state management and caching
- **wouter**: Lightweight client-side routing library
- **react-hook-form**: Forms library with validation support

## External Services
- **Telegram**: The landing page promotes a Telegram channel, with direct links to join the channel
- **Google Fonts**: Uses Inter and Orbitron fonts loaded from Google Fonts CDN
- **Replit Integration**: Contains Replit-specific development tooling and banner integration