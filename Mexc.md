# How to Create an API Key on MEXC

## Step 1: Log in to Your MEXC Account
Go to the official MEXC website and log in using your account credentials.

## Step 2: Open API Management
1. Click on your **profile icon** (top-right corner).
2. Select **API Management** from the dropdown menu.

![API Management Menu](https://raw.githubusercontent.com/ICG-Khalid/Mexc/refs/heads/main/Screenshot%201.png)

## Step 3: Create a New API Key
1. Click on **Create API**.
2. Enter an **API Name / Label** (e.g., “MM Bot”, “Liquidity Bot”, or project name).
3. Add an **IP whitelist** and include the IPs provided by the ICG Trading team (**separate each IP using a comma without spaces**).

![Create API Settings] https://raw.githubusercontent.com/ICG-Khalid/Mexc/refs/heads/main/Screenshot%202.png

## Step 4: Set API Permissions
Choose the following permissions based on your use case:

![API Permissions](PASTE_YOUR_RAW_GITHUB_LINK_FOR_SCREENSHOT_3_HERE)

### Spot Access
- View Account Details
- View Order Details
- Trade
- View Deposit/Withdrawal Details
- Read transfer information

> **Important:** Do **NOT** enable withdrawals for security reasons.

## Step 5: Security Verification
Complete the required security checks:
- Email verification code
- Google Authenticator (2FA)

## Step 6: Save API Credentials
After creation, MEXC will display:
- API Key
- Secret Key

![API Key Created](PASTE_YOUR_RAW_GITHUB_LINK_FOR_SCREENSHOT_4_HERE)

> **Warning:** The Secret Key is shown only once. Store it securely.

## Security Best Practices
- Never share API keys publicly
- Use IP whitelist whenever possible
- Disable or delete unused API keys
- Review permissions regularly
