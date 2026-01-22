# SPR Software Website

A minimal single-page static website designed to meet Stripe's business verification requirements.

## Project Structure

```
spr-software/
├── index.html    # Main single-page website
├── styles.css    # Responsive styling
├── README.md     # This file
└── .gitignore    # Git ignore rules
```

## Placeholder Replacement Checklist

Before deploying, replace all placeholder text in `index.html`:

### Required (Critical for Stripe Verification)

- [ ] `[REQUIRED: Your registered business address]` - Must match Companies House registration
- [ ] `[REQUIRED: City, Postcode]` - Complete address
- [ ] `[REQUIRED: Business phone number]` - Monitored phone line
- [ ] `[REQUIRED: Business email address]` - Professional email address

### Recommended

- [ ] `[PLACEHOLDER: Add your company tagline/mission statement]` - Header tagline
- [ ] `[PLACEHOLDER: Add company registration number]` - About section
- [ ] `[PLACEHOLDER: Add year established]` - About section
- [ ] `[PLACEHOLDER: List your SaaS products with brief descriptions once available]` - Services section
- [ ] `[PLACEHOLDER: Companies House number]` - Contact section
- [ ] `[PLACEHOLDER: VAT number if registered]` - Contact section (remove if not VAT registered)
- [ ] `[PLACEHOLDER: Add date]` - Privacy Policy and Terms dates
- [ ] `[PLACEHOLDER: Add your Data Protection Officer contact if applicable]` - Privacy section (remove if not applicable)
- [ ] `[PLACEHOLDER: Define your refund policy]` - Terms section
- [ ] `[PLACEHOLDER: Specify jurisdiction]` - Terms section (likely "England and Wales")
- [ ] `[PLACEHOLDER: "Registered in England and Wales. Company No: XXXXXXXX"]` - Footer

## Deployment Options

### Option 1: GitHub Pages (Recommended)

1. Create a new repository on GitHub
2. Push your code:
   ```bash
   git init
   git add .
   git commit -m "Initial website"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/spr-software.git
   git push -u origin main
   ```
3. Go to repository Settings > Pages
4. Under "Source", select "Deploy from a branch"
5. Select "main" branch and "/ (root)" folder
6. Click Save
7. Your site will be live at `https://YOUR_USERNAME.github.io/spr-software/`

**Custom Domain Setup (GitHub Pages):**
1. In repository Settings > Pages > Custom domain, enter your domain
2. Add DNS records with your domain registrar:
   - For apex domain (example.com): A records pointing to GitHub's IPs:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153
   - For www subdomain: CNAME record pointing to `YOUR_USERNAME.github.io`
3. Enable "Enforce HTTPS" once DNS propagates

### Option 2: Netlify

**Via Git:**
1. Push code to GitHub/GitLab/Bitbucket
2. Log in to [Netlify](https://netlify.com)
3. Click "Add new site" > "Import an existing project"
4. Connect your repository
5. Deploy settings: leave defaults (no build command needed)
6. Click "Deploy site"

**Via Drag-and-Drop:**
1. Log in to [Netlify](https://netlify.com)
2. Drag the project folder onto the deploy area
3. Site deploys instantly

**Custom Domain (Netlify):**
1. Go to Site settings > Domain management
2. Click "Add custom domain"
3. Follow DNS configuration instructions provided

### Option 3: Vercel

1. Push code to GitHub
2. Log in to [Vercel](https://vercel.com)
3. Click "Add New" > "Project"
4. Import your repository
5. Framework Preset: "Other"
6. Click "Deploy"

**Custom Domain (Vercel):**
1. Go to Project Settings > Domains
2. Add your domain
3. Configure DNS as instructed

## SSL/HTTPS

All three hosting platforms provide automatic HTTPS via Let's Encrypt:
- **GitHub Pages**: Automatic once custom domain is verified
- **Netlify**: Automatic for all sites
- **Vercel**: Automatic for all sites

## Pre-Stripe Verification Checklist

Before applying for Stripe:

- [ ] Website is live and accessible via HTTPS
- [ ] Custom domain configured (e.g., sprsoftware.co.uk)
- [ ] All placeholder text replaced with actual business information
- [ ] Business address matches Companies House registration exactly
- [ ] Contact information is accurate and monitored
- [ ] Privacy Policy includes GDPR/UK DPA 2018 compliance
- [ ] Terms of Service mentions Stripe as payment processor
- [ ] Website clearly describes your services/products

## Local Development

To preview locally, simply open `index.html` in a web browser. For a local server:

```bash
# Python 3
python -m http.server 8000

# Node.js (if npx available)
npx serve .
```

Then visit `http://localhost:8000`

## Customisation

### Colours

Edit `styles.css` to change the colour scheme. Key variables:
- Primary blue: `#1a365d` (header, footer, headings)
- Accent blue: `#3182ce` (links, decorative elements)
- Light background: `#f7fafc` (alternating sections)

### Typography

The site uses system fonts for optimal performance. To use custom fonts, add a Google Fonts link to `index.html` and update the `font-family` in `styles.css`.

## Support

For questions about Stripe verification requirements, consult:
- [Stripe Support](https://support.stripe.com)
- [Stripe Verification Guide](https://stripe.com/docs/connect/identity-verification)
