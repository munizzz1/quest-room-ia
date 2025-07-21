# Question Room IA
This project allows you to create rooms where you can ask questions that are answered instantly by artificial intelligence, all based on the context of recorded audio.

## Back-end

### Technologies
- **Node.js** with native TypeScript (experimental strip types)
- **Fastify** - Framework web
- **PostgreSQL** with **pgvector** extension for vectors
- **Drizzle ORM** - Type-safe database operations
- **Zod** - Schema validation
- **Docker** - Database containerization
- **Biome** - Linting and code formatting

### ⚙️ Setup and Configuration
### Prerequisites

- Node.js (version supporting `--experimental-strip-types`)
- Docker e Docker Compose

### Installation

### 1. Clone the repository
```bash
git clone <repository-url>
cd server
```

### 2. Configure the database
```bash
docker-compose up -d
```

### 3. Configure environment variables

Create a `.env` file in the project root:

```env
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
```

### 4. Install dependencies
```bash
npm install
```

### 5. Perform database migrations
```bash
npx drizzle-kit migrate
```

### 6. (Opcional) Populate the database with sample data
```bash
npm run db:seed
```

### 7. Run the project

**Development:**
```bash
npm run dev
```

**Production:**
```bash
npm start
```

## Front-end
### Technologies
- **React 19.1** - Library for user interfaces
- **TypeScript 5.8** - Statically Typed JavaScript Superset
- **Vite 7.0** - Build tool and development server
- **TailwindCSS 4.1** - Framework CSS utility-first
- **React Router Dom 7.6** - Routing Library
- **TanStack React Query 5.8** - Server state and cache management
- **Shadcn/ui** - Component system
- **Lucide React** - Icon library

### ⚙️ Setup and Configuration
### Prerequisites
- Node.js (version 18 or higher)
- npm ou yarn

### Installation
1. Install dependencies:
   ```bash
   npm install
   ```

3. Run the development server:
   ```bash
   npm run dev
   ```

4. Access the application at `http://localhost:5173`

### Available Scripts

- `npm run dev` - Start the development server
- `npm run build` - Generates production build
- `npm run preview` - Production Build Preview

### Backend

The project consumes an API that must be running on port 3333. Make sure the backend is configured and running before starting the frontend.

## 🛠️ Project Structure

```
src/
├── components/ui/    # Interface Components
├── pages/           # Application pages
├── lib/             # Utilities and settings
└── app.tsx          # Root component
``` 
