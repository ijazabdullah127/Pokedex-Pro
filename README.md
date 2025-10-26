# 🎮 PokéDex Pro - Ultimate Pokémon Encyclopedia

A comprehensive, modern Pokémon encyclopedia built with React, TypeScript, and Tailwind CSS. Features advanced search, team building, battle simulation, and much more!

![PokéDex Pro](https://img.shields.io/badge/Pokemon-Encyclopedia-blue?style=for-the-badge&logo=pokemon)
![React](https://img.shields.io/badge/React-18.2.0-61DAFB?style=for-the-badge&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0.2-3178C6?style=for-the-badge&logo=typescript)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.3.0-38B2AC?style=for-the-badge&logo=tailwind-css)

## ✨ Features

### 🔍 **Complete Pokédex**
- Browse all 1000+ Pokémon with high-quality artwork
- Advanced search and filtering by type, generation, stats
- Infinite scroll pagination for smooth browsing
- Detailed Pokémon information including stats, abilities, moves

### 👥 **Team Builder**
- Create and customize teams of up to 6 Pokémon
- Set custom nicknames, levels, and movesets
- Team composition analysis and type coverage
- Export/import team configurations

### ⚔️ **Battle Simulator**
- Turn-based battle system with dynamic AI opponents
- Real-time battle log with elegant animations
- Team member status panels with visual HP indicators
- Actual Pokemon move names and damage calculations
- Fainted Pokemon visual indicators (opacity/grayscale)
- Dynamic AI team generation with random Pokemon and moves

### 📊 **Type Effectiveness Chart**
- Interactive type matchup reference
- Visual effectiveness indicators
- Click-to-highlight specific type interactions
- Mobile-friendly responsive design

### 🔄 **Pokémon Comparison**
- Side-by-side stat comparisons for up to 4 Pokémon
- Visual stat bars and effectiveness analysis
- Type matchup comparisons
- Battle readiness assessment

### ❤️ **Favorites & Collections**
- Save favorite Pokémon for quick access
- Recently viewed Pokémon history
- Personal collection management
- Sync across browser sessions

### 🎨 **Modern UI/UX**
- Dark/Light theme toggle with system preference detection
- Smooth animations and transitions with Framer Motion
- Fully responsive design for all screen sizes
- Accessibility-first approach with ARIA labels
- Progressive Web App (PWA) capabilities

### 🚀 **Performance & Technical**
- Intelligent caching with React Query
- Optimized API calls to PokéAPI
- Image lazy loading and optimization
- TypeScript for type safety
- Error boundaries for graceful error handling

## 🛠️ Tech Stack

- **Frontend Framework**: React 18.2.0
- **Language**: TypeScript 5.0.2
- **Styling**: Tailwind CSS 3.3.0
- **State Management**: Zustand + React Context
- **Data Fetching**: React Query (TanStack Query)
- **Animations**: Framer Motion
- **Icons**: Lucide React
- **Build Tool**: Vite 4.4.5
- **API**: PokéAPI v2

## 🚀 Quick Start

### Prerequisites
- Node.js 16.0 or higher
- npm or yarn package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/ijazabdullah127/pokedex-pro.git
   cd pokedex-pro
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Start development server**
   ```bash
   npm run dev
   # or
   yarn dev
   ```

4. **Open your browser**
   Navigate to `http://localhost:3000`

### Build for Production

```bash
npm run build
# or
yarn build
```

The built files will be in the `dist` directory.

## 📁 Project Structure

```
src/
├── components/           # Reusable UI components
│   ├── common/          # Generic components (PokemonCard, ErrorBoundary)
│   └── layout/          # Layout components (Navbar, Footer)
├── contexts/            # React Context providers
│   ├── PokemonContext.tsx    # Pokemon state management
│   └── ThemeContext.tsx      # Theme switching
├── hooks/               # Custom React hooks
│   └── usePokemonData.ts     # Pokemon data fetching hooks
├── pages/               # Page components
│   ├── Home.tsx         # Landing page
│   ├── PokemonList.tsx  # Pokemon browsing
│   ├── PokemonDetail.tsx # Individual Pokemon details
│   ├── TeamBuilder.tsx  # Team creation
│   ├── BattleSimulator.tsx # Battle system
│   ├── TypeChart.tsx    # Type effectiveness
│   ├── Compare.tsx      # Pokemon comparison
│   └── Favorites.tsx    # Favorite Pokemon
├── services/            # API and external services
│   └── pokemonApi.ts    # PokéAPI integration
├── types/               # TypeScript type definitions
│   └── pokemon.ts       # Pokemon-related types
├── utils/               # Utility functions
│   └── typeColors.ts    # Type color mappings
├── App.tsx              # Main app component
├── main.tsx             # App entry point
└── index.css            # Global styles
```

## 🎯 Key Features Explained

### Smart Caching System
The app implements intelligent caching to minimize API calls:
- 5-minute cache for individual Pokémon data
- 10-minute cache for lists and static data
- Automatic cache invalidation and refresh
- Offline-first approach with stale-while-revalidate

### Responsive Design
Built mobile-first with breakpoints:
- **Mobile**: < 640px (1 column layouts)
- **Tablet**: 640px - 1024px (2-3 column layouts)
- **Desktop**: > 1024px (4-5 column layouts)
- **Large Desktop**: > 1280px (optimized spacing)

### Accessibility Features
- Semantic HTML structure
- ARIA labels and roles
- Keyboard navigation support
- Screen reader compatibility
- High contrast mode support
- Focus management

### Performance Optimizations
- Code splitting with React.lazy()
- Image lazy loading
- Virtual scrolling for large lists
- Debounced search inputs
- Memoized expensive calculations
- Bundle size optimization

## 🔧 Configuration

### Environment Variables
Create a `.env` file in the root directory:

```env
# API Configuration
VITE_POKEMON_API_BASE_URL=https://pokeapi.co/api/v2
VITE_APP_TITLE=PokéDex Pro
VITE_APP_DESCRIPTION=Ultimate Pokémon Encyclopedia

# Feature Flags
VITE_ENABLE_BATTLE_SIMULATOR=false
VITE_ENABLE_ANALYTICS=false
```

### Customization
The app is highly customizable through:
- **Tailwind Config**: Modify `tailwind.config.js` for colors and themes
- **Type Colors**: Update `src/utils/typeColors.ts` for Pokemon type styling
- **API Settings**: Configure caching and endpoints in `src/services/pokemonApi.ts`

## 🧪 Testing

```bash
# Run unit tests
npm run test

# Run tests with coverage
npm run test:coverage

# Run E2E tests
npm run test:e2e
```

## 📱 PWA Features

The app includes Progressive Web App capabilities:
- Offline functionality
- Install prompt for mobile devices
- Background sync for favorites
- Push notifications (optional)
- App-like experience on mobile

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

### Development Workflow
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code Style
- Use TypeScript for all new code
- Follow the existing code style (Prettier + ESLint)
- Write meaningful commit messages
- Add JSDoc comments for functions
- Include unit tests for new features

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **PokéAPI**: Amazing free API providing all Pokémon data
- **Pokémon Company**: For creating the wonderful world of Pokémon
- **React Community**: For the excellent ecosystem and tools
- **Tailwind CSS**: For the utility-first CSS framework
- **Framer Motion**: For smooth animations and transitions

## 🐛 Bug Reports & Feature Requests

Please use the [GitHub Issues](https://github.com/ijazabdullah127/pokedex-pro/issues) page to:
- Report bugs
- Request new features
- Ask questions
- Share feedback

## 📊 Roadmap

### Version 2.0 (Coming Soon)
- [x] Battle Simulator with AI ✅
- [ ] Multiplayer battles
- [ ] Pokemon breeding calculator
- [ ] Advanced move damage calculator
- [ ] Team synergy analysis
- [ ] Export teams to Pokemon Showdown

### Version 2.1
- [ ] Pokemon location maps
- [ ] Shiny Pokemon gallery
- [ ] Evolution requirements guide
- [ ] Pokemon size comparisons
- [ ] Sound effects and music

### Version 3.0
- [ ] User accounts and cloud sync
- [ ] Community features
- [ ] Tournament brackets
- [ ] Achievement system
- [ ] Pokemon trading simulator

## 📞 Contact

**Developer**: Abdullah Ijaz
**GitHub**: [@ijazabdullah127](https://github.com/ijazabdullah127)  
**Project Link**: [https://github.com/ijazabdullah127/pokedex-pro](https://github.com/ijazabdullah127/pokedex-pro)

---

<div align="center">
  <p>Made with ❤️ for Pokémon trainers everywhere. Star ⭐ this repo Thanks</p>
  <p>
    <a href="#top">Back to Top ⬆️</a>
  </p>
</div>
