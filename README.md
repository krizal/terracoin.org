# About #
terracoin.org website

now uses PieCrust cms to generate static files.
PieCrust will be a submodule of this git repos once git 1.8.2 is part of debian stable distributions, to get:
git submodule add -b the_submodule_branch [Git repo URL]
git submodule update --remote

for now, PieCrust's git-stable branch is simply cloned locally:
 git clone https://github.com/ludovicchabant/PieCrust.git piecrust
 cd piecrust
 git checkout git-stable


# website creation #

piecrust/bin/chef init terracoin


# generating static pages #

cd terracoin
../piecrust/bin/chef bake


# site parameters #

vi _content/config.yml


# page creation #

cd terracoin
../piecrust/bin/chef prepare page index

news, alerts and howto documents will consist of 'blog' posts using our simple blog post template.


# categories and tags #

piecrust 'categories' matches the site's sestions:
 * home
 * about
 * news
 * alert
 * howto

'tags' are used within the 'howto' category :
 * client
 * wallet
 * ...

note that first terracoin client alert page was not created as a blog post but as a page instead, to keep existing url.
Following alerts will be created as blog posts under category 'alert'

