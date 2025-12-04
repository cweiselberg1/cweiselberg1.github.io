# Professional Portfolio - Google Sites Embedding Guide

## Portfolio Overview

Your professional portfolio consists of 5 pages:
1. **Home** - Overview and value proposition
2. **About** - Professional background and contact info
3. **Workflows** - Process optimization examples
4. **Customer Communications** - Communication strategy showcase
5. **Process Mapping** - Visual process documentation examples

All pages share a consistent navigation bar and professional design.

## Files Location

Your portfolio is located at:
`/Users/chuckw./Documents/chuckw-websites/portfolio-site/`

**Files:**
- `index.html` (Home page)
- `about.html`
- `workflows.html`
- `customer-communications.html`
- `process-mapping.html`
- `styles.css` (Shared stylesheet)

## Embedding Methods

### Method 1: GitHub Pages (RECOMMENDED)

This is the best method for a professional multi-page portfolio.

#### Step 1: Create GitHub Repository
1. Go to https://github.com and sign in
2. Click "New repository"
3. Repository name: `portfolio` (or any name you prefer)
4. Set to **Public**
5. Initialize with README: Optional
6. Click "Create repository"

#### Step 2: Upload All Files
1. In your repository, click "Add file" → "Upload files"
2. Drag and drop ALL files from `/portfolio-site/` folder:
   - index.html
   - about.html
   - workflows.html
   - customer-communications.html
   - process-mapping.html
   - styles.css
3. Commit the files (click "Commit changes")

#### Step 3: Enable GitHub Pages
1. Go to repository Settings
2. Click "Pages" in left sidebar
3. Under "Source", select **main** branch
4. Click "Save"
5. Wait 2-3 minutes for deployment
6. Your portfolio will be live at: `https://yourusername.github.io/portfolio/`

#### Step 4: Embed in Google Sites

**Option A: Embed Full Site (Recommended)**
1. In Google Sites, click "Insert" → "Embed"
2. Click "Embed code"
3. Paste this code (replace USERNAME and REPO):

```html
<iframe src="https://USERNAME.github.io/REPO/"
        width="100%"
        height="1000"
        frameborder="0"
        style="border:0;">
</iframe>
```

4. Click "Insert"

**Option B: Embed Individual Pages**

For more control, embed each page separately on different Google Sites pages:

Home page:
```html
<iframe src="https://USERNAME.github.io/REPO/index.html" width="100%" height="1000" frameborder="0"></iframe>
```

About page:
```html
<iframe src="https://USERNAME.github.io/REPO/about.html" width="100%" height="1200" frameborder="0"></iframe>
```

Workflows page:
```html
<iframe src="https://USERNAME.github.io/REPO/workflows.html" width="100%" height="1400" frameborder="0"></iframe>
```

Customer Communications page:
```html
<iframe src="https://USERNAME.github.io/REPO/customer-communications.html" width="100%" height="1400" frameborder="0"></iframe>
```

Process Mapping page:
```html
<iframe src="https://USERNAME.github.io/REPO/process-mapping.html" width="100%" height="1400" frameborder="0"></iframe>
```

### Method 2: Google Drive

If you prefer using Google Drive:

#### Step 1: Upload to Google Drive
1. Go to Google Drive
2. Create a new folder named "Portfolio"
3. Upload ALL files to this folder
4. Share the folder: Right-click → "Share" → "Anyone with the link can view"

#### Step 2: Get File IDs
For each HTML file, right-click → "Get link" and copy the file ID from the URL.

Example URL: `https://drive.google.com/file/d/1AbCdEfG123456/view`
File ID: `1AbCdEfG123456`

#### Step 3: Embed in Google Sites

Note: Google Drive embedding has limitations with multi-file sites and CSS may not load properly. GitHub Pages is strongly recommended.

If you still want to try:
```html
<iframe src="https://drive.google.com/file/d/FILE_ID/preview"
        width="100%"
        height="1000"
        frameborder="0">
</iframe>
```

**Important:** The `styles.css` file may not load correctly with this method, causing pages to appear unstyled.

### Method 3: Web Hosting Service

For a more professional setup:

1. **Purchase hosting** (e.g., Bluehost, SiteGround, Hostinger)
2. **Upload all files** via FTP or cPanel File Manager
3. **Access at your domain**: `https://yourdomain.com`
4. **Embed in Google Sites**:

```html
<iframe src="https://yourdomain.com"
        width="100%"
        height="1000"
        frameborder="0">
</iframe>
```

## Customizing Your Portfolio

### Update Your Information

**Contact Details (Multiple Pages)**
Search for and replace:
- `your.email@example.com` → Your actual email
- `linkedin.com/in/yourprofile` → Your LinkedIn URL
- `github.com/yourprofile` → Your GitHub URL (if applicable)

**Home Page (`index.html`)**
- Line 41: Update title and tagline
- Lines 47-53: Update value proposition text
- Lines 77-90: Update impact statistics

**About Page (`about.html`)**
- Lines 46-49: Update professional summary
- Lines 61-96: Update skills and competencies
- Lines 103-141: Update work experience
- Lines 148-159: Update education

**Workflows Page (`workflows.html`)**
- Lines 63-143: Replace with your actual workflow examples
- Update statistics and results

**Customer Communications Page (`customer-communications.html`)**
- Lines 97-167: Update email campaign details
- Lines 172-225: Customize communication templates

**Process Mapping Page (`process-mapping.html`)**
- Lines 108-218: Replace with your actual process maps
- Update improvement statistics

### Customize Colors

The portfolio uses a purple gradient color scheme. To change:

**In `styles.css`, find and replace:**
- `#667eea` (Light Purple) → Your primary color
- `#764ba2` (Dark Purple) → Your secondary color
- `#2c3e50` (Dark Blue-Gray) → Your text color

**Color Scheme Suggestions:**
- Professional Blue: `#0066cc` and `#004080`
- Corporate Gray: `#4a5568` and `#2d3748`
- Modern Teal: `#06b6d4` and `#0891b2`
- Energetic Orange: `#ff6b35` and `#f7931e`

### Adjust Heights for Embedding

If content is cut off in the iframe, increase the height values:

- Home page: 1000px (usually sufficient)
- About page: 1200px
- Workflows: 1400px (has more content)
- Customer Communications: 1400px
- Process Mapping: 1400px

Adjust as needed based on your content length.

## Testing Your Portfolio

### Before Embedding:

1. **Local Testing:** Open each HTML file in a browser
2. **Check All Links:** Ensure navigation works
3. **Mobile View:** Test on phone/tablet
4. **Content Review:** Proofread all text

### After Embedding:

1. **Navigation:** Click through all menu items
2. **Responsive Design:** Test on different screen sizes
3. **Load Time:** Check that pages load quickly
4. **Cross-Browser:** Test in Chrome, Safari, Firefox

## Troubleshooting

### Navigation Links Don't Work
**Problem:** Clicking nav links doesn't change pages in iframe
**Solution:** This is expected with iframe embedding. Each page needs to be embedded separately in Google Sites, OR use GitHub Pages for full navigation.

### CSS Styles Not Loading
**Problem:** Pages look plain/unstyled
**Solution:**
- Ensure `styles.css` is uploaded in the same directory as HTML files
- Use GitHub Pages instead of Google Drive
- Check browser console for errors (F12)

### Content Cut Off
**Problem:** Bottom of page not visible
**Solution:** Increase iframe height in embed code

### Pages Load Slowly
**Problem:** Portfolio takes time to appear
**Solution:**
- Optimize images (if you add any)
- Use GitHub Pages or proper hosting
- Check internet connection

### Can't Edit After Embedding
**Problem:** Need to make changes
**Solution:**
- Edit local HTML files
- Re-upload to GitHub/hosting
- Changes appear automatically (may need to refresh)

## Advanced: Custom Domain

If using GitHub Pages, you can add a custom domain:

1. Purchase domain (e.g., charlieweiselberg.com)
2. In GitHub repository settings → Pages
3. Add your custom domain
4. Update DNS settings with your domain registrar
5. Portfolio accessible at your domain

## Support Resources

- **GitHub Pages Documentation:** https://pages.github.com/
- **Google Sites Help:** https://support.google.com/sites
- **Bootstrap Documentation:** https://getbootstrap.com/docs/3.3/

## File Structure Summary

```
portfolio-site/
├── index.html              (Home - Landing page)
├── about.html             (About - Background & contact)
├── workflows.html          (Workflows - Process optimization)
├── customer-communications.html (Communications - Strategy)
├── process-mapping.html   (Process Maps - Visual documentation)
└── styles.css             (Shared styles for all pages)
```

## Best Practices

1. **Keep It Updated:** Regularly update with new projects/achievements
2. **Optimize for SEO:** Use descriptive meta tags (already included)
3. **Professional Email:** Use a professional email address
4. **LinkedIn Integration:** Keep LinkedIn profile current
5. **Analytics:** Consider adding Google Analytics to track visits
6. **Backup:** Keep copies of all files
7. **Mobile-First:** Always test on mobile devices

## Next Steps

1. ✅ Review and customize all content
2. ✅ Update contact information
3. ✅ Choose embedding method (GitHub Pages recommended)
4. ✅ Upload files
5. ✅ Test all functionality
6. ✅ Embed in Google Sites
7. ✅ Share with potential employers/clients!

---

**Need Help?** All files are self-contained and use standard Bootstrap 3. Any web developer can help if you need assistance.

**Your portfolio is ready to showcase your professional expertise!**
