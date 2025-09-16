# Elite Venture Capital - Portfolio Management Platform

## Overview

Elite Venture Capital is a sophisticated portfolio management platform designed for day trading and investment management. The application features a dark, professional UI inspired by premium financial platforms like Robinhood and Interactive Brokers. It provides secure user authentication, real-time portfolio tracking with compound growth simulation, and a clean dashboard interface for monitoring investment performance.

The platform is built as a full-stack web application targeting financial professionals and individual investors who need a premium interface for portfolio management and tracking.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript for type safety and modern development
- **Routing**: Wouter for lightweight client-side routing
- **UI Components**: Radix UI primitives with shadcn/ui component library for consistent, accessible design
- **Styling**: Tailwind CSS with custom design system featuring financial-grade color palette (dark theme with gold accents)
- **State Management**: React Context API for authentication state and TanStack Query for server state management
- **Form Handling**: React Hook Form with Zod validation for type-safe form management

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules for modern JavaScript features
- **Development Server**: Vite for fast development builds and HMR
- **Build System**: ESBuild for production bundling with external package handling

### Authentication System
- **Provider**: Firebase Authentication with Google OAuth integration
- **Session Management**: Firebase handles user sessions with automatic token refresh
- **User Context**: React Context provides authentication state throughout the application
- **Protected Routes**: Route-level authentication guards redirect unauthenticated users

### Database Design
- **Primary Database**: Firebase Firestore for user portfolios and real-time data
- **Schema Definition**: Drizzle ORM with PostgreSQL schema definitions (prepared for future migration)
- **Data Models**: 
  - Users table with username/password fields
  - Portfolio collection with balance, lastUpdate, and userId fields
  - Zod schemas for runtime validation

### Portfolio Management
- **Growth Simulation**: Automatic compound growth calculation (0.05% daily) to simulate trading performance
- **Update Logic**: Portfolio values update automatically when accessed after time intervals
- **Performance Metrics**: Weekly gain calculations with percentage changes
- **Data Persistence**: Real-time updates stored in Firestore with Date/Timestamp handling

### UI Design System
- **Color Scheme**: Dark theme with charcoal backgrounds (15 8% 8%) and gold accents (45 100% 35%)
- **Typography**: Inter font family with specific weights for financial data display
- **Component Library**: Complete shadcn/ui implementation with custom theming
- **Responsive Design**: Mobile-first approach with Tailwind breakpoints
- **Accessibility**: Radix UI primitives ensure WCAG compliance

## External Dependencies

### Authentication & Database
- **Firebase**: Authentication, Firestore database, and real-time data synchronization
- **Google OAuth**: Integrated through Firebase for seamless sign-in experience

### UI & Styling
- **Radix UI**: Comprehensive primitive components for accessible UI elements
- **Tailwind CSS**: Utility-first CSS framework with custom design tokens
- **Lucide React**: SVG icon library for consistent iconography
- **Google Fonts**: Inter font family for professional typography

### Development Tools
- **Vite**: Build tool and development server with React plugin
- **TypeScript**: Static type checking across the entire application
- **ESLint/Prettier**: Code quality and formatting tools
- **Drizzle Kit**: Database schema management and migrations

### Data Management
- **TanStack Query**: Server state management with caching and synchronization
- **React Hook Form**: Form state management with validation
- **Zod**: Runtime type validation and schema definition
- **Date-fns**: Date manipulation and formatting utilities

### Deployment Infrastructure
- **Replit**: Development environment with integrated deployment
- **Environment Variables**: Firebase configuration and API keys
- **Asset Management**: Static asset serving with Vite asset pipeline