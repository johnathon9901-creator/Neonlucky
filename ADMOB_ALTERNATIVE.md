# Google AdMob Integration (Alternative to AdSense)

This document provides information about using **Google AdMob** as an alternative monetization method for Neonlucky.

## When to Use AdMob vs AdSense

| Feature | AdSense | AdMob |
|---------|---------|-------|
| **Best For** | Websites & Blogs | Mobile Apps & Web Apps |
| **Ad Types** | Display, Link, Search | Banner, Interstitial, Rewarded |
| **Setup Complexity** | Medium | Medium-High |
| **Revenue Potential** | Good | Excellent (for mobile) |
| **Minimum Traffic** | 100 unique visitors/day | No minimum |

## Why AdMob for Neonlucky?

AdMob is particularly well-suited for Neonlucky because:

1. **Mobile-First**: Neonlucky is fully responsive and mobile-friendly
2. **Rewarded Ads**: Perfect for social casinos (e.g., "Watch an ad to get bonus coins")
3. **Better Fill Rates**: Generally higher CPM rates for gaming content
4. **Interstitial Ads**: Can display between game sessions
5. **User Experience**: Rewarded ads feel less intrusive to players

## AdMob Implementation for Web

### Prerequisites

- Google account
- Neonlucky website live on a domain (not localhost)
- Basic JavaScript knowledge

### Step 1: Create AdMob Account

1. Visit [Google AdMob](https://admob.google.com/)
2. Click **Sign in with Google**
3. Complete the account setup
4. Accept the terms and policies

### Step 2: Add Your App

1. In AdMob, click **Apps** > **Add app**
2. Select **Web** as the platform
3. Enter your app name: "Neonlucky"
4. Accept the policies and create

### Step 3: Create Ad Units

Create the following ad units:

#### Banner Ad Unit
- **Format**: Banner (320x50, 300x250, 728x90)
- **Placement**: Homepage and slots page
- **Copy the Ad Unit ID** (format: `ca-app-pub-xxxxxxxxxxxxxxxx~yyyyyyyyyy`)

#### Interstitial Ad Unit
- **Format**: Interstitial
- **Placement**: Between game sessions
- **Copy the Ad Unit ID**

#### Rewarded Ad Unit
- **Format**: Rewarded
- **Placement**: "Watch ad for bonus coins" button
- **Copy the Ad Unit ID**

### Step 4: Implement in Code

#### Basic Banner Ad

```html
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-app-pub-xxxxxxxxxxxxxxxx"></script>

<ins class="adsbygoogle"
     style="display:block"
     data-ad-format="banner"
     data-ad-client="ca-app-pub-xxxxxxxxxxxxxxxx"
     data-ad-slot="yyyyyyyyyy"></ins>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script>
```

#### Rewarded Ad (Bonus Coins)

```javascript
// Add this to your bonus button click handler
function showRewardedAd() {
  if (typeof google !== 'undefined' && google.ima) {
    // AdMob rewarded ad implementation
    // This requires more complex setup with the Google IMA SDK
  }
}
```

### Step 5: Test Ads

Before going live:

1. Add your device as a test device in AdMob settings
2. Use test ad unit IDs provided by Google
3. Verify ads display correctly
4. Check console for any errors

### Step 6: Deploy

1. Update your code with actual ad unit IDs
2. Commit and push to repository
3. Deploy to your hosting provider

## AdMob Monetization Strategies for Social Casinos

### Strategy 1: Rewarded Ads for Bonuses
- "Watch a 30-second ad to get 5,000 bonus coins"
- Increases user engagement and session length
- Users opt-in, so better user experience

### Strategy 2: Interstitial Ads Between Sessions
- Show after 3-5 game rounds
- Full-screen ads with high engagement
- Can significantly boost revenue

### Strategy 3: Banner Ads (Passive)
- Persistent banner at top or bottom
- Low impact on gameplay
- Steady baseline revenue

## Important Compliance Notes

✅ **Allowed:**
- Rewarded ads that give in-game currency
- Banner and interstitial ads
- Ads from non-gambling advertisers

❌ **NOT Allowed:**
- Real-money gambling ads
- Ads that encourage gambling
- Misleading ad placements
- Ads that violate AdMob policies

## Revenue Expectations

Typical CPM (Cost Per Mille) rates for gaming content:
- **AdSense**: $0.50 - $3.00 per 1000 impressions
- **AdMob**: $1.00 - $5.00+ per 1000 impressions (gaming)

Actual earnings depend on:
- Traffic volume
- User location (US/UK traffic pays more)
- Ad quality and relevance
- User engagement

## Hybrid Approach (Recommended)

For maximum revenue, use **both AdSense and AdMob**:

1. **AdSense**: For general display ads
2. **AdMob**: For rewarded ads and interstitials

This provides:
- Multiple revenue streams
- Better fill rates
- Improved user experience (rewarded ads feel less intrusive)
- Higher overall earnings

## Next Steps

1. Decide between AdSense, AdMob, or both
2. Set up your account(s)
3. Create ad units
4. Implement in Neonlucky
5. Test thoroughly
6. Monitor performance and optimize

## Resources

- [Google AdMob Documentation](https://support.google.com/admob)
- [AdMob Best Practices](https://support.google.com/admob/answer/6001347)
- [Gaming Monetization Guide](https://support.google.com/admob/answer/9989328)

## Support

For AdMob support: [Google AdMob Help Center](https://support.google.com/admob)
