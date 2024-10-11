# Simple Homeserver homepage, Single html file (no external packages/dependencies)
This is a very simple homepage for services hosted on your home server. It displays a list of services in a grid layout, with each service represented by a clickable button simple Single HTML file no external dependencies.

![homepage](https://github.com/user-attachments/assets/fabb7962-1192-4dc8-ba30-e780c581e978)

## Features

- **Dark Mode**: The page has a dark theme with light-colored text for better contrast.
- **Responsive Design**: The services are displayed in a grid layout that adjusts based on the screen size.
- **Interactive Buttons**: Service buttons have hover and click effects for an interactive experience.
- **JavaScript Driven**: Services are configured and rendered dynamically via JavaScript.

## Usage

### Prerequisites

Ensure you have a web server like NGINX, Apache, or any other server to serve this static HTML page.

### How to Use

1. **Modify the Services List**: 
    - Edit the `servicesConfig` array in the `<script>` section of the HTML file to include the services you want to display. Each service should have a `name` and `url`.

    ```javascript
    const servicesConfig = [
        { name: "File Sharing", url: "http://myserver/files" },
        { name: "Home Assistant", url: "http://myserver/homeassistant" },
        { name: "Media Server", url: "http://myserver/media" },
        { name: "Bitwarden", url: "http://myserver/bitwarden" },
    ];
    ```

2. **Deploy the HTML Page**: 
    - Place the HTML file on your web server (e.g., `/var/www/html/index.html` for NGINX).
    - Configure your server to serve this file.

3. **Access the Page**:
    - Open your browser and navigate to the server’s IP or domain to access the homepage.
    - Example: `http://myserver/`

### Customization

- **Styling**: You can update the background, font, or button styles by modifying the CSS in the `<style>` block.
- **New Services**: Add more services by updating the `servicesConfig` array with additional entries.

### Security

- You can protect this page using basic authentication (e.g., NGINX with `.htpasswd`) for added security.
