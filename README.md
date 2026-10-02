# LiveChat Support Dashboard

A Node.js customer-support dashboard for managing LiveChat conversations, support teams, groups and AI-assisted response workflows.

This project explores how support operations can be brought into a single interface with role-based access, real-time messaging and configurable automation.

## Features

- LiveChat conversation management
- Real-time customer messaging
- Support groups and team management
- Owner, administrator and agent roles
- Group-specific configuration
- AI-assisted customer responses
- Promotion and content management
- Configurable automated bot behavior
- Webhook-based LiveChat integration
- Manual agent replies
- Message history and conversation state
- Monitoring hooks for bot and webhook events
- Authentication and access controls
- Local persistence for development

## Architecture

The application uses an Express backend that coordinates:

- LiveChat API communication
- webhook processing
- support group configuration
- authentication and permissions
- AI-assisted responses
- conversation persistence
- real-time messaging

The browser-based dashboard provides the operational interface for support teams.

## Technology

- Node.js
- Express.js
- JavaScript
- WebSockets
- LiveChat APIs
- REST APIs
- OpenAI API integration
- SQLite
- MongoDB / Mongoose
- JSON Web Tokens
- bcrypt

## Main Components

`server2.js`  
Primary Express application and API server.

`newtest4.html`  
Support dashboard interface.

`livechat-webhook-bot.js`  
Webhook-driven LiveChat automation service.

`livechat-group-helpers.js`  
Utilities for mapping conversations and support groups.

`monitoring-hooks.js`  
Event hooks for observing inbound messages, AI responses, delivery results and bot errors.

## Webhook Events

The monitoring layer supports events such as:

- webhook received
- chat opened
- inbound message
- AI response generated
- LiveChat message sent
- message delivery failure
- skipped message
- unauthorized webhook
- bot error

Monitoring handlers are isolated so failures in monitoring code do not interrupt normal message processing.

## Local Development

Install dependencies:

`npm install`

Start the primary server:

`npm run server`

The project also contains development, webhook diagnostics and bot-testing scripts in `package.json`.

## Configuration

Runtime credentials and configuration should be supplied through environment variables.

Examples include:

- LiveChat authentication
- webhook secrets
- AI provider configuration
- application secrets
- support group settings

Never commit production API keys, access tokens or webhook secrets to the repository.

## Project Background

This repository represents an earlier standalone support-dashboard implementation developed while exploring LiveChat integrations, support automation and multi-team messaging.

The larger customer-support platform work is documented separately in the LiveChat Pro showcase:

https://github.com/benjihub/livechat-pro-showcase

## Status

Portfolio and development reference.

The repository remains public to demonstrate the Node.js, API-integration, real-time messaging and support-automation work behind the project.
