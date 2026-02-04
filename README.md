# Windows 95 Social Media Landing Page

A retro Windows 95-themed landing page for your social media links, designed for GitHub Pages.

## Features

- **Windows 95 Aesthetic**: Classic windows, taskbar, and icons.
- **Starry Night Background**: CSS-generated starry background to match your stream theme.
- **Twitch Embed**: Auto-plays your stream when you're live.
- **Social Links**: Quick links to Twitch, YouTube, Kick, Twitter, TikTok, and Instagram.
- **YouTube Feed**: Automatically displays your 3 most recent videos.
- **TikTok Shorts**: Embeds your top 3 recent TikToks.

## How to Customize

Open `index.html` in a text editor and look for the `<script>` section at the bottom.

### 1. YouTube Channel ID
To make the YouTube feed work, you need your **Channel ID** (starts with `UC`).
1. Go to [Comment Picker YouTube Channel ID](https://commentpicker.com/youtube-channel-id.php).
2. Enter your YouTube handle `@tellobyte`.
3. Copy the "Channel ID" it gives you.
4. Update this line in `index.html`:
   ```javascript
   youtubeChannelId: "UC..." // <-- Paste your ID here
   ```

### 2. TikTok Videos
TikTok does not allow fetching videos automatically without a complex API setup. You need to manually paste the links to the 3 videos you want to feature.
Update the `TIKTOK_URLS` array in `index.html`:
```javascript
const TIKTOK_URLS = [
  "https://www.tiktok.com/@tellobytetv/video/123456789...",
  "https://www.tiktok.com/@tellobytetv/video/987654321...",
  "https://www.tiktok.com/@tellobytetv/video/555555555..."
];
```

## How to Deploy to GitHub Pages

1. **Create a Repository**: Create a new public repository on GitHub (e.g., `social-hub`).
2. **Upload Files**: Upload `index.html` to the repository.
3. **Enable Pages**:
   - Go to **Settings** > **Pages**.
   - Under **Source**, select `main` (or `master`) branch.
   - Click **Save**.
4. **Done!** Your site will be live at `https://yourusername.github.io/social-hub/`.

## Notes
- **Twitch Embed**: The Twitch player requires the `parent` parameter to match your website's domain. The script automatically handles this for `localhost` and `github.io` domains. If you use a custom domain (e.g., `tellobyte.com`), it will also work automatically.
