# Adding content to the site

Run these from the site folder (the one with hugo.toml). Each command creates a new
file already filled in with the right format. Open it, write, save, then push.

    hugo new blog/my-post-title.md
    hugo new projects/my-project-name.md
    hugo new hobbies/my-hobby-name.md

The file name becomes the page URL and the default title (dashes become spaces).

Preview locally:   hugo server        then open http://localhost:1313
Publish:           git add .  &&  git commit -m "New post"  &&  git push

## Images
Put image files in static/images/, then:
- as a card/cover image, in the post's front matter:   image: 'images/photo.jpg'
- inside the text:                                     ![caption](/images/photo.jpg)

## Resume PDF
Put the PDF at static/files/resume.pdf and set  resumePDF = 'files/resume.pdf'  in hugo.toml.

## Other edits
- Home page intro text:      content/_index.md
- Resume text:               content/resume.md
- Contact links / email:     [params] section of hugo.toml
- Colors and fonts:          assets/css/main.css (the variables at the top)
- Delete a post:             delete its .md file and push

## Nav buttons (dragon balls)
The icons are static/images/nav/1.png ... 5.png, assigned per menu item in hugo.toml
(the `icon = ...` line under each [[menus.main]]). Swap files or numbers there.
