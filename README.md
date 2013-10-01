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


# piecrust setup #

piecrust/bin/chef init terracoin
cd terracoin
../piecrust/bin/chef bake

# site parameters #

vi _content/config.yml

# page creation #

cd terracoin
../piecrust/bin/chef prepare page index

