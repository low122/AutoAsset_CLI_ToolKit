# AutoAsset CLI ToolKit

A comprehensive CLI toolkit for managing and tracking digital assets, featuring an email subscription tracker that uses IMAP and OpenAI's GPT-4 for intelligent analysis.

## Email Subscription Tracker

### Features

- Connects to Gmail using IMAP securely
- Fetches and analyzes recent emails
- Identifies subscription-related information automatically
- Displays subscription details in a formatted table
- Handles duplicate emails and prioritizes important senders
- Provides detailed error messages and status updates

### Prerequisites

1. Python 3.9 or higher
2. Gmail account with IMAP enabled
3. Gmail App Password (for authentication)
4. OpenAI API key

### Setup

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Configure environment variables in `.env`:
   ```env
   # Email Configuration
   IMAP_SERVER=imap.gmail.com
   EMAIL_USER=your.email@gmail.com
   EMAIL_PASSWORD=your-app-specific-password  # Gmail App Password

   # OpenAI Configuration
   OPENAI_API_KEY=your-openai-api-key
   ```

#### Getting Gmail App Password

1. Go to your Google Account settings
2. Enable 2-Step Verification if not already enabled
3. Go to Security → App Passwords
4. Generate a new App Password for 'Mail'
5. Use this 16-character password in your `.env` file

#### Getting OpenAI API Key

1. Go to [OpenAI's website](https://platform.openai.com)
2. Sign up or log in
3. Go to API section
4. Generate a new API key
5. Copy the key to your `.env` file

### Usage

Run the subscription tracker:
```bash
python subtrack.py
```

The script will:
1. Connect to your Gmail account
2. Fetch recent emails
3. Analyze them for subscription information
4. Display results in a formatted table

### Error Messages

- ✗ Missing environment variables: Check your `.env` file
- ✗ IMAP error: Check your email/password and internet connection
- ✗ API error: Verify your OpenAI API key and quota

## Contributing

Feel free to submit issues and enhancement requests!

## License

MIT License