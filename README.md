# Lumen - Cinematic Movie Tracker

A beautiful glassmorphism movie tracker powered by the Trakt API. Discover trending and popular movies, manage your watchlist, track watched history, and get personalized recommendations.

![Lumen Screenshot](public/opengraph-image-p98pqg.png) <!-- You may want to add an actual screenshot -->

## Features

- 🎬 **Trending Movies**: See what the world is watching right now
- 🌟 **Popular Movies**: Browse the most popular films
- 🔍 **Movie Search**: Search for any movie title
- 📋 **Watchlist**: Save movies to watch later (requires Trakt account)
- 👁️ **Watched History**: Track movies you've watched (requires Trakt account)
- 💡 **Personalized Recommendations**: Get movie suggestions based on your taste (requires Trakt account)
- 🎨 **Glassmorphism UI**: Stunning frosted glass design with smooth animations
- 📱 **Responsive**: Works on desktop and mobile devices
- 🔐 **Secure**: Your Trakt API key is stored only in your browser

## Tech Stack

- **Framework**: React 18 with Vite
- **Language**: TypeScript
- **State Management**: TanStack React Query
- **Routing**: React Router DOM
- **Styling**: TailwindCSS with custom glassmorphism effects
- **UI Components**: Shadcn/ui (Radix UI primitives)
- **Icons**: Lucide React
- **Forms**: React Hook Form with Zod validation
- **Data Fetching**: Custom Trakt API integration
- **Notifications**: Sonner toast notifications
- **Testing**: Vitest

## Getting Started

### Prerequisites

- Node.js (v18 or higher)
- npm or bun
- A [Trakt.tv](https://trakt.tv/) account (free)

### Installation

1. Clone the repository
```bash
git clone <repository-url>
cd shimmer-show-tracer-main
```

2. Install dependencies
```bash
# Using npm
npm install

# Or using bun
bun install
```

3. Get your Trakt API credentials:
   - Go to [Trakt API Applications](https://trakt.tv/oauth/applications)
   - Create a new application
   - Set the redirect URI to `http://localhost:5173/callback` (for development)
   - Note your Client ID and Client Secret

4. Create a `.env` file in the root directory:
```env
VITE_TRAKT_CLIENT_ID=your_client_id_here
VITE_TRAKT_CLIENT_SECRET=your_client_secret_here
```

5. Start the development server
```bash
# Using npm
npm run dev

# Or using bun
bun run dev
```

6. Open your browser to `http://localhost:5173`

## Building for Production

```bash
# For production build
npm run build

# For development build (with sourcemaps)
npm run build:dev

# Preview the production build
npm run preview
```

## Project Structure

```
src/
├── components/     # Reusable UI components
├── hooks/          # Custom React hooks
├── lib/            # Trakt API integration and utilities
├── pages/          # Page components (Index, Callback, NotFound)
├── App.tsx         # Main app component with routing
├── main.tsx        # Entry point
└── index.css       # Global styles
```

## API Integration

This project uses the [Trakt API](https://trakt.docs.apiary.io/) to fetch movie data. The API integration is handled in `src/lib/trakt.ts` and includes:

- Trending movies endpoint
- Popular movies endpoint
- Movie search functionality
- User authentication (device flow)
- Watchlist management
- Watched history tracking
- Personalized recommendations

## Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `VITE_TRAKT_CLIENT_ID` | Your Trakt application Client ID | Yes |
| `VITE_TRAKT_CLIENT_SECRET` | Your Trakt application Client Secret | Yes |

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run build:dev` - Build for development (with sourcemaps)
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint
- `npm run test` - Run tests
- `npm run test:watch` - Run tests in watch mode

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgements

- [Trakt.tv](https://trakt.tv/) for providing the movie and TV show data
- [Shadcn/ui](https://ui.shadcn.com/) for the beautiful UI components
- [TailwindCSS](https://tailwindcss.com/) for the utility-first CSS framework
- [Lucide](https://lucide.dev/) for the icons
- [Sonner](https://sonner.emilkowal.ski/) for the toast notifications
- [TanStack Query](https://tanstack.com/query) for the data fetching and state management

---

Made with ❤️ for movie lovers