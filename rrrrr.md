# MEXC API Key Creation Guide

Step-by-step screenshots from MEXC (via ICG Trading interface) showing how to create a Spot API key with trading permissions and IP restrictions.

## 1. API Management Section
Located under Profile → API Management

![API Management Menu](https://i.imgur.com/placeholder-for-sidebar.png)  
*(Sidebar: Profile → API Management)*

## 2. Create New API Key – Settings & Permissions

Spot permissions enabled:
- View Account Details
- View Order Details + Trade
- View Deposit/Withdrawal Details (no Withdraw)
- Read Transfer information

Notes: "Market Making Account"  
Linked IPs (example): `111.111.1.1,222.222.2.2`

Warning: Keys without IP link expire after 90 days (not recommended)

![API Creation Form](https://i.imgur.com/placeholder-for-api-form.png)  
*(Spot trading enabled, IP field filled)*

## 3. Security Verification

- Email code sent to ko***@gmail.com → "Get Code"
- 2FA Authenticator code
- Agree to risk reminders
- Submit

![Security Verification Popup](https://i.imgur.com/placeholder-for-verification.png)  
*(Email + Authenticator code entry)*

## 4. API Key Created Successfully

**Access Key**  
`mxOvgiVW o9NPD NalQg` (example – copy immediately)

**Secret Key**  
`63f0a5e119da44a4ac58a7731689686bc` (example – shown **only once**, save securely!)

Linked IPs confirmed below.

![API Key Success Popup](https://i.imgur.com/placeholder-for-success.png)  
*(Access Key & Secret Key displayed – save both!)*

### Important Security Notes
- Never share the **Secret Key** – it cannot be retrieved later.
- Strongly recommended: Link to IP address(es) → up to 20 allowed.
- Without IP restriction → key valid for only 90 days.
- You can create up to 30 API key sets per account.
- For market making or third-party tools, review MEXC API documentation.

**Save your keys securely now – this screen won't appear again.**