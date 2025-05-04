# Connekz Chat

![Connekz Logo](https://storage.connekz.com/static/logos/logo-120.webp)

Connekz Chat is a powerful, cross-platform chat solution designed for businesses to seamlessly integrate real-time communication into websites and mobile applications. This official npm package enables developers to embed text chat, voice messages, file sharing, audio/video calls, and AI-driven features into their projects. It supports web, iOS, and Android platforms, with comprehensive event handling and functions for external control, making it ideal for custom chat applications.

## Features

- **Text Chat**: Real-time messaging with support for group and private conversations.
- **Voice Messages**: Send and receive voice recordings.
- **File Sharing**: Securely share files of various formats.
- **Audio/Video Calls**: High-quality calls with cross-platform support.
- **AI-Driven Auto Reply**: Configure automated responses based on business data for customer support, booking forms, and more.
- **Mobile App Integration**: Full support for iOS and Android, including call/notification events and external control functions.
- **Cross-Platform**: Works seamlessly on web, iOS, and Android with a unified API.
- **Social Media Integration**: Link WhatsApp, Messenger, and Instagram for centralized communication.
- **Comprehensive APIs**: Manage users, messages, and settings programmatically.
- **Custom Branding**: Create multiple chat apps under one organization with unique branding and settings.
- **Connekz Handle**: Unique user handles for easy connection via QR code scanning.
- **Web Portal**: Manage organizations and chat apps through a dedicated web interface.

## Installation

Install the Connekz Chat package via npm:

```bash
npm install @connekz/chat
```

## Usage

### Web Integration

To integrate Connekz Chat into a website, import and initialize the package:

```javascript
import ConnekzChat from '@connekz/chat';

const chat = new ConnekzChat({
  apiKey: 'YOUR_API_KEY',
  organizationId: 'YOUR_ORG_ID',
  appId: 'YOUR_APP_ID',
  containerId: 'chat-container' // ID of the HTML element to mount the chat
});

// Initialize the chat
chat.init();
```

Add a container in your HTML:

```html
<div id="chat-container"></div>
```

### Mobile App Integration

For iOS and Android, use the package with Capacitor for native integration. The package provides events and functions to handle calls and notifications.

```javascript
import ConnekzChat from '@connekz/chat';

// Initialize for mobile
const chat = new ConnekzChat({
  apiKey: 'YOUR_API_KEY',
  organizationId: 'YOUR_ORG_ID',
  appId: 'YOUR_APP_ID',
  platform: 'mobile' // Specify mobile platform
});

// Handle incoming call event
chat.on('incomingCall', (callData) => {
  console.log('Incoming call:', callData);
  // Trigger native notification or UI
});

// Start a call
chat.startCall({
  userId: 'TARGET_USER_ID',
  type: 'video' // or 'audio'
});
```

### Event Handling

The package emits events for real-time updates, such as messages, calls, and notifications:

```javascript
// New message received
chat.on('newMessage', (message) => {
  console.log('New message:', message);
});

// Call ended
chat.on('callEnded', (callData) => {
  console.log('Call ended:', callData);
});
```

### API Control

Manage users and messages via the API:

```javascript
// Add a user
chat.addUser({
  userId: 'USER_ID',
  name: 'John Doe',
  handle: '@john'
});

// Send a message
chat.sendMessage({
  userId: 'USER_ID',
  recipientId: 'RECIPIENT_ID',
  content: 'Hello!'
});
```

## Configuration

Configure the chat with options during initialization:

```javascript
const chat = new ConnekzChat({
  apiKey: 'YOUR_API_KEY',
  organizationId: 'YOUR_ORG_ID',
  appId: 'YOUR_APP_ID',
  autoReply: {
    enabled: true,
    data: {
      faq: {
        'What are your hours?': 'We are open 9 AM to 5 PM.'
      }
    }
  },
  branding: {
    primaryColor: '#007bff',
    logoUrl: 'https://your-brand.com/logo.png'
  },
  integrations: {
    whatsapp: { enabled: true, phoneNumber: '+1234567890' },
    messenger: { enabled: true, pageId: 'YOUR_PAGE_ID' }
  }
});
```

## Web Portal

Manage your organization and chat apps via the [Connekz Web Portal](https://connekz.com/portal). Create organizations, configure apps, and customize settings like branding and auto-reply rules.

## Mobile App

Download the Connekz mobile app from the [App Store](https://apple.com/app-store) or [Google Play](https://play.google.com) to communicate with businesses or individuals using Connekz.

## API Documentation

For detailed API documentation, visit [Connekz API Docs](https://connekz.com/docs/api).

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add your feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

## License

MIT License. See [LICENSE](LICENSE) for details.

## Support

For issues or questions, contact us at [support@connekz.com](mailto:support@connekz.com) or open an issue on [GitHub](https://github.com/connekz/chat).
