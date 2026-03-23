# 📚 Book Library System (ReadingHub)

A modern, professional book library web application that allows users to discover, search, and explore books across multiple categories. Built with cutting-edge technologies and best practices in web development.

## 🎯 Project Overview

ReadingHub is a full-featured book discovery platform that integrates with the Google Books API to provide real-time access to a vast collection of books. The application offers a seamless user experience with support for multiple languages, dark/light themes, and responsive design.

## ✨ Key Features

### 📖 Core Functionality
- **Multi-Category Browse**: Explore books across 6+ categories including Art, Biography, Fiction, History, Medical, Poetry, Science, and Technology
- **Google Books Integration**: Real-time book data fetching with detailed book information (title, authors, publisher, ratings, descriptions, and cover images)
- **Book Details Page**: Comprehensive view of individual books with ratings, descriptions, page count, publication date, and preview links
- **Smart Search**: Built-in search functionality to discover books by title or keywords
- **Attractive UI**: Modern carousel and grid layouts for browsing books by category

### 🌐 Internationalization
- **Multi-Language Support**: Full support for English and Vietnamese
- **Browser Language Detection**: Automatic detection of user's preferred language
- **Persistent Language Selection**: User language preferences saved in localStorage

### 🎨 User Experience
- **Dark Mode Support**: Toggle between light and dark themes with persistent preference storage
- **Smooth Animations**: Page transitions with fade effects using React Transition Group
- **Responsive Design**: Fully responsive interface that works seamlessly across all devices
- **Lazy Loading**: Code splitting for optimal performance with lazy-loaded routes
- **Loading States**: Suspense boundaries for better loading experience

### 🏗️ Technical Excellence
- **Strict TypeScript**: Full type safety throughout the application
- **Component Architecture**: Well-organized component structure with separation of concerns
- **API Abstraction**: Centralized API client with Axios for clean HTTP management
- **CSS-in-Utility**: Tailwind CSS for maintainable and scalable styling
- **ESLint Integration**: Code quality enforcement and consistent code style

## 🚀 Technology Stack

### Frontend Framework
- **React 19** - Latest React version with improved performance
- **TypeScript 5.7** - Full type safety and better IDE support
- **Vite 6** - Lightning-fast build tool and dev server

### UI & Styling
- **Tailwind CSS 4** - Utility-first CSS framework
- **React Icons** - Comprehensive icon library
- **Motion** - Smooth animations and transitions
- **React Transition Group** - Advanced page transition effects
- **Swiper** - Carousel and slider component

### State Management & Routing
- **React Router DOM v7** - Modern client-side routing
- **React Context API** - Lightweight state management

### API & Data
- **Axios** - Promise-based HTTP client
- **Google Books API** - Real-time book data source

### Internationalization
- **i18next** - Powerful internationalization framework
- **react-i18next** - React binding for i18next
- **i18next-browser-languagedetector** - Automatic language detection

### Development Tools
- **ESLint 9** - Code linting and quality checks
- **typescript-eslint** - TypeScript-specific linting rules

## 📁 Project Structure

```
src/
├── api/                          # API integration layer
│   ├── axiosClient.ts           # Axios configuration
│   └── googleBooks.api.ts       # Google Books API endpoints
├── components/
│   ├── BookSections/            # Category-specific book sections
│   │   ├── ArtSection.tsx
│   │   ├── BiographySection.tsx
│   │   ├── BookCard.tsx         # Reusable book card component
│   │   ├── BookDetail.tsx       # Book detail modal/page
│   │   └── ...other sections
│   └── layout/                   # Layout components
│       ├── Header.tsx           # Navigation header
│       ├── Footer.tsx           # Footer component
│       ├── Banner.tsx           # Promotional banner
│       └── MainLayout.tsx       # Main layout wrapper
├── data/                         # Static data
│   ├── banner.ts               # Banner content
│   ├── categories.ts           # Category definitions
│   └── navLinks.ts             # Navigation links
├── hooks/                        # Custom React hooks
│   └── useDarkMode.ts          # Dark mode toggle hook
├── locales/                      # i18n translations
│   ├── en/                      # English translations
│   └── vi/                      # Vietnamese translations
├── pages/
│   ├── auth/                    # Authentication pages (expandable)
│   │   ├── Login.tsx
│   │   └── Register.tsx
│   └── main/                    # Main application pages
│       ├── Home.tsx            # Home page
│       ├── About.tsx           # About page
│       ├── Contact.tsx         # Contact page
│       ├── BookDetail.tsx      # Individual book details
│       ├── Shop.tsx            # Shop page (expandable)
│       └── NotFound.tsx        # 404 page
├── routes/                       # Route configuration
│   └── Routes.tsx              # Route definitions
├── types/                        # TypeScript type definitions
│   ├── api.ts                  # API types
│   ├── common.ts               # Common types
│   ├── googleBooks.types.ts    # Google Books API types
│   └── ...other types
├── App.tsx                       # Root component
├── main.tsx                      # Application entry point
└── i18n.ts                       # Internationalization setup
```

## 🎓 Development Practices

### Type Safety
- Complete TypeScript implementation across all files
- Strict type definitions for API responses
- Proper typing for React hooks and components

### Component Design
- Functional components with React Hooks
- Reusable component architecture
- Lazy loading for route-based code splitting
- Clear separation between container and presentational components

### Performance Optimization
- Code splitting with lazy routes
- Image optimization with modern formats (AVIF)
- Efficient component rendering with React 19
- Asset minification and bundling with Vite

### Code Quality
- ESLint configuration for code standards
- Consistent code style with TypeScript
- Modular API layer for maintainability
- Clean component organization

## 🛠️ Installation & Setup

### Prerequisites
- Node.js (v18 or higher)
- npm or yarn package manager

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd book-library-system
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Configuration**
   Create a `.env` file in the root directory:
   ```env
   VITE_API_BASE_URL=https://www.googleapis.com/books/v1
   ```

4. **Development Server**
   ```bash
   npm run dev
   ```
   The application will be available at `http://localhost:5173`

5. **Build for Production**
   ```bash
   npm run build
   ```

6. **Preview Production Build**
   ```bash
   npm run preview
   ```

## 📝 Available Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server with hot reload |
| `npm run build` | Build for production (TypeScript compilation + Vite bundling) |
| `npm run lint` | Run ESLint to check code quality |
| `npm run preview` | Preview the production build locally |

## 🌍 Internationalization

The application supports English and Vietnamese with automatic language detection:

- **English (`en`)**: Default language
- **Vietnamese (`vi`)**: Fully translated interface

Users can manually switch languages using the language selector in the header. Language preference is persisted in localStorage.

### Translation Files Location
- `src/locales/en/` - English translations
- `src/locales/vi/` - Vietnamese translations

## 🎨 Theming

The application supports light and dark modes with automatic persistence:

- **Light Mode**: Clean, bright interface for daytime use
- **Dark Mode**: Eye-friendly dark interface for reduced eye strain

Theme preference is stored in localStorage and automatically applied on next visit.

## 📱 Responsive Design

The application is fully responsive and works seamlessly on:
- Desktop (1920px and above)
- Laptop/Tablet (1024px - 1919px)
- Mobile (480px - 1023px)
- Small devices (below 480px)

## 🔧 Customization Guide

### Adding New Book Categories

1. Create a new section component in `src/components/BookSections/`
2. Add category data in `src/data/categories.ts`
3. Import and render in the Home page

### Extending Translations

1. Add new keys to `src/locales/en/*.json`
2. Add corresponding translations to `src/locales/vi/*.json`
3. Use with `useTranslation()` hook

### Adding New Pages

1. Create page component in `src/pages/main/`
2. Add route in `src/routes/Routes.tsx` with lazy loading:
   ```tsx
   const NewPage = lazy(() => import('../pages/main/NewPage'));
   { path: '/new-page', component: NewPage }
   ```

## 📊 API Integration

The application uses the Google Books API for real-time book data:

- **Search Books by Subject**: `GET /volumes?q=subject:{subject}`
- **Get Book Details**: `GET /volumes/{bookId}`
- **Response Type**: Fully typed Google Books API responses

All API calls go through the centralized `axiosClient` for consistent error handling and configuration.

## 🐛 Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers

## 📈 Future Enhancements

- [ ] User authentication and profiles
- [ ] Book wishlist/favorites functionality
- [ ] User book reviews and ratings
- [ ] Shopping cart and checkout
- [ ] Advanced search filters
- [ ] Book recommendations engine
- [ ] Social sharing features
- [ ] Progressive Web App (PWA) capabilities

## 💼 Professional Highlights

### Code Quality
✅ Strict TypeScript configuration  
✅ ESLint integration for code standards  
✅ Component-based architecture  
✅ DRY principles throughout  

### Performance
✅ Code splitting and lazy loading  
✅ Vite for fast development and production builds  
✅ Optimized images (AVIF format)  
✅ Minimal bundle size  

### User Experience
✅ Smooth animations and transitions  
✅ Dark/Light theme support  
✅ Multi-language support  
✅ Fully responsive design  
✅ Loading states and error handling  

### Best Practices
✅ Modern React patterns (Hooks, Suspense)  
✅ Clean component organization  
✅ Centralized API management  
✅ Type-safe development  

## 📄 License

This project is created as a portfolio project. Feel free to use it as a reference or starting template.

## 👨‍💻 Author

Created as a comprehensive demonstration of modern full-stack web development practices and technologies.

---

**Note**: This is a portfolio project showcasing professional development practices, modern tooling, and clean architecture principles. It serves as an excellent example of production-ready code structure and follows industry best practices.
