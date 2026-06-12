**Source article:** [How to Set Up Live Chat on WordPress Without Breaking Your Site](https://helpmate.chat/live-chat-wordpress-setup-guide/)

---

# Live Chat on WordPress: Zero-Code Installation Guide

Live chat delivers 73% customer satisfaction and ~20% conversion lift according to Nextiva 2025 research. This guide shows how to add Helpmate Live Chat without touching theme files or writing code.

## Installation
- Install via WordPress Plugins > Add New, search \"Helpmate\" or upload the zip
- Activate, run the onboarding wizard—API key generates automatically
- Helpmate injects through wp_footer hook; no header.php edits required
- Widget appears bottom-right by default; verify in incognito window

## Widget Placement & Performance

- Appearance tab controls positioning: all pages, specific post types, or URL exclusions
- Bottom-right avoids navigation conflicts; auto-sizes mobile (<768px)
- Enable lazy loading in Behavior tab to delay initialization until scroll/interaction
- Use script deferral instead of async to maintain execution order
- With optimizations, chat impact stays under 100ms on Core Web Vitals

## Team Access

- Go to Helpmate > Control Center > Teams & Roles
- Three levels:
  - Administrator: Full settings, analytics, team management
  - Agent: Live queue access, assigned conversations
  - Viewer: Read-only analytics and history
- Assign by job duties, not titles; marketing can have Viewer access without queue clutter

## AI-to-Human Handover

- Configure triggers in Behavior > Chatbot Settings:
- Keywords: \"refund\", \"complaint\", \"speak to human\"
- Three consecutive AI responses without resolution
- Explicit human request button
- Outside business hours when agents available
- Knowledge Base trains AI on products, posts, pages, URLs, Q&A pairs, CSVs, PDFs
- Handover delivers full context including AI interaction history

## Performance Settings

- Enable script deferral in Behavior tab
- Adjust connection intervals: 3s during active chats, 30s idle
- Exclude Helpmate dynamic endpoints from page caching (WP Rocket, W3 Total Cache, LiteSpeed)
- Test via sandbox in admin sidebar before going live

## Troubleshooting

- Widget missing? Check plugin active, API key valid, theme implements wp_footer()
- JavaScript errors? Exclude Helpmate scripts from aggressive minification plugins
- Message delivery issues? Verify wp-cron.php runs periodically
- Conversation data stays in WordPress DB unless explicitly deleted during uninstall

## Requirements

- PHP 7.4+, WordPress 5.8+, HTTPS active
- Free tier includes live chat, AI chatbot, CRM features
  - Unlimited agents on free plan with role controls

Key success pattern: build Knowledge Base first, define team roles before opening queue, test thoroughly in sandbox.
