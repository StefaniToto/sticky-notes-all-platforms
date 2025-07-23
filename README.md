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

2. Install dependencies for each platform:

**Desktop (Electron):**
```bash
cd desktop
npm install
npm start
```

**Mobile (Ionic):**
```bash
cd mobile
npm install
ionic serve
```

**Web:**
```bash
cd web
npm install
npm run dev
```

## Project Structure

```
sticky-notes-all-platforms/
├── desktop/          # Electron desktop application
├── mobile/           # Ionic Capacitor mobile app
├── web/              # Web application
├── shared/           # Shared utilities and types
├── firebase/         # Firebase configuration and functions
└── docs/             # Documentation
```

## Development

Each platform can be developed independently while sharing common business logic and data models.

### Desktop Development
- Built with Electron
- Cross-platform compatibility for Windows, macOS, and Linux
- Native system integration for notifications

### Mobile Development
- Built with Ionic Capacitor
- Native mobile features integration
- Push notifications support

### Web Development
- Progressive Web App (PWA)
- Responsive design for all screen sizes
- Offline capability with service workers

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

- [ ] Basic note creation and editing
- [ ] Bullet point formatting
- [ ] Notification system
- [ ] Firebase integration
- [ ] Cross-platform synchronization
- [ ] Mobile app development
- [ ] Desktop app enhancements
- [ ] Offline mode
- [ ] Collaboration features