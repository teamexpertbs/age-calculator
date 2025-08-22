# Overview

This is a full-stack web application built as an age calculator. The application allows users to input their birth date and calculates their age in years, months, and days, along with additional statistics like total days, hours, and minutes lived. The frontend is built with React and TypeScript, featuring a modern UI with Tailwind CSS and shadcn/ui components. The backend uses Express.js with TypeScript, and the application is configured for deployment on Replit.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript for type safety and modern development
- **Routing**: Wouter for lightweight client-side routing
- **Styling**: Tailwind CSS with custom CSS variables for theming and shadcn/ui component library for consistent, accessible UI components
- **State Management**: TanStack Query (React Query) for server state management and caching
- **Form Handling**: React Hook Form with Zod validation for type-safe form validation
- **Build Tool**: Vite for fast development and optimized production builds

The frontend follows a component-based architecture with clear separation between UI components (`/components/ui/`), business logic components (`/components/`), and pages (`/pages/`). The age calculation logic is isolated in utility functions for testability and reusability.

## Backend Architecture
- **Framework**: Express.js with TypeScript for robust server-side development
- **Architecture Pattern**: RESTful API design with modular route registration
- **Storage Interface**: Abstract storage interface (`IStorage`) with in-memory implementation (`MemStorage`) for development, designed to easily swap to database implementations
- **Request Handling**: Express middleware for JSON parsing, URL encoding, and comprehensive request/response logging
- **Error Handling**: Centralized error handling middleware with proper HTTP status codes

The backend uses a clean architecture approach with separated concerns: routes for HTTP handling, storage interface for data persistence abstraction, and middleware for cross-cutting concerns.

## Development Environment
- **Monorepo Structure**: Client and server code in separate directories with shared TypeScript configurations and schemas
- **Hot Reloading**: Vite dev server with HMR for frontend, tsx for backend development with auto-restart
- **Development Middleware**: Vite middleware integration in development mode for seamless full-stack development
- **Static Serving**: Production-ready static file serving with proper fallback handling for SPA routing

## External Dependencies

### Database & ORM
- **Drizzle ORM**: Type-safe database toolkit with PostgreSQL dialect configured
- **Neon Database**: Serverless PostgreSQL database (@neondatabase/serverless) for production data storage
- **Connection Pooling**: Built-in connection management through Neon's serverless driver

### UI & Styling
- **Radix UI**: Comprehensive set of accessible, unstyled UI primitives for building the component system
- **Tailwind CSS**: Utility-first CSS framework with custom design system configuration
- **Lucide React**: Icon library providing consistent iconography throughout the application
- **Class Variance Authority**: Utility for creating variant-based component APIs

### Development Tools
- **TypeScript**: Full-stack type safety with shared types between client and server
- **ESBuild**: Fast JavaScript bundler for production server builds
- **PostCSS**: CSS processing with Tailwind CSS and Autoprefixer plugins
- **Replit Integration**: Custom Vite plugins for Replit development environment compatibility