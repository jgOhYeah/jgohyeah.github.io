# jgohyeah.github.io
User Website.

Uses Jekyll to generate the static HTML components.

Go to [jgohyeah.github.io](jgohyeah.github.io) to see the page in a more easily readable format.

## Usage
GitHub pages is set to automatically deploy the main branch upon push. For local development, see [this guide](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll). In short:

1. Install Ruby and Jekyll.
2. `cd` to this folder.
3. Run `bundle3.2 exec jekyll serve`.
4. Access the page in a web browser at [`http://localhost:4000`](http://localhost:4000).

## Useful templates / includes
### Git repositories
<pre>
{%- include github-bookmark.html name="<b>REPO_NAME</b>" description="<b>REPO_DESC</b>" url="<b>REPO_URL</b>" thumbnail="<b>REPO_THUMNAIL_OPTIONAL</b>" -%}
</pre>

Where:
- `REPO_NAME` is the name of the repository.
- `REPO_DESC` is the description / subtitle.
- `REPO_URL` is the URL.
- `REPO_THUMBNAIL_OPTIONAL` is the URL (relative or absolute) of an image thumbnail. This doesn't need to be provided if there isn't a relevant thumbnail.

### Captioned images
<pre>
{%- include captioned-image.html src="<b>IMAGE_SRC</b>" alt="<b>IMAGE_ALT_TEXT</b>" caption="<b>IMAGE_CAPTION_OPTIONAL</b>" -%}
</pre>

Where:
- `IMAGE_SRC` is the relative or absolute URL of the image.
- `IMAGE_ALT_TEXT` is the alternate text for the image.
- `IMAGE_CAPTION_OPTIONAL` is the caption. If this isn't provided then the alternate text will be used as the caption instead.

### YouTube videos
- Use the *Share > Embed* menu to generate an `iframe`. Enable the *Privacy Enhance Mode* and copy the text.
- Paste in the page and delete the `width` and `height` attributes. Replace these with `class="embedded-4by3"` or `class="embedded-16by9"` depending on the aspect ratio.

### Other web pages
Use an `iframe` with the `webpage-iframe` class.
<pre>
&lt;iframe src="<b>URL</b>" class="webpage-iframe"&gt;&lt;/iframe&gt;
</pre>

### PDFs
<pre>
&lt;object data="<b>URL</b>" class="pdf-document" type="application/pdf"&gt;&lt;/object&gt;
</pre>