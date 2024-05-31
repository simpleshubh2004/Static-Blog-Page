This project is a simple HTML and CSS page for displaying a collection of blog posts with a clean and responsive design. Each blog post is represented as a card containing an image, title, description, author information, and tags.

Table of Contents
Features
File Structure
Usage
Customization
Credits
Features
Responsive design
Hover effects for images and titles
Author information with avatars generated using DiceBear
Categorized blog posts
File Structure
my-blogs/
├── index.html
├── index.css
├── blog1.avif
├── blog2.avif
├── blog3.avif
├── blog4.avif
├── blog5.avif
├── blog6.avif
├── blog7.avif
├── blog8.avif
└── README.md
index.html: The main HTML file containing the structure of the blog page.
index.css: The CSS file for styling the blog page.
blogX.avif: Placeholder images for the blog posts.
Usage
To view the blog page, simply open the index.html file in a web browser. Ensure all linked images (blogX.avif) and the CSS file (index.css) are in the same directory.

Customization
Changing Blog Content
To change the blog content, modify the HTML within each card_container div:

<div class="card_container">
    <a href="#" class="card_image_container">
        <img
        src="your-image-source.avif"
        alt="your image description"
        class="card_image"
        loading="lazy"
        />
    </a>
    <div class="card_title_container">
        <a href="#" class="card_title_anchor">
            <h2 class="card_title">Your Blog Title</h2>
        </a>
        <p class="card_desc">Your blog description goes here.</p>
    </div>
    <div class="card_footer_container">
        <div class="author_container">
            <div class="author_avatar_container">
                <img
                src="your-avatar-url"
                loading="lazy"
                class="author_avatar"
                alt="author avatar"
                />
            </div>
            <div class="author_info_container">
                <span id="id1">Author Name</span>
                <span id="id2">Publish Date</span>
            </div>
        </div>
        <div class="card_tag_container">
            <span>Your Tag</span>
        </div>
    </div>
</div>
Updating Author Avatars
Author avatars are generated using DiceBear. You can customize the avatar by changing the URL in the src attribute of the img tag within author_avatar_container:
<img
src="https://api.dicebear.com/8.x/notionists/svg?seed=YourSeed&size=64"
loading="lazy"
class="author_avatar"
alt="avatar"
Replace YourSeed with any string to generate different avatars.

Modifying CSS
The CSS file (index.css) is used to style the HTML page. Below is a summary of the CSS classes and their purposes:
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}
a {
    text-decoration: none;
}
body {
    width: 100%;
    height: 100%;
}
.container {
    max-width: 90vw;
    padding: 2rem 1rem;
    margin: 0 auto;
}
.header_container {
    margin-bottom: 2.8rem;
}
.header_title {
    margin-bottom: 1.2rem;
    font-size: 1.8rem;
    line-height: 2rem;
    font-weight: 700;
    text-align: center;
}
.header_desc {
    max-width: 568px;
    text-align: center;
    color: rgb(82, 79, 79);
    margin: 0 auto;
}
.main_container {
    display: grid;
    gap: 1.5rem;
    grid-template-columns: repeat(4, 1fr);
}
.card_container {
    display: flex;
    overflow: hidden;
    flex-direction: column;
    border: 1px solid rgb(111, 109, 109);
    border-radius: 7px;
}
.card_image_container {
    position: relative;
    overflow: hidden;
    height: 17rem;
}
.card_image {
    object-fit: cover;
    object-position: center;
    position: absolute;
    height: 100%;
    width: 100%;
}
.card_title_container {
    display: flex;
    flex-direction: column;
    padding: 1.55rem;
}
.card_container:hover .card_image {
    transform: scale(1.06);
    transition-duration: 500ms;
}
.card_title {
    font-size: 1.1rem;
    font-weight: 725;
    color: rgb(58, 53, 53);
    line-height: 1.5rem;
    margin-bottom: 0.3rem;
}
.card_title_anchor:hover .card_title {
    color: coral;
}
.card_desc {
    color: rgb(96, 89, 89);
    font-size: 1rem;
}
.card_footer_container {
    display: flex;
    justify-content: space-between;
    padding: 1.5rem;
}
.author_container {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 1.5rem;
}
.author_avatar_container {
    height: 2rem;
    width: 2rem;
    overflow: hidden;
    border: 1px solid rgb(121, 101, 101);
    border-radius: 50%;
    background-color: rgb(243, 241, 241);
}
.author_info_container {
    display: flex;
    flex-direction: column;
}
#id1 {
    color: tan;
}
#id2 {
    color: rgb(120, 114, 114);
}
.card_tag_container {
    font-size: 0.9rem;
    border: 1px solid rgb(131, 128, 128);
    border-radius: 3px;
    line-height: 1rem;
    padding: 0.25rem 0.4rem;
    color: grey;
}
You can customize the styles by modifying the CSS classes to fit your design preferences.

Credits
Avatar images are generated using DiceBear Avatars.
Placeholder images are in .avif format for better performance and quality.
Feel free to modify the content and style as per your needs. Contributions and suggestions are welcome!

