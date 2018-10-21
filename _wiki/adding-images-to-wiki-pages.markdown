---
layout: post
title:  "How to add images to wiki pages"
category: Meta
---

## Adding images from external websites

This applies if your image is from an external website, such as Imgur or Chief Delphi.

1. Get the URL of the image. This can be done by right-clicking/two-finger-clicking on an image and clicking on "Copy image address".

1. Type the following into your wiki page, in the location that you want to insert the image

    {% highlight markdown %}
    !\[Description of image if image won't load]\(https://example.com/url/to/image/banana.png)
    {& endhighlight &}


## Adding your own images

This is mildly more complicated

1. Make sure that your image filenames are descriptive.

1. Remember your filename

1. Navigate to the `assets` folder from the repository's home page

1. Click the "Upload Files" button.
    ![Image of the button]({{ "/assets/upload-files-button-adding-images-instructions.png" | absolute_url}})

1. Upload your images

1. Commit your changes to finalize the upload

1. In the wiki page that you wish to add an image to, insert the following Markdown

    {% highlight markdown %}
    !\[Description]({{ "/assets/name_of_image.png" | absolute_url}})
    {% endhighlight %}
    
    Make sure to replace `name_of_image.png` with the filename of your image
