# Detox

Detox is a beautiful, modern [Ghost](http://www.ghost.org) theme.

#### → [See the demo](http://www.jrdnbwmn.com/blueberry/detox/lunch/)

## Features

* Fully responsive
* Minimal and focused on content
* Built with Sass (and the Sass files are included in the download in case you want to do some editing).
* [Moot](https://moot.it/) comments

## Installation

1. Download the files using the GitHub .zip download
2. Unzip the files and rename the folder to `Detox`
4. Copy the folder into your Ghost theme directory `ghost/content/themes`
5. Restart ghost and log in to your dashboard
6. In settings under themes select **Detox** and save

## Setting up comments

Detox comes with Moot comments installed, but YOU'LL NEED TO SET UP MOOT FOR YOUR OWN BLOG.

To set up Moot comments, do the following:

1. Go to: https://moot.it/ and create a new forum (near the bottom) and username for yourself.
2. Inside your new forum, create a discussion section that you'll use for comments (most people just name it "Posts").
3. Use a text editor to open the post.hbs file in this theme.
4. Find this code in that file:
	```
    <section id="comments">
        <a class="moot"
            title="{{title}}"
            href="https://moot.it/i/detox/posts:{{title}}">
            Comments for this blog entry
        </a>
    </section>
    ```
5. Replace "detox" with the name of the forum you created and "posts" with the name of the discussion section you created, like this:
	```
    href="https://moot.it/i/your-forumname/your-discusionsection:{{title}}"
    ```
Then you should be good to go!

For more information:
- [https://moot.it/docs/embedding.html](https://moot.it/docs/embedding.html)
- [https://ghost.org/forum/plugins/605-blog-comments-discus/?page=2](https://ghost.org/forum/plugins/605-blog-comments-discus/?page=2)

## Setting up highlight JS
Detox now uses [highlight JS](https://highlightjs.org/) to automatically style your code when posting.

To change the default theme (github-gist):

1. Download the latest release of highlight JS [here](https://github.com/isagalaev/highlight.js)
2. Go to the highlight theme [demo](https://highlightjs.org/static/demo/) and find the theme you wish to use.
3. Find the associated .css file with that theme -> `/src/styles/themeName.css`, then place it within `detox/assets/css`.
4. Edit default.hbs with the new .css file, normally found on line 31.
5. Enjoy!

## License
[MIT License](http://oswaldoacauan.mit-license.org/)
