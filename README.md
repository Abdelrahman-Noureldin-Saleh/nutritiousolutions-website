# Nutritious Solutions Website

Welcome! This is the complete website for **Nutritious Solutions** by Haidy Youssef, CDN.

This guide will walk you through **step-by-step** how to get your website live on the internet. Don't worry if you're not technical — we'll explain everything in simple terms!

---

## 📋 What's Included

This website has:
- ✅ **7 pages**: Home, About Me, Services, Appointments, Blog, Testimonials, and Nutrify Services
- ✅ **8 blog posts** with full content
- ✅ **6 client testimonials**
- ✅ **All images** from your emails already organized
- ✅ **Mobile-friendly design** (works on phones, tablets, and computers)
- ✅ **Professional color scheme** matching your brand (sage green, teal, coral)

---

## 🌐 How to Get Your Website Online

There are **3 main steps**:

1. **Buy hosting** (a place on the internet to store your website files)
2. **Upload your website files** to that hosting
3. **Connect your domain name** to your hosting

Let's go through each step together!

---

## Step 1: Buy Hosting from Namecheap

**What is hosting?** Think of hosting like renting a storage unit for your website. Your website files need to live somewhere on the internet so people can visit them.

### Instructions:

1. Go to [Namecheap.com](https://www.namecheap.com) and **log in** to your account (the same account where you bought your domain name)

2. In the top menu, click **"Hosting"** → then click **"Shared Hosting"**

3. You'll see different hosting plans. For this website, the **"Stellar" plan** is perfect (around $2-3/month). Click **"Add to Cart"**

4. During checkout:
   - **Duration**: Choose at least 1 year (you get a discount for longer periods)
   - **Auto-renewal**: You can turn this ON so your hosting doesn't expire accidentally
   - **Domain**: Select your domain name from the dropdown (the one you already own)

5. Complete the payment

6. Wait for the **confirmation email** from Namecheap — this usually arrives within 5-10 minutes

---

## Step 2: Upload Your Website Files to Hosting

**What are we doing here?** We're moving all the website files from your computer to Namecheap's servers (the hosting you just bought) so people on the internet can see them.

### Instructions:

### A. Access Your Hosting Control Panel (cPanel)

1. Go to [Namecheap.com](https://www.namecheap.com) and **log in**

2. Click on your profile icon (top right) → **"Dashboard"**

3. In the left sidebar, click **"Hosting List"**

4. Find your hosting package and click **"Manage"**

5. Scroll down and click the button that says **"Go to cPanel"**
   - **What is cPanel?** It's like the "control center" for your hosting — a dashboard where you manage your website files

### B. Upload the Website Files

1. Once you're in cPanel, scroll down to the **"Files"** section

2. Click on **"File Manager"**
   - A new tab will open showing your hosting files and folders

3. In File Manager, look for a folder called **`public_html`** and **double-click it to open it**
   - **What is public_html?** This is the special folder where your website files must go. Anything in this folder will be visible on the internet at your domain name

4. **Delete any files already in public_html**:
   - You might see files like `index.html`, `cgi-bin`, or `.htaccess`
   - Select them all (click the checkbox at the top) → click **"Delete"** at the top menu
   - **Why?** Namecheap puts default "Coming Soon" files there. We need to replace them with your real website.

5. Now **upload your website files**:
   - Click the **"Upload"** button at the top of File Manager
   - A new page will open

6. **On your computer**, open the folder where you downloaded this website. You should see these items:
   ```
   index.html
   css (folder)
   js (folder)
   images (folder)
   pages (folder)
   ```

7. **Drag and drop** OR **click "Select File"** and upload:
   - `index.html`
   - The `css` folder
   - The `js` folder
   - The `images` folder
   - The `pages` folder

   **Important:** Make sure you upload the *folders themselves*, not just the files inside them!

8. Wait for all files to finish uploading (you'll see a progress bar)

9. Click **"Go Back to /public_html"** when done

10. You should now see:
    ```
    public_html/
    ├── index.html
    ├── css/
    ├── js/
    ├── images/
    └── pages/
    ```

---

## Step 3: Connect Your Domain Name to Your Hosting

**What are we doing here?** Your domain name (like `nutritiousolutions.com`) needs to "point" to your hosting so when people type your website address, they see your website.

### Instructions:

**Good news!** If you bought your domain AND hosting from the same Namecheap account, they should already be connected automatically. But let's verify:

1. Go back to your Namecheap **Dashboard**

2. Click **"Domain List"** in the left sidebar

3. Find your domain name and click **"Manage"**

4. Scroll down to the **"Nameservers"** section

5. Make sure it says **"Namecheap BasicDNS"** or **"Namecheap PremiumDNS"**
   - If it says something else (like "Custom DNS"), change it:
     - Select the dropdown and choose **"Namecheap BasicDNS"**
     - Click the green checkmark to save

6. Scroll further down to **"Advanced DNS"** tab → click it

7. Under **"Host Records"**, make sure there are 2 records that look like this:

   | Type | Host | Value |
   |------|------|-------|
   | A Record | @ | (some IP address) |
   | CNAME Record | www | (your domain name) |

   **What are these?** These are "directions" that tell the internet where your website lives.

   - If they're **already there** — you're all set!
   - If they're **missing**, click **"Add New Record"**:
     - **For the A Record:**
       - Type: `A Record`
       - Host: `@`
       - Value: Go back to cPanel → look for your **Server IP** (usually shown on the right sidebar)
       - TTL: `Automatic`
     - **For the CNAME Record:**
       - Type: `CNAME Record`
       - Host: `www`
       - Value: `yourdomain.com` (replace with your actual domain)
       - TTL: `Automatic`

8. Click **Save All Changes**

---

## Step 4: Wait & Test (Usually 5-30 Minutes)

**What's happening?** The internet needs a bit of time to "update" and connect your domain to your hosting. This is called **DNS propagation**.

1. Wait **5-30 minutes** (sometimes up to 24 hours, but usually much faster)

2. Open a **new browser tab** (Chrome, Safari, Firefox, etc.)

3. Type your domain name in the address bar:
   - `yourdomain.com`
   - `www.yourdomain.com`

4. **If you see your website** — Congratulations! You're live! 🎉

5. **If you see an error or "Coming Soon" page**:
   - Wait a bit longer (try again in 15 minutes)
   - Clear your browser cache (Google: "how to clear cache on [your browser]")
   - Try visiting from a different device or browser

---

## ✏️ Before You Go Live: Add Your Missing Info

Your website has a few placeholder spots that need to be filled in. Here's what you need to update:

### 1. **Add Your Phone Number**

**File to edit:** `pages/appointments.html`

1. Open `pages/appointments.html` in a text editor (Notepad on Windows, TextEdit on Mac)

2. Find this line (around line 73):
   ```html
   <p>📞 <span style="opacity:0.7;">Coming soon</span></p>
   ```

3. Replace it with:
   ```html
   <p>📞 <a href="tel:+1234567890">+1 (234) 567-890</a></p>
   ```
   *(Use your actual phone number)*

4. Save the file

### 2. **Add Your Booking Links**

**File to edit:** `pages/appointments.html`

1. Find this line (around line 63):
   ```html
   <a href="#" class="btn btn-primary">Book Now</a>
   ```

2. Replace the `#` with your actual booking software URL:
   ```html
   <a href="https://your-booking-link.com" class="btn btn-primary">Book Now</a>
   ```

3. Find this line (around line 70):
   ```html
   <a href="#" class="btn btn-teal">Schedule a Call</a>
   ```

4. Replace the `#` with your discovery call URL

5. Save the file

### 3. **Add Social Media Links**

**Files to edit:** `index.html` and `pages/about.html`

1. Open `index.html`, find (around line 78):
   ```html
   <a href="#" aria-label="Facebook">📘 Facebook</a>
   <a href="#" aria-label="Instagram">📷 Instagram</a>
   ```

2. Replace the `#` with your actual social media links:
   ```html
   <a href="https://facebook.com/yourpage" aria-label="Facebook">📘 Facebook</a>
   <a href="https://instagram.com/yourpage" aria-label="Instagram">📷 Instagram</a>
   ```

3. Save the file

4. Repeat the same process for `pages/about.html` (around line 70)

### 4. **Re-upload After Edits**

After you make these changes:
1. Go back to **cPanel → File Manager → public_html**
2. Delete the old `index.html` and `pages/appointments.html`
3. Upload the new edited versions

---

## 🆘 Troubleshooting

### "My website isn't showing up"

**Possible causes:**
- **DNS propagation takes time** → Wait 30 minutes to 24 hours
- **Files in wrong folder** → Make sure everything is in `public_html`, not a subfolder
- **Browser cache** → Clear your browser cache or try incognito/private mode
- **Nameservers wrong** → Go back to Step 3 and verify your nameservers

### "Images aren't loading"

- Make sure you uploaded the entire `images` folder (not just the files inside)
- Check that the folder is at `public_html/images/` (not `public_html/public_html/images/`)

### "The website looks weird on mobile"

- The website is already mobile-friendly! Make sure you're testing after uploading all CSS files
- Clear your mobile browser cache

### "I see a folder list instead of my website"

- You're missing `index.html` in `public_html`
- Make sure `index.html` is directly in `public_html` (not in a subfolder)

---

## 📧 Need More Help?

If you get stuck:

1. **Namecheap Support** (they're available 24/7):
   - Live Chat: [https://www.namecheap.com/support/live-chat/](https://www.namecheap.com/support/live-chat/)
   - Tell them: *"I need help uploading my website files to my shared hosting"*

2. **YouTube Tutorials**:
   - Search: *"How to upload website to Namecheap cPanel"*
   - There are many video guides that show this process visually

3. **Email the developer** (the person who gave you this guide)

---

## ✅ Checklist

Before you consider yourself "done", make sure:

- [ ] You can visit `yourdomain.com` and see your website
- [ ] You can visit `www.yourdomain.com` and see your website
- [ ] All pages work (Home, About, Services, Appointments, Blog, Testimonials, Nutrify)
- [ ] All blog posts open correctly
- [ ] Images are loading
- [ ] You've added your phone number
- [ ] You've added your booking links
- [ ] You've added your social media links
- [ ] The website looks good on your phone

---

## 🎉 You're Done!

Your website is now live on the internet. Anyone can visit it by typing your domain name!

**What's Next?**

- Share your website link on social media
- Add it to your email signature
- Submit it to Google Search Console (so it shows up in Google search)
- Monitor your email for client inquiries through the contact form

**Congratulations on your new website!** 🌿

---

## 📝 Technical Details (For Developers)

This is a static HTML/CSS website with:
- **Vanilla JavaScript** (no frameworks)
- **Google Fonts** (Playfair Display, Dancing Script, Lato)
- **Responsive design** (mobile-first approach)
- **No database required** (pure static files)
- **No backend/server-side code** (HTML/CSS/JS only)

All files can be hosted on any static web host (Namecheap, GitHub Pages, Netlify, Vercel, etc.).

---

*Website built from email specifications — February 2026*
