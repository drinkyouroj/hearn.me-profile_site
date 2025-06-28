# Professional Homepage for hearn.me

This repository contains the source code for the personal homepage of Justin Hearn, hosted at hearn.me.

## Features

- A clean, modern, and responsive design.
- A professional photo.
- Links to Resume, LinkedIn, GitHub, Twitter, YouTube, and a personal blog.
- Styled with an electric/vibrant color scheme.
- Icons for each link from Font Awesome.

## Setup

To run this site locally, simply open the `index.html` file in your web browser. No special setup is required.

## Deployment with Nginx

To deploy this site with Nginx and HTTPS, follow these steps:

1.  **Move the Nginx configuration file**:

    ```bash
    sudo mv hearn.me.conf /etc/nginx/sites-available/hearn.me
    ```

2.  **Create a symbolic link** to enable the site:

    ```bash
    sudo ln -s /etc/nginx/sites-available/hearn.me /etc/nginx/sites-enabled/
    ```

3.  **Obtain an SSL certificate** using Let's Encrypt and Certbot:

    ```bash
    sudo apt update
    sudo apt install certbot python3-certbot-nginx
    sudo certbot --nginx -d hearn.me -d www.hearn.me
    ```

4.  **Test and restart Nginx**:

    ```bash
    sudo nginx -t
    sudo systemctl restart nginx
    ```

## Design Choices

- **Colors**: The color scheme is designed to be vibrant and electric, using a dark background with bright, neon-like colors for text and highlights.
- **Fonts**: A clean, sans-serif font is used for readability.
- **Layout**: A simple, centered layout is used to focus on the essential information.
- **Icons**: Font Awesome is used to provide icons for the links, making them more visually appealing and recognizable.