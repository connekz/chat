# @connekz/chat

A lightweight and powerful chat widget for businesses to integrate seamless communication into their websites.  
Built with Vue 3 and Vuetify, this package allows Connekz clients to embed a fully-featured chat application with support for text chat, voice messages, file sharing, audio/video calls, and AI-driven features like auto-replies and booking form filling.

---

## About Connekz

Connekz is a cross-platform chat application designed for businesses, offering a unified communication solution across web, iOS, and Android. Key features include:

- **Text Chat**: Real-time messaging for business-client communication.
- **Voice Messages**: Send and receive voice notes.
- **File Sharing**: Securely share files with clients.
- **Audio/Video Calls**: High-quality calls for direct interaction.
- **AI-Driven Features**: Auto-replies based on business data, booking form filling, and more.
- **Third-Party Integrations**: Connect with WhatsApp, Messenger, and Instagram to centralize communication.
- **Customizable Apps**: Create branded chat apps with different settings via the Connekz Portal.

Learn more at the Connekz Website (placeholder—replace with the actual URL if available) or manage your chat apps through the Connekz Portal (placeholder—replace with the actual URL if available).

---

## Installation

Install the package via npm:

```bash
npm install @connekz/chat
```

---

## Setup and Usage Guide

### 1. Import and Initialize the Chat Widget

Add the chat widget to your website by importing and initializing it in your JavaScript or TypeScript code.

```javascript
import { initConnekzChat } from '@connekz/chat';

// Initialize the chat widget in a DOM element with the specified ID
const chat = initConnekzChat('connekz-chat');
```

### 2. Add the Container Element

Ensure you have a `<div>` element in your HTML where the chat widget will be mounted. The widget will respect the dimensions of this element.

```html
<!DOCTYPE html>
<html>
<head>
  <title>Connekz Chat Integration</title>
</head>
<body>
  <h1>My Website with Connekz Chat</h1>
  <!-- Container for the chat widget -->
  <div id="connekz-chat" style="width: 400px; height: 600px; border: 2px solid black;"></div>

  <!-- Import the chat widget -->
  <script type="module">
    import { initConnekzChat } from '@connekz/chat';
    const chat = initConnekzChat('connekz-chat');

    // Optional: Unmount the chat after a certain time
    setTimeout(() => {
      chat.unmount();
      console.log('Chat unmounted');
    }, 10000);
  </script>
</body>
</html>
```

### 3. Customize the Chat Widget

- **Dimensions**: The chat widget will automatically fit within the dimensions of the `#connekz-chat` element. Adjust the `width` and `height` in the element's style to suit your needs.
- **Styling**: The widget is encapsulated in a Shadow DOM, ensuring it doesn't interfere with your website's styles. However, you can style the container element (`#connekz-chat`) as needed.
- **Features**: Configure features like AI auto-replies and third-party integrations via the Connekz Portal.

---

## Documentation

For detailed documentation on advanced configuration, API usage, and integration with the Connekz ecosystem, visit the Connekz Documentation (placeholder—replace with the actual URL if available).

---

## Support

- **Issues**: Report bugs or request features on the GitHub Issues page.
- **Connekz Support**: Contact the Connekz team via the Connekz Website for business-specific support or inquiries about the Connekz Portal.

---

## License

This package is licensed under the MIT License. See the LICENSE file for details.
