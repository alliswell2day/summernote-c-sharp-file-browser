# Summernote C# File Browser

This plugin adds a simple file browser to the summernote editor from https://summernote.org/

This asp.net C# file browser allows you to browse a folder on your website (set as /docs/ as default) and will insert an image in your page for .jpg, .png, .gif and .svg files or will create a link for other file types.

Requires Bootstrap 4

Requires Font Awesome

## Installation

To install copy "filebrowser" folder to your summernote plugin directory. 

Copy images from /images to /images on your website.

Edit filebrowser.aspx to style sheet locations
```
<link rel="stylesheet" href="/css/bootstrap.min.css" />
<link rel="stylesheet" href="/css/font-awesome.min.css">
<link rel="stylesheet" href="/css/fa-regular.min.css">
```

Edit iframe path on line 58 in summernote-ext-browser.js to the location of filebrowser.aspx if summernote folder not in site root.

To add to your summernote editor you need to include the plugin javascript:
```
<script src="/summernote/plugin/filebrowser/summernote-ext-browser.js"></script>
```
Add the filebrowser icon/button to your editor using 'filebrowser'

Below is an example of the editor config which includes the new button.
```
$(document).ready(function () {
            $('#summernote').summernote({
                height: 500,
                toolbar: [
                    ['style', ['style']],
                    ['style', ['bold', 'italic', 'underline', 'clear']],
                    ['font', ['strikethrough', 'superscript', 'subscript']],
                    ['color', ['color']],
                    ['insert', ['picture', 'link', 'video', 'table','filebrowser', 'hr']],
                    ['para', ['ul', 'ol', 'paragraph']],
                    ['undo', ['undo', 'redo']],
                    ['codeview', ['codeview']],
                ]
            });
        });
```
## In Use

You can view a demo video of this file browser in use

[![](http://img.youtube.com/vi/ktV_6uy4zEw/0.jpg)](http://www.youtube.com/watch?v=ktV_6uy4zEw "Video demo")