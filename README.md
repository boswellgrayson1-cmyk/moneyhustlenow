# MoneyHustleNow

A simple, fast-loading website focused on helping people find legitimate side hustles and ways to make money near them.

## About This Project

MoneyHustleNow provides curated lists of side hustles, gig apps, and money-making opportunities that are available in most cities. The site includes:

- **Side Hustles Near Me** - Local and flexible income opportunities
- **Side Jobs Near Me** - Traditional part-time jobs that hire quickly
- **Ways to Make Money Near Me** - Various income strategies
- **Gig Apps Near Me** - App-based earning opportunities
- **50 Side Hustles Guide** - A $7 digital product with detailed side hustle information

## Project Structure

```
/
├── index.html                          # Homepage (Side Hustles Near Me)
├── side-hustles-near-me.html          # Side hustles listing page
├── side-jobs-near-me.html             # Side jobs listing page
├── ways-to-make-money-near-me.html    # Ways to make money page
├── gig-apps-near-me.html              # Gig apps listing page
├── product-50-side-hustles.html       # Product sales page ($7 guide)
├── styles.css                          # Main stylesheet
├── sitemap.xml                         # SEO sitemap
├── robots.txt                          # Search engine crawler instructions
├── CNAME                               # Custom domain configuration
└── README.md                           # This file
```

## Setup Instructions

### 1. Local Development

To run this site locally:

1. Clone the repository:
   ```bash
   git clone https://github.com/boswellgrayson1-cmyk/moneyhustlenow.git
   cd moneyhustlenow
   ```

2. Open `index.html` in your web browser, or use a local server:
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Node.js (http-server)
   npx http-server
   ```

3. Navigate to `http://localhost:8000` in your browser

### 2. GitHub Pages Deployment

This site is configured to deploy via GitHub Pages:

1. The site is already configured with a `CNAME` file for `moneyhustlenow.com`
2. Go to your repository Settings → Pages
3. Set Source to the `main` branch (or your default branch)
4. GitHub will automatically deploy your site

### 3. Domain Configuration

The site is configured for the custom domain `moneyhustlenow.com`.

**DNS Configuration Steps:**

1. Go to your domain registrar's DNS settings
2. Add the following DNS records:

   **For apex domain (moneyhustlenow.com):**
   ```
   Type: A
   Name: @
   Value: 185.199.108.153
   
   Type: A
   Name: @
   Value: 185.199.109.153
   
   Type: A
   Name: @
   Value: 185.199.110.153
   
   Type: A
   Name: @
   Value: 185.199.111.153
   ```

   **For www subdomain:**
   ```
   Type: CNAME
   Name: www
   Value: boswellgrayson1-cmyk.github.io
   ```

3. Wait for DNS propagation (can take up to 48 hours, usually much faster)
4. In your GitHub repository settings, enable HTTPS for your custom domain

### 4. Payment Integration Setup

The `product-50-side-hustles.html` page includes a "Buy Now for $7" button that needs payment integration.

**Recommended Options:**

#### Option 1: Gumroad (Easiest for Digital Products)
1. Sign up at [gumroad.com](https://gumroad.com)
2. Create a new product:
   - Set price: $7
   - Upload your "50 Side Hustles" PDF guide
   - Configure delivery settings
3. Copy your product's share link
4. Update the button href in `product-50-side-hustles.html`:
   ```html
   <a class="button" href="https://yourname.gumroad.com/l/yourproduct">Buy Now for $7</a>
   ```

#### Option 2: Stripe Payment Links
1. Sign up at [stripe.com](https://stripe.com)
2. Create a Payment Link:
   - Product: "50 Side Hustles Guide"
   - Price: $7
   - One-time payment
3. Copy the payment link
4. Update the button href with your Stripe payment link

#### Option 3: PayPal
1. Log into your PayPal Business account
2. Go to Merchant Services → PayPal Buttons
3. Create a "Buy Now" button for $7
4. Replace the button code in the HTML file

#### Option 4: Buy Me a Coffee
1. Sign up at [buymeacoffee.com](https://buymeacoffee.com)
2. Create a digital product or membership
3. Use your Buy Me a Coffee link

**After setting up payments:**
- Test the purchase flow
- Ensure customers receive the digital product automatically
- Update the payment button text if needed

## Technology Stack

- **HTML5** - Semantic markup
- **CSS3** - Responsive styling
- **Vanilla JavaScript** - Minimal JS for dynamic year in footer
- **No build process** - Simple, static site

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## SEO Features

- Semantic HTML structure
- Meta descriptions on all pages
- Responsive viewport configuration
- Sitemap.xml for search engines
- robots.txt for crawler control
- Fast loading (no dependencies)

## Content Updates

To update content:

1. Edit the relevant HTML file
2. Maintain the existing structure (header, nav, main, footer)
3. Keep navigation links consistent across all pages
4. Test all changes locally before committing
5. Commit and push to deploy via GitHub Pages

## License

See the [LICENSE](LICENSE) file for details.

## Support

For questions or issues with the site, please open an issue in this repository.

---

**Live Site:** https://moneyhustlenow.com  
**Repository:** https://github.com/boswellgrayson1-cmyk/moneyhustlenow
