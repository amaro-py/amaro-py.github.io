# Linktree Clone with Spotify Integration

A beautiful, modern Linktree clone with real-time Spotify integration, built with glassmorphism design and deployed via GitHub Pages.

## Features

- 🎵 **Real-time Spotify Integration** - Shows your currently playing track
- 🌟 **Glassmorphism Design** - Modern blue theme with backdrop blur effects
- 📱 **Fully Responsive** - Works perfectly on all devices
- 🔐 **Secure Authentication** - Uses PKCE flow for client-side security
- 🚀 **GitHub Pages Deployment** - Automatic deployment via GitHub Actions
- 🎨 **Animated Background** - Beautiful liquid blob animations
- 📊 **Discord Profile** - Shows Discord badges and status
- 📂 **Instagram Dropdown** - Multiple Instagram account options
- 🎧 **Audio Player** - Functional music player with controls

## Setup Instructions

### 1. Fork this Repository
- Click "Fork" in the top right corner
- Clone your fork to your local machine

### 2. Create a Spotify App
1. Go to [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)
2. Click "Create an app"
3. Fill in:
   - App name: `Your Linktree Clone`
   - App description: `Personal Linktree with Spotify integration`
   - Redirect URI: `https://yourusername.github.io/your-repo-name`
4. Accept the terms of service
5. Copy your **Client ID** (you'll need this for step 3)

### 3. Set up GitHub Repository Secret
1. Go to your GitHub repository
2. Navigate to **Settings > Secrets and variables > Actions**
3. Click "New repository secret"
4. Name: `SPOTIFY_CLIENT_ID`
5. Value: Your Spotify Client ID from step 2
6. Click "Add secret"

### 4. Enable GitHub Pages
1. Go to **Settings > Pages**
2. Under "Source", select **GitHub Actions**
3. The site will automatically deploy when you push to main

### 5. Customize Your Content
Edit `linktree.html` to customize:
- Profile image (`icon.png`)
- Banner image (`banner.png`)
- Discord username and badges
- Instagram dropdown options
- Link buttons and their URLs
- Audio player track

## File Structure

```
├── linktree.html          # Main HTML file
├── linktree.css           # Styling and animations
├── icon.png               # Profile image
├── banner.png             # Banner background
├── untitled.flac          # Audio file for player
├── .github/workflows/
│   └── deploy.yml         # GitHub Actions deployment
└── README.md              # This file
```

## How It Works

### Spotify Integration
- Uses **PKCE (Proof Key for Code Exchange)** for secure authentication
- No client secret needed (more secure for client-side apps)
- Automatically refreshes tokens when expired
- Updates every 30 seconds to show current track
- Handles "not playing" states gracefully

### GitHub Actions Deployment
- Automatically triggered on push to main branch
- Injects Spotify Client ID from repository secrets
- Builds and deploys to GitHub Pages
- No manual deployment needed

### Security Features
- Client secret never exposed in client-side code
- PKCE flow prevents authorization code interception
- Tokens stored securely in localStorage
- Automatic cleanup of temporary auth data

## Troubleshooting

### Spotify not connecting?
- Check that your Client ID is correct in repository secrets
- Verify your redirect URI matches your GitHub Pages URL
- Make sure your Spotify app is not in development mode restrictions

### Site not deploying?
- Check the Actions tab for build errors
- Ensure repository secrets are set correctly
- Verify GitHub Pages is enabled with "GitHub Actions" source

### Audio player not working?
- Check that `untitled.flac` file exists and is accessible
- Verify file format is supported by browsers
- Check browser console for any errors

## Customization

### Colors
Edit the CSS variables in `linktree.css` to change the color scheme:
```css
/* Main colors */
background: rgb(30, 64, 175);  /* Base blue */
border: 1px solid rgba(147, 197, 253, 0.5);  /* Border blue */
```

### Animations
Modify the blob animations in the CSS:
```css
@keyframes blob1 { /* Custom animation */ }
@keyframes blob2 { /* Custom animation */ }
```

### Content
Update the HTML content in `linktree.html`:
- Change Discord username and badges
- Modify Instagram dropdown options
- Update link URLs and text
- Replace images with your own

## License

This project is open source and available under the [MIT License](LICENSE).

## Contributing

Feel free to submit issues and pull requests to improve the project!

## Support

If you encounter any issues, please create an issue in this repository with:
- Description of the problem
- Steps to reproduce
- Browser and device information
- Any error messages from browser console 