# chefdk-julia
An Opinionated Cookbook Creator

_with spunk and a grin, by Nordstrom_

 * home: https://git.nordstrom.net/projects/CHF/repos/chefdk-julia


## About
Julia is a special type of Chef cookbook that is designed to generate code
(cookbooks, templates, etc).

It is based upon the default code_generator cookbook introduced in ChefDK 0.9.0
(`chef generate generator`) and is meant to be a
simplified successor to chef-gen-flavors.

## Installation
For now, we're recommending grabbing the latest version from git:

    cd ~/chef/cookbooks
    git clone ssh://git@git.nordstrom.net/chf/chefdk-julia.git

Once you have the code locally, you need to configure `chef` to use Julia
instead of the built-in default generator by adding this to your
`~/.chef/config.rb` or `~/.chef/knife.rb` configuration file:

    chefdk.generator_cookbook "~/chef/cookbooks/chefdk-julia"

Adjust the `~/chef/cookbooks/chefdk-julia` path as needed if you put it somewhere
else. Be sure that the folder's name is 'chefdk-julia' so that it matches the
metadata.rb's name for the cookbook.

## Generating a cookbook
Once chefdk-julia is installed, you should be able to generate a cookbook with
the `chef` command:

    chef generate cookbook the_art_of_french_cooking

where `the_art_of_french_cooking` is the name of the cookbook you want to create.
