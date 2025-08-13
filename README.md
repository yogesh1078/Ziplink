# Ziplink

Ziplink is a URL shortener web application that converts long, unwieldy links into short, manageable URLs that are easy to share and remember.

## Features

- URL Shortening: Convert long URLs into concise, shareable links
- Custom Aliases: Create personalized short links with custom aliases
- Analytics: Track clicks and visitor information for your shortened URLs
- Link Management: Organize and manage all your shortened links in one place
- Secure: HTTPS encryption for all shortened links

## Tech Stack

- Frontend: JavaScript, React, HTML5, CSS3
- Backend: Node.js, Express
- Database: MongoDB
- Deployment: Docker, Heroku

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- MongoDB

### Installation

1. Clone the repository
```bash
git clone https://github.com/yogesh1078/Ziplink.git
cd Ziplink
```

2. Install dependencies
```bash
npm install
```

3. Set up environment variables
```bash
cp .env.example .env
```
Edit the `.env` file with your configuration details.

4. Start the development server
```bash
npm run dev
```

## Usage

1. Navigate to the application in your browser
2. Paste a long URL into the input field
3. Click "Shorten" to generate a shortened URL
4. Copy and share your new short link!



### Redirect to original URL
```
GET /:shortCode
```
Yogesh - [@yogesh1078](https://github.com/yogesh1078)

Project Link: [https://github.com/yogesh1078/Ziplink](https://github.com/yogesh1078/Ziplink)
