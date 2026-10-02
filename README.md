# Excellence Training Center (ETC) Website

A simple website made of ordinary files. It needs no server, database or special software.

## 1. How to open the website
Open the folder and double-click **index.html**. It opens in your browser. Pages link to each other, so you can click around. (Fonts load from the internet; without internet the site still works with standard fonts.)

## 2. Where the images are
All pictures are in the **images** folder. They are WebP files (small and fast). The logo is `images/logo.png`.

**Important:** the pictures supplied with this project are *illustrations*, not photographs of ETC. Replace them with real ETC photos when you have them (see next section).

## 3. How to replace an image
1. Prepare your photo (landscape, about 1200 pixels wide is ideal). Convert to WebP for speed (for example with squoosh.app) or keep it as JPG/PNG.
2. Give it **exactly the same file name** as the image you want to replace (for example `classroom-1.webp`) and put it in the `images` folder, replacing the old one.
3. If your photo has a different file type (for example `.jpg`), open the HTML pages in Notepad and change the file name there (use Find & Replace).

Teacher photos are `teacher-1.webp` to `teacher-6.webp` (in the order shown on the Teachers page).

## 4. How to change the logo
Replace `images/logo.png` with your logo (a wide PNG, about 760 x 200 px, transparent background). The small browser icon is `images/favicon.png`.

## 5. How to change text
Open any `.html` file with Notepad (or VS Code). Find the text you want and edit it. Do not delete the `<` `>` symbols around it. Save the file and refresh the page.

## 6. How to change phone numbers or the WhatsApp number
- **Phone numbers and address** appear in the HTML files. Use *Find & Replace in all files* (VS Code: Ctrl+Shift+H) to replace an old number with a new one.
- **WhatsApp number:** the number format is international without `+` or `00`. ETC's is `249915749548`. Replace `249915749548` in all files, and change it at the top of `js/script.js` (`whatsapp: '249915749548'`).

## 7. How the WhatsApp registration works
The registration form has no server. When a student presses **Register via WhatsApp**:
1. The form is checked (name, phone and program are required).
2. The website writes a neat message with all the details.
3. WhatsApp opens (the app on phones, WhatsApp Web on computers) with the message already typed to ETC's number.
4. The student presses **Send**. ETC receives it as a normal WhatsApp message.

The website does not store anything. The "Have a question?" form works the same way. All "Ask on WhatsApp" buttons open WhatsApp with a ready message, and they work even if JavaScript is off.

Message wording lives in `js/script.js` (the `T = { ... }` list) and is also written into the buttons in the HTML.

## 8. How to add a new program
1. Copy an existing program page, for example `ielts.html`, and rename it (for example `new-program.html`).
2. Edit the title, text and image names inside it.
3. Add it to the programs list in `programs.html` (copy one `<article class="pcard">...</article>` block), and add a link in the footer of the pages.
4. Add the new option to the Program dropdown in `registration.html`.
5. Add the page to `sitemap.xml`.

## 9. How to publish on GitHub Pages
1. Create a free account at github.com and click **New repository** (name it, for example, `etc-website`, set to Public).
2. Click **uploading an existing file** and drag in **everything inside this folder** (index.html, css, js, images, etc.), then **Commit changes**.
3. Go to **Settings > Pages**. Under *Branch* choose `main` and folder `/ (root)`. Save.
4. After about a minute your site is live at `https://YOUR-USERNAME.github.io/etc-website/`.

**To update later:** open the repository, click **Add file > Upload files**, drop in the changed files (same names), and commit.

**After publishing:** open `sitemap.xml` and `robots.txt` and replace `YOUR-USERNAME` and `YOUR-REPOSITORY` with your real GitHub address.

## 10. Directions button
The **Get directions** button opens a Google Maps search for Deim Madina, Port Sudan. When you have the exact Google Maps link for ETC, replace the `https://www.google.com/maps/search/...` link in `contact.html` with it.

## 11. Things this site deliberately does not include
No prices, schedules, exam-score promises, teacher qualifications, accreditation claims or social-media links, because none were provided. Add them yourself when ready.
