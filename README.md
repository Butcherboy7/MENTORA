# EduBuddy - AI Learning Assistant

## Overview
EduBuddy is a modern AI-powered learning assistant application built with React and Express. The application provides personalized tutoring across multiple subjects including coding, math, science, law, and history. It features an interactive chat interface with speech recognition, text-to-speech capabilities, and career guidance tools.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Styling**: Tailwind CSS with shadcn/ui component library
- **State Management**: React hooks and TanStack Query for server state
- **Routing**: React Router for client-side navigation
- **Build Tool**: Vite for fast development and optimized builds

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ESM modules
- **Database**: PostgreSQL with Drizzle ORM
- **Database Provider**: Neon Database (serverless PostgreSQL)
- **Session Storage**: PostgreSQL-based sessions using connect-pg-simple

### Key Components

#### Chat System
- Multi-modal study modes (coding, math, science, law, history, general)
- Real-time chat interface with markdown support
- Smart suggestions and follow-up questions
- Speech-to-text and text-to-speech capabilities
- Message retry and copy functionality

#### Career Guidance
- Separate career guidance page that opens in a new window
- Personalized career path recommendations
- Skills assessment and learning roadmaps
- Integration with main learning platform

#### UI Components
- Comprehensive shadcn/ui component library
- Responsive design with mobile support
- Dark/light theme support (infrastructure in place)
- Collapsible sidebar with navigation
- Toast notifications for user feedback

## Data Flow

### Client-Side Flow
1. User selects study mode and enters questions
2. Messages are sent through custom chat hooks
3. Mock responses are generated (placeholder for LLM integration)
4. UI updates with streaming-like responses
5. Smart suggestions are generated based on context

### Server-Side Flow
1. Express server handles API routes (structure in place)
2. Database operations through Drizzle ORM storage interface
3. User authentication and session management ready
4. Static file serving for production builds

## External Dependencies

### Core Libraries
- **@neondatabase/serverless**: Serverless PostgreSQL driver
- **drizzle-orm**: Type-safe database ORM
- **@tanstack/react-query**: Server state management
- **react-markdown**: Markdown rendering for chat messages
- **@radix-ui/***: Headless UI components foundation

### Development Tools
- **Vite**: Build tool with React plugin
- **esbuild**: Server-side bundling
- **TypeScript**: Type safety across the stack
- **Tailwind CSS**: Utility-first styling

### Replit Integration
- **@replit/vite-plugin-runtime-error-modal**: Development error handling
- **@replit/vite-plugin-cartographer**: Development tools integration

## Deployment Strategy

### Development
- Runs on port 5000 with Vite dev server
- Hot module replacement for rapid development
- TypeScript compilation and type checking
- PostgreSQL database provisioning through Replit

### Production
- Client builds to `dist/public` directory
- Server bundles with esbuild to `dist/index.js`
- Serves static files through Express
- Auto-scaling deployment target on Replit
- Environment-based configuration

### Database Management
- Drizzle Kit for schema migrations
- Database schema defined in TypeScript
- Connection through environment variables
- User authentication schema ready for implementation

## Changelog
- June 19, 2025. Initial setup
- June 19, 2025. Enhanced UI with left sidebar navigation and resizable code editor panels

## Recent Changes
✓ Fixed syntax errors in Index.tsx file causing app crashes
✓ Redesigned layout with collapsible left sidebar for navigation
✓ Added mouse-draggable resize functionality to code playground
✓ Moved navigation buttons to sidebar to prevent scrolling issues
✓ Implemented proper dark mode with CSS variables and localStorage persistence
✓ Made layout fully responsive for mobile devices with overlay sidebar
✓ Fixed chat window to be fixed height with proper scrolling
✓ Added Enter key functionality in code editor AI help section
✓ Improved mobile button sizing and text responsiveness
✓ Migrated from Replit Agent to standard Replit environment
✓ Integrated Google Gemini API for dynamic AI responses
✓ Enhanced speech recognition with proper microphone permissions
✓ Added collapsible AI help panel in code editor with copy functionality
✓ Implemented dynamic career guidance using Gemini LLM
✓ Fixed clear chat functionality and mobile layout optimization
✓ Enhanced code execution with improved JavaScript sandboxing and Python simulation
✓ Added comprehensive scrollbars to code editor, output panel, AI assistant, and chat window
✓ Removed PDF summarizer functionality completely per user request

## User Preferences
Preferred communication style: Simple, everyday language.
Layout preferences: Left sidebar navigation, resizable code editor panels, fixed chat window with scroll, responsive mobile design
UI preferences: Working dark mode, mobile-responsive layout, Enter key shortcuts
