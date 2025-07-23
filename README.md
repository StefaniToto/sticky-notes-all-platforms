# Sticky Notes - Cross-Platform Task Manager

A powerful sticky notes application designed to keep you organized across all your devices. Create notes with bullet points, set notifications, and stay synchronized between Android, iOS, web, and desktop platforms.

## Features

- 📝 **Rich Text Notes**: Create sticky notes with bullet points and formatting
- 🔔 **Smart Notifications**: Set reminders to never miss important tasks
- 🔄 **Cross-Platform Sync**: Stay synchronized across all your devices
- 📱 **Mobile Apps**: Native Android and iOS apps built with Ionic Capacitor
- 💻 **Desktop Apps**: Electron-based apps for Windows, macOS, and Linux
- 🌐 **Web App**: Access your notes from any browser
- ☁️ **Cloud Storage**: Secure data storage with Firebase

## Platforms

- **Mobile**: Android & iOS (Ionic Capacitor)
- **Desktop**: Windows, macOS, Linux (Electron)
- **Web**: Progressive Web App
- **Backend**: Firebase for real-time synchronization

## Getting Started

### Quick Start (Current Status)

The project is ready to run locally with basic functionality:

1. **Install dependencies:**
```bash
npm install
cd shared && npm install && npm run build
cd ../web && npm install
cd ../desktop && npm install
cd ../mobile && npm install
```

2. **Run applications:**
```bash
# Web application
cd web && npm start

# Desktop application  
cd desktop && npm start

# Mobile application
cd mobile && ionic serve
```

### Current Status

✅ **Phase 1 Complete - Basic Functionality**
- Monorepo structure with shared library
- ✅ Angular web application with sticky notes
- ✅ Ionic mobile application structure
- ✅ Electron desktop application with notes
- ✅ Local storage persistence
- ✅ Drag and drop functionality
- ✅ Bullet points with checkboxes
- ✅ Note creation, editing, and deletion
- ✅ Color-coded notes
- 🔄 Firebase backend (configured, not connected yet)
- 🔄 Cross-platform synchronization (next phase)

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn
- For mobile development: Ionic CLI, Android Studio, Xcode

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/sticky-notes-all-platforms.git
cd sticky-notes-all-platforms
```

2. Install all dependencies:
```bash
npm run install:all
```

3. Build the shared library:
```bash
cd shared && npm run build
```

### Firebase Setup

Before running the applications, you'll need to set up Firebase:

1. Create a new Firebase project at [Firebase Console](https://console.firebase.google.com)
2. Enable Authentication, Firestore Database, and Cloud Messaging
3. Create a web app in your Firebase project
4. Copy the Firebase configuration and add it to each platform:
   - Web: `web/src/environments/environment.ts`
   - Mobile: `mobile/src/environments/environment.ts`
   - Desktop: Create `desktop/src/firebase-config.js`

5. Deploy Firebase rules and indexes:
```bash
cd firebase
firebase login
firebase use --add  # Select your project
firebase deploy --only firestore
```

### Running the Applications

After setup is complete, you can run each platform:

**Desktop (Electron):**
```bash
npm run dev:desktop
```

**Mobile (Ionic):**
```bash
npm run dev:mobile
```

**Web (Angular):**
```bash
npm run dev:web
```

## Project Structure

```
sticky-notes-all-platforms/
├── desktop/              # Electron desktop application
├── mobile/               # Ionic Capacitor mobile app (Angular + Ionic)
├── web/                  # Angular web application (PWA)
├── shared/               # Shared TypeScript library (models, services, utils)
├── firebase/             # Firebase configuration, rules, and functions
└── docs/                 # Documentation and development guides
```

## Development

This is a monorepo where each platform shares common business logic through the `shared` library. Any changes to the shared library require rebuilding it before the changes are reflected in the applications.

### Desktop Development
- Built with **Electron**
- Cross-platform compatibility for Windows, macOS, and Linux
- Native system integration for notifications
- Uses shared TypeScript models and services

### Mobile Development
- Built with **Angular + Ionic + Capacitor**
- Native mobile features integration
- Push notifications support
- Shared codebase with web application

### Web Development
- Built with **Angular**
- Progressive Web App (PWA) capabilities
- Responsive design for all screen sizes
- Offline capability with service workers
- Firebase integration for real-time sync

### Shared Library
- **TypeScript** models and interfaces
- **Firebase** service configurations  
- Common utilities and constants
- Platform-agnostic business logic

### Development Workflow

1. Make changes to shared library: `cd shared && npm run build`
2. Develop platform-specific features in respective directories
3. Test across all platforms before committing

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

If you encounter any issues or have questions, please file an issue on the GitHub repository.

## Roadmap
