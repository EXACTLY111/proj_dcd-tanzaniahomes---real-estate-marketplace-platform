# TanzaniaHomes - Real Estate Marketplace Platform

A comprehensive real estate marketplace platform for Tanzania, starting with Dodoma as the pilot market. The platform enables property owners and agents to list properties while allowing buyers to browse and contact sellers directly via WhatsApp integration. Features include admin verification system, commission-based monetization, and mobile-first design optimized for emerging markets.

## 🏗️ Project Overview

TanzaniaHomes is a modern, mobile-first real estate platform designed specifically for the Tanzanian market. The platform addresses the unique challenges of real estate transactions in emerging markets by integrating with WhatsApp, implementing rigorous admin verification for listings, and providing a seamless mobile experience.

### Key Features

- **Property Listings**: Comprehensive property search and filtering system
- **WhatsApp Integration**: Direct communication between buyers and sellers via WhatsApp
- **Admin Verification**: Quality control through centralized property verification
- **Mobile-First Design**: Optimized for mobile devices with responsive layouts
- **Multi-Language Support**: Support for English and Swahili
- **Commission Tracking**: Built-in system for tracking successful transactions
- **City-Based Architecture**: Scalable structure starting with Dodoma

## 🚀 Technology Stack

### Frontend
- **Next.js 14** - React framework with App Router
- **TypeScript** - Type-safe development
- **React 18** - Latest React features including Server Components
- **Tailwind CSS** - Utility-first CSS framework (to be configured)

### Backend
- **Python/FastAPI** - High-performance Python backend
- **PostgreSQL** - Primary database
- **Redis** - Caching and session management
- **Prisma** - Type-safe database ORM

### DevOps & Tools
- **Docker** - Containerization
- **Kubernetes** - Container orchestration
- **GitHub Actions** - CI/CD pipelines
- **Sentry** - Error tracking and monitoring
- **Vercel** - Frontend deployment

### Code Quality
- **ESLint** - Code linting for JavaScript/TypeScript
- **Prettier** - Code formatting
- **Husky** - Git hooks for pre-commit checks
- **lint-staged** - Run linters on staged files

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** >= 18.0.0
- **npm** >= 9.0.0
- **PostgreSQL** >= 14
- **Redis** >= 6.0
- **Docker** (optional, for containerized development)

## 🛠️ Getting Started

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd proj_dcd-tanzaniahomes---real-estate-marketplace-platform
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env.local
   ```
   Then edit `.env.local` with your configuration values.

4. **Set up the database**
   ```bash
   # Run database migrations
   npx prisma migrate dev

   # Seed the database (optional)
   npx prisma db seed
   ```

5. **Install Husky hooks**
   ```bash
   npm run prepare
   ```

### Development

Start the development server:

```bash
npm run dev
```

The application will be available at [http://localhost:3000](http://localhost:3000)

### Building for Production

```bash
# Build the application
npm run build

# Start the production server
npm start
```

## 📝 Available Scripts

- `npm run dev` - Start development server with hot reload
- `npm run build` - Build the application for production
- `npm start` - Start production server
- `npm run lint` - Run ESLint to check code quality
- `npm run type-check` - Run TypeScript compiler checks without emitting files
- `npm run format` - Format code using Prettier
- `npm run format:check` - Check if code is properly formatted

## 🏛️ Project Architecture

### Directory Structure

```
proj_dcd-tanzaniahomes/
├── src/
│   ├── app/              # Next.js App Router pages
│   │   ├── [city]/       # City-specific routes
│   │   ├── admin/        # Admin dashboard
│   │   ├── auth/         # Authentication pages
│   │   └── api/          # API routes
│   ├── components/       # React components
│   │   ├── ui/           # Reusable UI components
│   │   ├── property/     # Property-related components
│   │   ├── admin/        # Admin components
│   │   └── auth/         # Authentication components
│   ├── lib/              # Utility functions and configurations
│   ├── hooks/            # Custom React hooks
│   ├── types/            # TypeScript type definitions
│   ├── data/             # Static data (locations, amenities)
│   └── styles/           # Global styles
├── backend/              # Python/FastAPI backend
├── prisma/               # Database schema and migrations
├── public/               # Static assets
└── docs/                 # Documentation

```

### Key Architectural Decisions

1. **Mobile-First Approach**: All components and layouts prioritize mobile experience
2. **City-Based Routing**: URLs structured as `/[city]/properties` for easy expansion
3. **Admin Verification**: Centralized trust mechanism for marketplace quality control
4. **WhatsApp Integration**: Leverages existing user behavior in the target market
5. **Progressive Enhancement**: Core functionality works without JavaScript

## 🔐 Environment Variables

See `.env.example` for a complete list of required environment variables. Key variables include:

- `DATABASE_URL` - PostgreSQL connection string
- `NEXTAUTH_URL` - NextAuth.js URL for authentication
- `NEXTAUTH_SECRET` - Secret for session encryption
- `CLOUDINARY_*` - Image upload and optimization
- `WHATSAPP_API_*` - WhatsApp integration credentials
- `REDIS_URL` - Redis connection string

## 🧪 Testing

```bash
# Run all tests
npm test

# Run tests in watch mode
npm run test:watch

# Run tests with coverage
npm run test:coverage
```

## 📦 Deployment

### Vercel (Frontend)

The frontend is configured for easy deployment to Vercel:

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel
```

### Docker

Build and run with Docker:

```bash
# Build the image
docker build -t tanzaniahomes .

# Run the container
docker run -p 3000:3000 tanzaniahomes
```

### Kubernetes

Deploy to Kubernetes cluster:

```bash
kubectl apply -f k8s/
```

## 🤝 Contributing

We welcome contributions! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code Style

- Follow the ESLint and Prettier configurations
- Write meaningful commit messages
- Add tests for new features
- Update documentation as needed

### Pre-commit Checks

The project uses Husky and lint-staged to run checks before commits:
- TypeScript compilation
- ESLint linting
- Prettier formatting

## 📄 License

This project is proprietary and confidential.

## 👥 Team

- Development Team
- Product Management
- Design Team

## 📞 Support

For support, email support@tanzaniahomes.co.tz or open an issue in the repository.

## 🗺️ Roadmap

### Phase 1: Dodoma Pilot (Current)
- [ ] Core property listing functionality
- [ ] Admin verification system
- [ ] WhatsApp integration
- [ ] Mobile-optimized UI

### Phase 2: Expansion
- [ ] Additional cities (Dar es Salaam, Arusha, Mwanza)
- [ ] Enhanced search and filtering
- [ ] User reviews and ratings
- [ ] Advanced analytics dashboard

### Phase 3: Advanced Features
- [ ] Property valuation tools
- [ ] Mortgage calculator
- [ ] Virtual property tours
- [ ] Multi-currency support

## 🙏 Acknowledgments

- Next.js team for the excellent framework
- Vercel for hosting and deployment platform
- All contributors and supporters of this project
