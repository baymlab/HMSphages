# HMSphages
Online manual for the 2025 Summer Phage Discovery Program at Harvard Medical School

# [http://phages.hms.harvard.edu](http://phages.hms.harvard.edu)

## To edit this site

You can check out Natalia's original setup of the site on [her blog](https://nataquinones.github.io/blog/2021/06/20/thiswebsite.html).

1. **Git clone this repository.**
2. **Get Jekyll set up on your machine:**
    - Follow [these instructions](https://jekyllrb.com/docs/installation/macos/).
    - After running `gem install jekyll`, also install the bundler and the theme:
      ```sh
      gem install bundler just-the-docs
      ```  
3. On your local computer, open the `docs/_config.yml` file. Under **# JEKYLL STUFF**, you should see one line beginning with `remote_theme` and one line beginning with `#theme`
    - Delete the `#` before `#theme` and add a `#` before `remote_theme`.
   This change allows local rendering of the website with the **Just the Docs** theme. **Do not commit this change to GitHub!**
4. From the `docs` directory, run:
      ```sh
      jekyll serve
      ```
    - The last few lines of the output should be something like:
      ```
      Server address: http://127.0.0.1:4000
      Server running... press ctrl-c to stop.
      ```
      Copy the URL (in this case, http://127.0.0.1:4000) into your browser to see the site.

Once you are happy with your local changes, you can git commit your changes, and then push. The site will automatically deploy using a github action.
