SAV Group Website
=================

Our group website is powered by [Jekyll]() and was gratefully adapted from the [UW-Sampa](https://github.com/uwsampa/research-group-web) group template.

This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License][license].

[license]: https://creativecommons.org/licenses/by-nc/4.0/


Setup
-----

To build/test the site locally, you'll need to install the prerequisites at:

https://jekyllrb.com/docs/


Updating Site Content
---------------------

GitHub Pages will automatically build the projects and posts from the templates. You only need to commit/push the templates, NOT the built pages.

For adding/updating group members, go to ./_data/people.yml. Do NOT change the unique identifiers (e.g. 'prof-sunjun'), even if the role changes, as this may accidentally break project pages.

For adding/updating projects, create/modify the .md files in ./_projects. Note the 'active' flag, which determines whether a project is current and appears on the front page or not.

For adding news posts, create a file ./_posts/YYYY-MM-DD-title-of-news-post.md. Follow the template of existing posts. Note that our Twitter account will automatically tweet a link to any newly created news posts, so please test locally first.

Supplementary materials (e.g. self-contained mini-sites) should be placed in ./supplementary-material. Follow the template of existing pages to automatically generate the standard layout.

Building/Testing Locally
------------------------

First, clone this repository on your local machine.

In the root directory, use this:

    bundle exec jekyll serve

Then access/test the site locally at: http://localhost:4000

Please do test all changes locally before deploying.

Updating Publication List
-------------------------

Unfortunately, the HTML of our publication list must be built offline.

To do this, update the BibTeX file in ./bibs/pubs.bib. Then, in the root directory, run:

     bundle exec make

This will transform the BibTeX into HTML. Simply commit/push the updated file after running the above.

(Note that Chris will do this automatically whenever a new paper appears on Sun Jun's / mine DBLP page.)

Help
----

Contact cposkitt@smu.edu.sg if you face any issues, or want access to the repository / organisation account.