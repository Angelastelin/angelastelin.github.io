**angelastelin.github.io**

A website for Angela Stelin to showcase her art.

There are two versions of the site:
- English: index.html
- Portuguese: port.html

You can switch between them using the language button on the site.



**Updating the Gallery (English Version)**

All images used in the English gallery live inside the images/ folder.
Each artwork has two files:
- A thumbnail (small preview) → shown in the gallery grid
- A full-size image → opened when someone clicks on the artwork

Both must be placed in the correct folders.

1. Uploading a Thumbnail
- Resize the image to 687px × 432px.
- Upload it to: images/thumbs/
- Name it consistently with the other images already in that folder: Thumb Algarve


2. Uploading the Full-Size Image
- Upload the full-resolution version to: images/fulls/
- Use the exact same filename as the thumbnail.
- Name it consistently with the other images already in that folder: Algarve

Deleting a File (e.g., wrong upload)

- If you’ve uploaded the wrong image:
- Click on the file in GitHub.
- On the top right, click the three-dot menu (⋮).
- Scroll to the bottom and choose Delete file.
- Commit your changes.
  
<br>

**Adding the Images to the English Gallery (index.html)**

Once the new thumbnail and full-size images are uploaded, the next step is to “register” them inside the index.html file so they appear on the page.

1. Finding the Image Path

- Inside the GitHub file browser, click on your newly uploaded image.
- At the top of the page, GitHub shows the exact path to the file (for example:images/thumbs/Thumb_NewArtwork.png).
- You can copy this path directly, then paste it into the code so you don’t need to type it manually.

2. Open index.html
   
Inside this file, each artwork is represented by a small block of HTML code.
These blocks also control:
- which image to display
- where the full-size image is located
- the caption that appears on hover
- the spacing on desktop and mobile (6u 12u(mobile))

You do not need to change any spacing classes unless you want to change the layout.

3. Adding a Row of Two Images
- If you want to add two artworks side-by-side, copy and paste the following block under the last existing row:

```html
<br>
<div class="row 20% images">
    <div class="6u 12u(mobile)">
        <a href="images/fulls/Ondas Lunares.jpeg" class="image fit from-left">
            <img src="images/thumbs/Thumb Ondas Lunares.png" title="Ondas Lunares, acrylic on canvas - 2025, 70 x 100 cm" alt=""/>
        </a>
    </div>
    <div class="6u 12u(mobile)">
        <a href="images/fulls/Flash.jpeg" class="image fit from-right">
            <img src="images/thumbs/Thumb Flash.png" title="Flash, acrylic on canvas - 2025, 80 x 120 cm" alt=""/>
        </a>
    </div>
</div>
```

Then update the following in both halves of the row:
- the full image path (images/fulls/...)
- the thumbnail path (images/thumbs/...)
- the title text inside the title="" attribute (this is your caption)

Everything else can stay the same.

4. Adding a Row with One Image Only
If you prefer a single artwork centred on the row, use this alternative block:
```html
<!-- This is the code if the row just has one single image -->
<br>
<div class="row 20% images">
    <div class="6u -3u 12u(mobile)">
        <a href="images/fulls/Genesis II.jpeg" class="image fit from-bottom">
            <img src="images/thumbs/Thumb Genesis II.png" title="Genesis II, acrylic on canvas - 2023, 120 x 80cm" alt=""/>
        </a>
    </div>
</div>
```

Again, update:
- images/fulls/...
- images/thumbs/...
- the title="" caption

Note: The spacing class 6u -3u is what centres the image on desktop.

5. Save and Refresh
After pasting and editing:
- Click Commit changes on the top right
- Allow GitHub to run its checks
- Refresh the browser
- Your new artworks should appear immediately

If nothing shows up, check:
- filename spelling
- file extension (.jpeg, .jpg, .png)
- that both the thumbnail and full-size image exist in the correct folders


**Updating the Portuguese Version**

The Portuguese version of the website lives inside the port/ folder.
Everything you need for that page — the HTML file and the images — is located inside this folder.

1. Where to find the Portuguese files

From the repository’s main page:
Click on the folder named port
Inside it, you will see:
- port.html (the Portuguese page)
- An images folder containing:
- thumbs/ — thumbnails
- fulls/ — full-size images

2. Uploading Portuguese gallery images
The steps are similar to the English version but take place inside the port/ directory.

Upload the Thumbnail
- Make sure to resize the image to 687px × 432px.
- Upload it to: port/images/thumbs/
- Use the same naming format as your other thumbnails.

Upload the Full-Size Image
- Upload the full-resolution version to: port/images/fulls/
- Use the exact same filename as the thumbnail.

3. Getting the correct file path

To avoid mistakes, after uploading an image you can click on that file and copy the file path shown at the top of the page.
This ensures your ``` <img src="...">``` and ``` <a href="...">``` paths are 100% correct.

4. Updating port.html
Once the images are uploaded:
- Open port/port.html
- Scroll to the gallery section
- Copy the appropriate code block (either the 2-image row or the 1-image row)
- Replace the href="..." and src="..." file paths with your new image filenames
- Update the title="..." text if you want to change or add the caption

Note: The code blocks must be wrapped in triple backticks in the README to avoid being rendered as images.

5. Saving Your Changes
When finished:
- Click Commit changes
- Allow GitHub to run its checks
- Refresh the live website after a few seconds — the updated images should appear.

If anything doesn’t look right, or you’re unsure where something is located, feel free to contact me anytime.
