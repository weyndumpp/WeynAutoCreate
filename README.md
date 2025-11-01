# Facebook Account Creator Tool

## Overview
This is a Python-based CLI tool that automates the creation of Facebook accounts using temporary email addresses. The tool was imported from GitHub and completely rewritten with Filipino and RPW (role-play world) names support, along with advanced features.

**Current State**: Configured and ready to run. The application is a command-line interface tool that runs interactively with full customization options.

## Project Structure
- `weynFBCreate.py` - Main Python script that creates Facebook accounts using advanced registration method
- `requirements.txt` - Python dependencies (requests, faker, beautifulsoup4, fake-useragent)
- `weynFBCreate.txt` - Output file for generated accounts (auto-saved with full file path displayed)
- Custom email generator with 30+ rotating domains built-in
- Beautiful purple and blue WEYN ASCII banner

## Dependencies
- Python 3.11
- requests - HTTP library for API calls
- faker - Library for generating fake user data
- beautifulsoup4 - HTML parsing library
- fake-useragent - Random user agent generation
- Built-in modules: os, sys, re, time, json, random, string, hashlib

## Features
- **Beautiful WEYN Banner**: Stunning purple and blue ASCII art banner with pro branding
- **Name Options**: Choose between Filipino names or RPW (role-play world) names
- **Gender Selection**: Choose male or female for consistent name generation
- **Birthday Range**: Automatically generates birthdates between 1990-2003
- **Password Options**: Auto-generated (Name + 4 digits) or custom password
- **Multi-Domain Email Rotation**: Uses 30+ different temporary email domains to avoid flagging
- **Smart Retry System**: Automatically retries failed accounts up to 2 times with new email domains
- **Anti-Rate Limiting**: Random delays (3-5 seconds) between account creations
- **Colored Console Output**: Green checkmarks and colored success/failure messages for better visibility
- **Auto-Save to File**: Successful accounts automatically saved to `weynFBCreate.txt` with full path displayed
- **Simplified Output**: Shows only name, email, password, and user ID
- **No Email Confirmation**: Accounts are created without requiring OTP/email verification
- **Dynamic Token Extraction**: Uses fresh session tokens for each registration attempt
- **Clean Account Storage**: Saves accounts in organized format with name | email | password | user ID

## How to Use
1. **Run the Application**: Click the "Run" button or the workflow will start automatically
2. **Select Name Type**: Choose between Filipino names (1) or RPW names (2)
3. **Select Gender**: Choose male (1) or female (2)
4. **Select Password Type**: Auto-generated (1) or custom password (2)
5. **Enter Quantity**: Specify how many accounts you want to create
6. **Wait for Results**: The tool will generate accounts and display them in the console with colored output
7. **Check Output**: All successful accounts are auto-saved to `weynFBCreate.txt` in format: `Name | Email | Password | User ID`
8. **Download to Your Device**: 
   - Look at the left sidebar in Replit
   - Find the `weynFBCreate.txt` file
   - Right-click → Download
   - Or follow the instructions displayed at the end of account creation

## Name Lists
### Filipino Names
- **Male**: Juan, Jose, Miguel, Gabriel, Rafael, Antonio, Carlos, Luis, Marco, Paolo, Angelo, Joshua, and more
- **Female**: Maria, Ana, Sofia, Isabella, Gabriela, Valentina, Camila, Angelica, Nicole, Michelle, and more
- **Last Names**: Reyes, Santos, Cruz, Bautista, Garcia, Flores, Gonzales, Martinez, Ramos, and more

### RPW (Role-Play World) Names
- **Male**: Zephyr, Shadow, Phantom, Blaze, Storm, Frost, Raven, Ace, Knight, Wolf, Dragon, Phoenix, and more
- **Female**: Luna, Aurora, Mystic, Crystal, Sapphire, Scarlet, Violet, Rose, Athena, Venus, Nova, Stella, and more
- **Last Names**: Shadow, Dark, Light, Star, Moon, Sun, Sky, Night, Dawn, Storm, Frost, Fire

## Technical Details
- **Email System**: Custom generator with 30+ prioritized rotating domains to avoid email flagging
  - High success domains: mailto.plus, fexpost.com, tmpnator.live, wuuvo.com, rteet.com, and more
  - Random username generation (10-15 characters) for each attempt
- **Anti-Detection Measures**:
  - Smart retry system: Up to 2 retries per account with fresh email domains
  - **Fast creation**: Random delays of 1-2 seconds between successful accounts
  - 2-second delay before each retry attempt
  - Random user agents for each session
- **API Integration**:
  - Uses Facebook's mobile registration endpoint (www.facebook.com/reg/submit/)
  - Dynamically extracts session tokens (fb_dtsg, jazoest, lsd, m_ts) from registration form
- **Data Generation**:
  - Generates random user data based on selected name type
  - Birthday range: January 1, 1990 to December 31, 2003
  - Gender properly mapped to Facebook API requirements (male="2", female="1")
- **Output Features**:
  - Terminal color codes for better UX (purple/blue banner, green for success, red for failure, yellow for retries)
  - Auto-saves successful accounts to weynFBCreate.txt
  - Displays full file path for easy access
- No email confirmation or OTP verification required

## Important Notes
- This tool creates accounts without email verification
- Account creation success depends on Facebook's API availability and rate limits
- The tool does NOT require proxies (unlike the old version)
- **Created accounts are automatically saved to weynFBCreate.txt** with all login details
- Smart retry system helps reduce failures from email flagging
- **Fast creation speed**: Only 1-2 seconds delay between accounts
- **Download instructions**: Clear steps shown at the end to download file to your device
- Accounts may require additional verification from Facebook after creation
- The file is saved in the Replit workspace - use the download instructions to save to your device

## Recent Changes
- **2025-10-31**: Speed Optimization & Download Instructions
  - **Faster Account Creation**: Reduced delays to 1-2 seconds between accounts (was 3-5 seconds)
  - **Faster Retries**: Reduced retry delays to 2 seconds (was 3 seconds)
  - **Download Instructions**: Added clear step-by-step guide to download file to your device
  - **Better User Experience**: Purple download icon and colored instructions for easy visibility

- **2025-10-31**: Major Anti-Detection & UI Overhaul
  - **Beautiful Purple & Blue WEYN Banner**: Added stunning ASCII art banner with purple and blue color combination
  - **Smart Retry System**: Automatically retries failed accounts up to 2 times with new email domains
  - **Auto-Save to weynFBCreate.txt**: Changed output file from username.txt to weynFBCreate.txt
  - **Improved Email Domains**: Prioritized high-success email domains at the top of rotation list
  - **Better Error Handling**: Retry indicators with yellow warning messages
  - **File Path Display**: Shows full absolute path to weynFBCreate.txt file at the end
  - **Enhanced Colors**: Purple for summary header, cyan for info, yellow for warnings

- **2025-10-31**: Email Flagging Fix & UI Improvements
  - Replaced single-domain email generator with 30+ rotating domains to avoid flagging
  - Added terminal color support for better visibility (green for success, red for failure)
  - Success messages now display in green with ✓ checkmark
  - Email addresses shown in blue during creation, green when successful
  - Removed fake_email dependency in favor of custom multi-domain email generator
  - Updated requirements.txt to remove duplicate dependencies
  - Improved anti-detection measures with domain rotation

- **2025-10-31**: GitHub Import to Replit Environment
  - Successfully imported project from GitHub ZIP archive
  - Installed Python 3.11 module in Replit environment
  - Installed all Python dependencies: requests, faker, beautifulsoup4, fake-useragent
  - Configured "FbCreator CLI" workflow for console-based interactive execution
  - Verified application starts successfully and displays interactive menu
  - Project ready to use - user can interact with CLI via console

- **2025-10-31**: Initial setup in Replit environment
  - Installed Python 3.11
  - Created requirements.txt with proper dependencies
  - Set up workflow for CLI execution
  - Added .gitignore for Python project
  - Created project documentation

- **2025-10-31**: Major customization update
  - Added Filipino names support with authentic Filipino first and last names
  - Added RPW (role-play world) names for creative accounts
  - Implemented interactive menu for name type selection
  - Implemented interactive menu for gender selection
  - Changed birthday generation to 1999-2003 range
  - Simplified output to show only name, email, and password
  - Fixed gender mapping to properly work with Facebook API ('male'/'female')
  - Improved proxy filtering to ignore comment lines
  - Added timeouts to prevent hanging requests
  - Updated username.txt format for cleaner output

- **2025-10-31**: Complete rewrite with advanced features
  - Extracted auto-create method from advanced script
  - Installed beautifulsoup4, fake-useragent, fake_email dependencies
  - Implemented dynamic token extraction for session security
  - Removed proxy requirement (no longer needed)
  - Added custom password option
  - Changed birthday range to 1990-2003 (from 1999-2003)
  - Removed email confirmation/OTP functionality completely
  - Fixed hard-coded tokens to use dynamic form extraction
  - Improved error handling and user feedback
  - Updated output format to include User ID
