# YKB Bricks - Fly Ash Brick Manufacturing Website

## Overview

This is a full-stack web application for YKB Bricks, a fly ash brick manufacturing company based in Chhotha Village, Jharkhand. The application serves as both a company website and a contact management system, featuring a modern React frontend with a Node.js/Express backend.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **Routing**: Wouter for lightweight client-side routing
- **UI Components**: Radix UI with shadcn/ui for consistent design system
- **Styling**: Tailwind CSS with custom color scheme and component variants
- **State Management**: TanStack Query for server state management
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Database**: PostgreSQL with Neon Database serverless
- **ORM**: Drizzle ORM for type-safe database operations
- **Session Management**: Connect-pg-simple for PostgreSQL session storage
- **API Design**: RESTful API with JSON responses

## Key Components

### Frontend Components
- **Landing Page**: Single-page application with multiple sections (hero, features, products, gallery, about, testimonials, contact)
- **Contact Form**: Validated form with phone, name, quantity selection, and message fields
- **UI Components**: Comprehensive component library including buttons, cards, forms, toasts, and navigation elements
- **Responsive Design**: Mobile-first approach with breakpoint-based styling

### Backend Components
- **Route Handlers**: Contact form submission and message retrieval endpoints
- **Storage Layer**: Abstracted storage interface with in-memory implementation and database-ready structure
- **Schema Validation**: Zod schemas for request/response validation
- **Error Handling**: Centralized error handling with appropriate HTTP status codes

### Database Schema
- **Users Table**: Basic user management with username/password authentication
- **Contact Messages Table**: Stores customer inquiries with name, phone, quantity, message, and timestamp
- **Type Safety**: Drizzle ORM provides compile-time type checking for database operations

## Data Flow

1. **User Interaction**: Users interact with the React frontend through form submissions and navigation
2. **Form Validation**: Client-side validation using React Hook Form and Zod schemas
3. **API Requests**: TanStack Query manages API calls to the Express backend
4. **Server Processing**: Express routes handle requests, validate data, and interact with storage
5. **Database Operations**: Drizzle ORM executes type-safe database queries
6. **Response Handling**: JSON responses sent back to frontend with success/error states
7. **UI Updates**: React components update based on API responses with toast notifications

## External Dependencies

### Frontend Dependencies
- **UI Framework**: Radix UI primitives for accessible components
- **Icons**: Lucide React for consistent iconography
- **Date Handling**: date-fns for date manipulation
- **Class Management**: clsx and tailwind-merge for conditional styling
- **Form Validation**: @hookform/resolvers for Zod integration

### Backend Dependencies
- **Database**: @neondatabase/serverless for PostgreSQL connection
- **ORM**: drizzle-orm and drizzle-zod for database operations
- **Validation**: Zod for schema validation
- **Session Storage**: connect-pg-simple for PostgreSQL sessions
- **Development**: tsx for TypeScript execution

## Deployment Strategy

### Build Process
- **Frontend**: Vite builds optimized React application to `dist/public`
- **Backend**: ESBuild bundles TypeScript server code to `dist/index.js`
- **Database Migrations**: Drizzle Kit handles schema migrations with `db:push` command

### Development Environment
- **Local Development**: Vite dev server with HMR and Express backend
- **Environment Variables**: DATABASE_URL required for database connection
- **Replit Integration**: Specialized plugins for Replit development environment

### Production Deployment
- **Static Assets**: Frontend built and served from `dist/public`
- **Server**: Node.js serves API routes and static files
- **Database**: PostgreSQL database with connection pooling
- **Environment**: Production NODE_ENV with optimized builds

The application is designed to be easily deployable on platforms like Replit, Vercel, or traditional hosting providers with PostgreSQL database support.