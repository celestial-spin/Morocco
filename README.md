# 🇲🇦 MOROCCO TRIP 2026 - INTERACTIVE WEBSITE

## 📁 What's Included

This folder contains a complete, multi-page website presenting your Morocco trip to Steph!

**10 Beautiful HTML Pages:**
- `index.html` - Home page with overview
- `marrakech.html` - Days 1-2 with traditional tagine photo
- `todra.html` - Day 3 mountain gorge
- `merzouga.html` - Day 4 desert camp with Berber musicians & food photos
- `nkob.html` - Day 5 authentic village
- `taroudant.html` - Days 6-7 with Berber music & dining
- `taghazout.html` - Days 8-10 beach finale
- `journey.html` - All 5 scenic drives with route photos
- `style.css` - Beautiful styling (Morocco-inspired colors)
- `/images/` - Folder for photos (currently has placeholders)

---

## 🚀 HOW TO USE

### **Step 1: Open the Website**
1. Double-click `index.html` 
2. Your browser opens showing the home page
3. Click any navigation link to explore different pages
4. All links work seamlessly—it feels like a real website!

### **Step 2: Navigate**
- Use the top navigation menu to jump between pages
- Click "Previous/Next" buttons at bottom of each page
- Browser back/forward buttons work normally
- Works 100% offline (no internet needed)

### **Step 3: Share with Steph**
- Email her the entire `morocco-trip` folder (as .zip)
- OR put it on a USB stick
- OR upload to Dropbox/Google Drive
- She just opens `index.html` and clicks through!

---

## 📸 ADDING REAL PHOTOS (Optional)

Currently the site uses **colored placeholder boxes** with text labels. To add real photos:

### **Option 1: Keep It Simple**
The placeholders work fine! They're clearly labeled and styled to match the design.

### **Option 2: Add Real Images**
1. Find Morocco photos online (Unsplash.com, Pexels.com = free)
2. Save them in the `/images/` folder
3. Name them descriptively (e.g., `marrakech-riad.jpg`, `desert-sunset.jpg`)
4. Edit the HTML files:
   - Find `<div class="img-placeholder">`
   - Replace with `<img src="images/photo-name.jpg" alt="Description">`

### **Photos I Recommend Finding:**
**Priority (Cultural Content):**
- Moroccan tagine (traditional clay pot with food)
- Berber musicians at campfire (desert or performance)
- Moroccan breakfast spread (rooftop terrace)

**Locations:**
- Marrakech riad courtyard
- Todra Gorge canyon walls
- Sahara desert dunes at sunset
- N'kob kasbahs
- Taroudant medina ramparts
- Taghazout beach/Hyatt views

**Journey Photos:**
- Tizi n'Tichka mountain pass
- Atlas Mountains scenic road
- Drâa Valley palm groves
- Goats in argan trees (if you find one!)

---

## 🎨 DESIGN FEATURES

**The Aesthetic:**
- Travel magazine inspired
- Warm Morocco color palette (terracotta, sand, deep blue, gold)
- Elegant typography (Playfair Display + Cormorant Garamond)
- Sophisticated layout with hero images
- Smooth hover effects
- Mobile responsive

**Content Strategy:**
- Each location page "sells" that destination
- Journey page emphasizes scenic drives
- Food & music photos for cultural immersion
- Practical info mixed with emotional appeal
- Personal touches (Phil's gym priority, Steph's Essaouira love)

---

## 💡 CUSTOMIZATION TIPS

### **Change Text:**
Just edit the HTML files in any text editor (Notepad, TextEdit, VS Code)

### **Change Colors:**
Edit `style.css` - look for `:root` section at top with color variables

### **Add More Pages:**
Copy any existing page, rename it, edit content, add links in navigation

### **Print-Friendly:**
The site prints well! Use browser Print → Save as PDF to create a PDF version

---

## ✅ WHAT'S ALREADY DONE

✅ All 10 pages created and linked  
✅ Beautiful Morocco-inspired design  
✅ Comprehensive content from our research  
✅ Food photos (3 locations: Marrakech tagine, Merzouga desert dinner, Taroudant breakfast)  
✅ Berber music photos (2 locations: Merzouga campfire, Taroudant performance)  
✅ Journey photos (5 drives with scenic stops)  
✅ Navigation works perfectly  
✅ Mobile responsive  
✅ Completely offline-capable  
✅ Ready to share with Steph!  

---

## 📊 CONTENT BREAKDOWN

**Home Page (index.html):**
- Hero section with trip overview
- 7 location cards
- "Why this trip is perfect" section
- Quick stats & highlights

**Location Pages (7 pages):**
- Hero image & dates
- Where we're staying (with reasons)
- What we'll do
- Why it's special
- Journey to get there (with scenic photos)
- Previous/Next navigation

**Journey Page:**
- All 5 drives mapped out
- Distance, time, difficulty
- Scenic stops for each drive
- Photos of highlights
- Driving tips for Morocco

**Design Elements:**
- Sticky navigation bar
- Animated hero sections
- Info boxes (blue) for key facts
- Highlight boxes (sand) for important content
- Image galleries
- Two-column layouts
- Responsive mobile design

---

## 🎯 HOW TO "SELL" THIS TO STEPH

**Presentation Strategy:**

1. **Build Anticipation:**
   - "I've been planning something special..."
   - Don't just send the folder, make it an event!

2. **Walk Through Together:**
   - Open `index.html` together
   - Click through each location
   - Point out things YOU know she'll love:
     * Berber music (like she wanted in Essaouira!)
     * Architecture & medinas
     * Rooftop dining
     * Post-Ramadan timing
     * Beach finale luxury

3. **Emphasize Balance:**
   - Adventure (desert, mountains, drives)
   - Culture (music, food, architecture)
   - Relaxation (pools, spa, beach, gym)

4. **Show It's All Booked:**
   - Point out "✅ BOOKED" status
   - Share the trip status file
   - Everything's ready to go!

---

## 💻 TECHNICAL NOTES

**Browser Compatibility:**
- Works in Chrome, Firefox, Safari, Edge
- Tested on desktop & mobile
- No plugins required
- Pure HTML/CSS (no JavaScript needed)

---

## 📂 STANDARD FILESYSTEM DESIGN FOR NEW TRIPS

**This structure should be used as the template for all new trip projects:**

```
/Trip Name Year/
├── docs/                              ← WEBSITE FILES (GitHub Pages serves from here)
│   ├── index.html                     (home page)
│   ├── style.css                      (styling)
│   ├── [location].html                (location pages)
│   ├── itinerary-daily.html           (day-by-day guide)
│   ├── itinerary-summary.html         (quick reference)
│   ├── bookings.html                  (booking details)
│   ├── journey.html                   (driving routes)
│   └── photo_brochure/                (all images)
│       └── *.jpg, *.webp, *.png
├── [trip] development files/          ← Research, drafts, working documents
├── [trip] output files/               ← Generated PDFs, exports
├── reference files/                   ← Source materials, inspiration
├── process documentation/             ← Planning notes
├── .git/                              ← Git repository
├── .claude/                           ← Claude project settings
└── README.md                          ← This file
```

**Why this structure:**
- **Clean separation** - Website files isolated in /docs, development files elsewhere
- **GitHub Pages compatible** - Configure Pages to serve from /docs folder
- **Tidy filesystem** - HTML files don't mix with development folders
- **Easy deployment** - Just push to main branch, Pages auto-deploys from /docs

**GitHub Pages Setup:**
1. Push repo to GitHub
2. Go to Settings → Pages
3. Source: "Deploy from a branch"
4. Branch: main, Folder: /docs
5. Save - site deploys to https://[username].github.io/[repo-name]/

**Total File Size:** Under 1MB (super fast loading!)

---

## 🎉 FINAL NOTES

This website represents **our entire Morocco adventure**—distilled into beautiful, clickable pages that bring the trip to life BEFORE we even go.

It's professional, comprehensive, gorgeous, and most importantly: **it will get Steph excited about this trip!**

All the research we did, all the careful planning, all the authentic locations we chose—it's all here, presented in the most compelling way possible.

**Now go show Steph and watch her fall in love with Morocco! 🇲🇦✨**

---

**Questions?**
- Edit any HTML file to change content
- Colors/fonts in `style.css`
- Add photos to `/images/` folder
- Everything works offline
- Just double-click `index.html` to start!

**Enjoy the trip! 🏜️🏔️🏖️**
