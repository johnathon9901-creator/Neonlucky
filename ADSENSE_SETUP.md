# Google AdSense Integration Guide

This document provides step-by-step instructions for activating Google AdSense on the Neonlucky website.

## ⚠️ Important Legal Notice

**Social Casino Compliance**: Neonlucky is a free-to-play social casino with no real money involved. Before monetizing with AdSense, ensure you understand Google's policies:

- Social casino games are allowed on AdSense, but must include clear disclaimers
- Games must not target minors and must include 21+ age requirements
- Neonlucky already includes these disclaimers on all pages
- Do NOT advertise real-money gambling services on AdSense (use alternative ad networks for that)

## Step 1: Sign Up for Google AdSense

1. Visit [Google AdSense](https://www.google.com/adsense/start/)
2. Click **Sign Up Now**
3. Sign in with your Google account (create one if needed)
4. Enter your website URL: `https://yourdomain.com/` (replace with your actual domain)
5. Fill in your contact information
6. Accept the terms and submit

## Step 2: Verify Your Website

Google will send you a verification email. You need to add a verification meta tag to your site:

1. In your AdSense account, go to **Sites** > **Add site**
2. Copy the verification meta tag provided
3. Replace the placeholder in the `<head>` section of your HTML files with the actual verification tag
4. Deploy the changes to your website
5. Return to AdSense and click **Verify**

## Step 3: Get Your Publisher ID

Once approved, you'll receive your **Publisher ID** (format: `ca-pub-XXXXXXXXXXXXXXXX`).

## Step 4: Update Your Code

Replace all instances of `ca-pub-XXXXXXXXXXXXXXXX` with your actual Publisher ID in the following files:

### index.html
- Line 13: Update the AdSense script tag
- Line 131: Update the ad unit data-ad-client attribute

### slots.html
- Line 11: Update the AdSense script tag
- Line 178: Update the ad unit data-ad-client attribute

### ads.txt
- Line 3: Update with your Publisher ID

## Step 5: Create Ad Units

In your AdSense account:

1. Go to **Ads** > **Ad units**
2. Click **New ad unit**
3. Choose **Display ads**
4. Name your ad unit (e.g., "Homepage Banner")
5. Choose **Responsive** for ad size
6. Copy the generated **Ad Slot ID** (format: `XXXXXXXXXX`)

Create at least 2 ad units:
- **Homepage Banner**: For the home page
- **Game Banner**: For the slots game page

## Step 6: Update Ad Slot IDs

Replace `XXXXXXXXXX` with your actual ad slot IDs:

### index.html
- Line 132: Update data-ad-slot attribute with your Homepage Banner slot ID

### slots.html
- Line 179: Update data-ad-slot attribute with your Game Banner slot ID

## Step 7: Deploy Changes

1. Commit your changes to Git:
   ```bash
   git add .
   git commit -m "Activate Google AdSense with Publisher ID and Ad Slots"
   git push origin main
   ```

2. Deploy to your hosting (GitHub Pages, Netlify, Vercel, etc.)

## Step 8: Monitor Performance

Once deployed:

1. Wait 24-48 hours for ads to start appearing
2. Monitor your AdSense dashboard for impressions and earnings
3. Ensure ads are displaying correctly on all pages

## Troubleshooting

**Ads not showing?**
- Ensure your Publisher ID is correct
- Verify your ad slot IDs are valid
- Check that your site is live and accessible
- Wait 24-48 hours for initial approval
- Check the browser console for any JavaScript errors

**Low earnings?**
- Ensure proper ad placement (above the fold is better)
- Use responsive ad sizes for better fill rates
- Maintain good user experience (don't overload with ads)
- Ensure your content is high-quality and original

## Ad Placement Strategy

Current placements:
- **Homepage**: One responsive banner ad above the game cards
- **Slots Page**: One responsive banner ad below the balance display

Recommendations:
- Don't add more than 3 ad units per page (Google's limit)
- Place ads where they're visible without excessive scrolling
- Avoid placing ads directly above interactive elements
- Use responsive ads for better mobile experience

## Important Reminders

✅ **DO:**
- Maintain clear 21+ age disclaimers
- Keep the site free-to-play
- Provide quality user experience
- Monitor your account for policy violations

❌ **DON'T:**
- Click on your own ads (violates AdSense terms)
- Encourage users to click ads
- Place misleading content near ads
- Violate Google's content policies

## Support

For AdSense support, visit: [Google AdSense Help Center](https://support.google.com/adsense)

For Neonlucky issues, check the main README.md or create a GitHub issue.
