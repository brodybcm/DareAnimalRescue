# D.A.R.E. Animal Rescue Website Rebuild & Cost Elimination Guide

This repository contains the completely modernized, mobile-first website for **D.A.R.E. Animal Rescue, Inc.** (Defending, Advocating, Rescuing, Educating), a 501(c)(3) nonprofit in Valdosta, GA.

It replaces the legacy Web.com / Network Solutions website builder, which was charging roughly **$1,000 per year** for basic hosting and maintenance, and reduces ongoing costs to **$0/month forever**.

---

## 🐾 What Has Been Built

1. **Exact Navigation Menu & Submenus (1:1 with Original Site):**
   - `HOME`
   - `FOSTER/ADOPTION PROCESS` &rarr; *How to Become a Foster Parent*, *How to Adopt*, *Happy Endings*
   - `PETS FOR ADOPTION`
   - `VOLUNTEERING/PROGRAMS` &rarr; *How to Volunteer*, *Community Outreach*, *TNR*
   - `UPCOMING EVENTS`
   - `DONATE`
   - `CONTACT`
   - `REHOMING YOUR PET`
   - `OPTIONS FOR FOUND ANIMALS`
   - Mobile hamburger navigation drawer with collapsible sub-accordions.

2. **The 5 Teal Quick-Action Pill Buttons (Homepage Hero):**
   - `Foster Care Application` &rarr; Opens interactive Foster Care application modal.
   - `Adoption Application` &rarr; Opens interactive Adoption application modal.
   - `Our Pets on Pet Finder` &rarr; Direct link to D.A.R.E.'s active Petfinder organization portal (`dare-animal-rescue-ga834`).
   - `Rehoming Your Pet` &rarr; Jump link to the comprehensive owner rehoming guide.
   - `Options for Found Animals` &rarr; Jump link to the local lost/found animal protocol.

3. **Interactive & Printable Application Modals:**
   - **Foster Care Application**: Full screening form covering housing, fencing, existing pets, veterinary reference permission, and foster animal preferences. Printable with 1-click for physical signing or saving as PDF.
   - **Adoption Application**: Full screening form covering pet of interest, living environment, daily schedule, vet history, and agreement to the flat **$100 adoption donation** and 2-week foster-to-adopt trial period.

4. **Community Programs & Impact:**
   - Detailed **How to Adopt** section (7 stages + $100 fee breakdown covering spay/neuter, full vaccines, heartworm/FeLV test, and microchip).
   - **How to Become a Foster Parent** highlighting that **D.A.R.E. pays 100% of veterinary medical bills and supplies**.
   - **Trap-Neuter-Return (TNR)** community cat program in Lowndes County.
   - **Community Outreach** & **Volunteering Opportunities**.
   - **Upcoming Events** calendar cards (PetSmart Valdosta adoption days, supply drives).
   - **Rehoming Your Pet** safety advice (why never to advertise "free to good home", screening adopters).
   - **Options for Found Animals** (free microchip scanning at local vets, Lowndes County animal shelter reporting, D.A.R.E. Lost & Found contact).

5. **Donation & Contact Integrations:**
   - **PayPal One-Click Checkout** (`cmd=_s-xclick&hosted_button_id=D9ZYNDCUYBJRG`).
   - Physical check mailing instructions to `1709 A Gornto Road, PMB #322, Valdosta, GA 31601`.
   - Shelter wishlist.
   - Contact form, clickable phone hotline `(229) 242-1361`, email `dareanimalrescue@gmail.com`, and lost/found coordinator email `darelostandfound@gmail.com`.

6. **SEO & Discovery:**
   - Schema.org JSON-LD microdata for `NGO`, `AnimalShelter`, and `LocalBusiness` in Valdosta, GA.

---

## 💻 How to Test the Website Locally

No build tools, node modules, or installations are required:

1. Open your file explorer and navigate to `c:\Users\byron\Dare Animal Rescue\`.
2. Double-click **`index.html`** to open it in Chrome, Edge, Safari, or Firefox.
3. Everything works immediately right out of the box!

---

## 🚀 How to Host on GitHub Pages ($0/Month Forever)

**GitHub Pages** is completely free, supports custom domains (`dareanimalrescue.com`), provides a free automatic SSL security certificate (HTTPS), and requires zero server maintenance.

### Step 1: Create a Repository on GitHub
1. Sign in to your account at [github.com](https://github.com).
2. Click the **`+`** icon in the top right &rarr; **New repository**.
3. Name it (e.g. `dare-animal-rescue` or `dareanimalrescue`).
4. Set visibility to **Public** (required for free GitHub Pages).
5. Leave "Add a README file" unchecked (we already have one).
6. Click **Create repository**.

### Step 2: Push the Files to GitHub
Open your terminal or PowerShell in `c:\Users\byron\Dare Animal Rescue\` and run:

```bash
git init
git add .
git commit -m "Initial launch of new D.A.R.E. Animal Rescue website"
git branch -M main
git remote add origin https://github.com/<YOUR-GITHUB-USERNAME>/dare-animal-rescue.git
git push -u origin main
```
*(Replace `<YOUR-GITHUB-USERNAME>` with your actual GitHub username).*

Alternatively, you can drag and drop `index.html` and `README.md` directly into GitHub via your browser by clicking **"uploading an existing file"** on the repository page.

### Step 3: Enable GitHub Pages
1. In your GitHub repository, click **Settings** (gear tab at the top).
2. On the left sidebar menu, click **Pages**.
3. Under **Build and deployment**:
   - Source: Select **Deploy from a branch**.
   - Branch: Select **main** and folder **`/ (root)`**.
   - Click **Save**.
4. In about 60 seconds, your site will be live at `https://<YOUR-GITHUB-USERNAME>.github.io/dare-animal-rescue/`!

### Step 4: Add the Custom Domain (`dareanimalrescue.com`)
1. On that same GitHub **Pages** settings page, scroll down to **Custom domain**.
2. Type `dareanimalrescue.com` and click **Save**.
3. GitHub will create a `CNAME` file in your repository.
4. Check the box **Enforce HTTPS** once the certificate finishes provisioning.

### Step 5: Update DNS Records at the Domain Registrar
Log into wherever the domain `dareanimalrescue.com` is registered (e.g. Network Solutions, Web.com, GoDaddy, Namecheap, etc.) and update the DNS records:

1. **For the Apex Domain (`dareanimalrescue.com`)**, add or update the 4 GitHub Pages **A Records**:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`

2. **For the Subdomain (`www.dareanimalrescue.com`)**, add a **CNAME Record**:
   - Host / Name: `www`
   - Value / Points to: `<YOUR-GITHUB-USERNAME>.github.io`

---

## 💰 How to Safely Cancel the $1,000/Year Web.com Contract

> [!CAUTION]
> **DO NOT CANCEL THE DOMAIN REGISTRATION.**
> You only want to cancel the **hosting & website builder package**, while keeping ownership of the domain name `dareanimalrescue.com`.

1. **Log into her Web.com / Network Solutions account.**
2. Go to the **Domains** section and verify that `dareanimalrescue.com` is listed:
   - Ensure the domain contact email is set to `dareanimalrescue@gmail.com` or her personal email.
   - Ensure domain lock / auto-renew for the domain registration is active. (Optional: You can also transfer the domain registration to Cloudflare Registrar or Namecheap where annual renewal is only ~$10–$14/year).
3. Under **Subscriptions / Services / Products**:
   - Find the item labeled **Website Builder**, **Custom Website Package**, or **Hosting**.
   - Turn off auto-renewal or call Web.com customer service to cancel the hosting/maintenance subscription only.
   - Explicitly tell the representative: *"I am moving my website hosting to GitHub Pages. I want to cancel my website hosting and builder subscription, but I want to keep my domain name `dareanimalrescue.com` active."*
