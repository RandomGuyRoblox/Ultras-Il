# Ultras IL - Israeli Football Fan Community Platform

## Overview

This is a Hebrew-language e-commerce platform for Israeli football (soccer) fan communities. Users can purchase staff ranks and leadership roles for their favorite teams. The application features a dark-themed, gaming-inspired UI with RTL (right-to-left) support for Hebrew text.

Key features:
- Product catalog with staff ranks and leadership roles
- Team selection for leadership purchases
- Shopping cart with Zustand state management
- Order creation and processing
- Gallery section showcasing fan culture imagery

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter (lightweight React router)
- **State Management**: 
  - Zustand for global cart state
  - TanStack React Query for server state and API caching
- **Styling**: 
  - Tailwind CSS with custom dark theme
  - shadcn/ui component library (New York style)
  - Framer Motion for animations
- **Fonts**: Chakra Petch (display/headers) and Rubik (body text)
- **RTL Support**: Full Hebrew language support with `dir="rtl"` layout

### Backend Architecture
- **Runtime**: Node.js with Express 5
- **Language**: TypeScript with ESM modules
- **API Pattern**: RESTful endpoints defined in `shared/routes.ts`
- **Validation**: Zod schemas for request/response validation
- **Build**: esbuild for server bundling, Vite for client

### Data Storage
- **Database**: PostgreSQL
- **ORM**: Drizzle ORM with drizzle-zod for schema validation
- **Schema Location**: `shared/schema.ts` (shared between client and server)
- **Tables**: products, teams, orders

### API Structure
All endpoints are prefixed with `/api`:
- `GET /api/products` - List all products (staff ranks and leadership roles)
- `GET /api/teams` - List all Israeli football teams
- `POST /api/orders` - Create a new order with cart items

### Build and Development
- **Development**: `npm run dev` runs Vite dev server with HMR
- **Production Build**: `npm run build` compiles both client and server
- **Database Migrations**: `npm run db:push` using Drizzle Kit

## External Dependencies

### Database
- **PostgreSQL**: Primary database (connection via `DATABASE_URL` environment variable)
- **connect-pg-simple**: PostgreSQL session store (available but sessions not currently implemented)

### UI Component Libraries
- **Radix UI**: Full primitive component library for accessible UI components
- **shadcn/ui**: Pre-styled component collection built on Radix
- **Embla Carousel**: For carousel/slider components
- **cmdk**: Command palette component

### Animation and Styling
- **Framer Motion**: Animation library for page transitions and micro-interactions
- **Tailwind CSS**: Utility-first CSS framework
- **class-variance-authority**: For component variant management

### Form and Validation
- **Zod**: Schema validation for API inputs/outputs
- **React Hook Form** with **@hookform/resolvers**: Form state management

### Development Tools
- **Vite**: Frontend build tool and dev server
- **esbuild**: Server bundling
- **Drizzle Kit**: Database migration tooling
- **TypeScript**: Static type checking

### Replit-Specific
- **@replit/vite-plugin-runtime-error-modal**: Error overlay for development
- **@replit/vite-plugin-cartographer**: Development tooling
- **@replit/vite-plugin-dev-banner**: Development environment indicator