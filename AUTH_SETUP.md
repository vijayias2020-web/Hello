# GitHub Authentication Setup

## Option 1: Personal Access Token (Recommended)

1. **Generate a Token on GitHub**:
   - Go to https://github.com/settings/tokens/new
   - Log in with your GitHub account
   - Enter a name: "Git Push Token"
   - Select scope: **repo** (full control of private repositories)
   - Click "Generate token"
   - **Copy the token** (you won't see it again!)

2. **Update Git Configuration**:
   Run this in PowerShell (replace TOKEN with your copied token):
   ```powershell
   git config --global credential.helper store
   git config --global user.email "your-email@example.com"
   git config --global user.name "vijayias2020-web"
   ```

3. **Try Pushing Again**:
   ```powershell
   cd "c:\Users\Vijay Yadav\OneDrive\Desktop\Hello"
   git push -u origin main
   ```
   When prompted for username/password:
   - Username: `vijayias2020-web`
   - Password: Paste your token (not your GitHub password!)

## Option 2: SSH Keys (Advanced)

If you prefer SSH setup, follow GitHub's guide:
https://docs.github.com/en/authentication/connecting-to-github-with-ssh

## Troubleshooting

If still getting error 403:
- Make sure you're using the correct GitHub username
- Verify the repository is created at: https://github.com/vijayias2020-web/Hello
- Check your token has `repo` scope selected
- Token must not be expired
