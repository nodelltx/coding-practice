# Google Maps API Setup Instructions

Follow these steps to get your Google Maps API key and enable the interactive store locator.

## Step 1: Create a Google Cloud Account

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Sign in with your Google account
3. Accept the Terms of Service if prompted

## Step 2: Create a New Project

1. Click on the project dropdown at the top of the page
2. Click "New Project"
3. Give your project a name (e.g., "Outdoor Store Locator")
4. Click "Create"
5. Wait for the project to be created, then select it

## Step 3: Enable the Maps JavaScript API

1. In the left sidebar, click on "APIs & Services" > "Library"
2. Search for "Maps JavaScript API"
3. Click on "Maps JavaScript API"
4. Click the "Enable" button
5. Wait for the API to be enabled

## Step 4: Create an API Key

1. In the left sidebar, click on "APIs & Services" > "Credentials"
2. Click "+ CREATE CREDENTIALS" at the top
3. Select "API key"
4. Your API key will be created and displayed
5. **IMPORTANT**: Copy this key - you'll need it in the next step

## Step 5: Add the API Key to Your Website

1. Open the file `store-locator.html` in your code editor
2. Find this line near the bottom of the file:
   ```html
   <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY_HERE&libraries=places&callback=initMap" async defer></script>
   ```
3. Replace `YOUR_API_KEY_HERE` with your actual API key
4. Save the file

## Step 6: Test Your Store Locator

1. Open `store-locator.html` in your web browser
2. You should now see an interactive map with store markers
3. Try the "Find Nearest Store" button (will ask for location permission)
4. Try searching by address or ZIP code

## Pricing Information

- Google Maps offers **$200 in free credit every month**
- This covers approximately 28,000 map loads per month
- For a small business, this is usually more than enough
- You won't be charged unless you explicitly enable billing and exceed the free tier

## Optional: Restrict Your API Key (Recommended)

For security, you should restrict your API key:

1. Go back to "Credentials" in Google Cloud Console
2. Click on your API key
3. Under "Application restrictions":
   - Select "HTTP referrers (websites)"
   - Add your website domain (e.g., `yourwebsite.com/*`)
4. Under "API restrictions":
   - Select "Restrict key"
   - Select only "Maps JavaScript API"
5. Click "Save"

## Troubleshooting

**Problem**: Map not loading or shows "For development purposes only" watermark
- **Solution**: Make sure you've replaced `YOUR_API_KEY_HERE` with your actual API key

**Problem**: "This page can't load Google Maps correctly" error
- **Solution**: Check that the Maps JavaScript API is enabled in your Google Cloud project

**Problem**: Map loads but shows errors in console
- **Solution**: Make sure your API key has the correct restrictions and permissions

## Need Help?

- [Google Maps Platform Documentation](https://developers.google.com/maps/documentation)
- [Maps JavaScript API Guide](https://developers.google.com/maps/documentation/javascript/tutorial)

---

**Note**: Keep your API key secure! Don't share it publicly or commit it to public repositories without restrictions.
