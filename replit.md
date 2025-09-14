# StoryCanvas - 8-Week Writing Challenge

*Where your story comes to life*  
*Featured by DahTruth.com*

## Overview

StoryCanvas is a comprehensive writing application designed to support writers through an 8-week novel challenge. The platform provides a complete writing ecosystem with progress tracking, goal management, chapter organization, and export capabilities. Built as a full-stack application, it helps writers stay motivated and organized throughout their novel-writing journey with features like writing sessions, daily goals, achievement systems, and calendar-based progress visualization.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
The client-side is built with React and TypeScript, utilizing modern development patterns:
- **React with TypeScript**: Main UI framework with strict type safety
- **Wouter**: Lightweight routing library for single-page application navigation
- **TanStack React Query**: Server state management and data synchronization
- **Shadcn/ui + Radix UI**: Comprehensive component library built on Radix primitives
- **Tailwind CSS**: Utility-first CSS framework with custom design system
- **Vite**: Fast development server and build tool with hot module replacement

The application follows a component-based architecture with clear separation of concerns. Pages are organized by feature (dashboard, write, chapters, calendar, export), and reusable components are modularized in the UI directory.

### Backend Architecture  
The server-side implements a REST API using Express.js with TypeScript:
- **Express.js**: Web framework handling HTTP requests and middleware
- **TypeScript**: Full type safety across the backend codebase
- **Storage Layer**: Abstract interface pattern allowing for multiple storage implementations
- **Route Organization**: Modular route definitions with clear endpoint structure
- **Error Handling**: Centralized error handling with consistent response formats

The backend uses an interface-based storage pattern, making it database-agnostic while providing a clean API for data operations.

### Data Storage Strategy
The application uses a PostgreSQL database with a modern ORM approach:
- **Drizzle ORM**: Type-safe database operations with automatic migrations
- **PostgreSQL**: Primary database using Neon serverless hosting
- **Schema Management**: Centralized schema definitions with Zod validation
- **Migration System**: Automated database schema evolution

The database schema supports complex relationships between users, novels, chapters, writing sessions, daily goals, and achievements.

### State Management Pattern
The application implements a hybrid state management approach:
- **Server State**: Managed by TanStack React Query with automatic caching and synchronization  
- **Client State**: Local React state for UI interactions and form handling
- **Form State**: React Hook Form with Zod validation for type-safe form handling

This approach reduces complexity while ensuring data consistency and optimal performance.

### Component Architecture
The UI follows the Compound Component pattern with Shadcn/ui:
- **Design System**: Consistent theming with CSS custom properties
- **Component Variants**: Class Variance Authority for component styling variations
- **Accessibility**: Built-in ARIA support through Radix UI primitives
- **Responsive Design**: Mobile-first approach with responsive breakpoints

Components are organized hierarchically with clear prop interfaces and consistent naming conventions.

## External Dependencies

### Database & Hosting
- **Neon Database**: Serverless PostgreSQL hosting with connection pooling
- **Replit**: Development and deployment platform with integrated tooling

### UI & Styling
- **Shadcn/ui**: Pre-built accessible components
- **Radix UI**: Headless component primitives
- **Tailwind CSS**: Utility-first CSS framework
- **Lucide React**: Consistent icon library

### State & Data Management  
- **TanStack React Query**: Server state management with caching
- **React Hook Form**: Form state management and validation
- **Zod**: Runtime type validation and schema definition

### Development Tools
- **Vite**: Development server and build system
- **TypeScript**: Static type checking
- **ESBuild**: Fast JavaScript bundling for production builds

### Third-party Integrations
- **Date-fns**: Date manipulation and formatting utilities
- **Class Variance Authority**: Component styling variant management
- **Embla Carousel**: Carousel component functionality

The architecture prioritizes developer experience with hot reloading, type safety, and modern tooling while maintaining production-ready performance and scalability.