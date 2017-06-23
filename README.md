# 96boards Jekyll Documentation
The 96boards website is built using Jekyll, a static website generator based on Ruby, which allows the site to be more responsive and increase the performance of the site.
# Table of Contents
1. [Jekyll Deployment](Jekyll-Deployment)
    1. [\_config.yml setup](##\_config.yml-setup)
    2. [96 boards Dependencies](##96boards dependencies)
    3. [Jekyll Dependencies](##Jekyll Dependencies)
        1. [Ruby](### 1. Ruby)
            1. [Install Ruby](#### Install Ruby)
        2. [Jekyll](### 2. Jekyll)
            1. [Install Jekyll](#### Install Jekyll)
    4. [Jekyll Commands](## Jekyll Commands)
2. [Jekyll Assets](# Jekyll Assets)
3. [Website Content](# Website Content)

# Jekyll-Deployment
Jekyll uses Ruby to generate the static website so having Ruby installed is a must if you are
trying to build the 96boards site. Before you build the site use the following steps to make sure your environment is setup for a Jekyll build.

## \_config.yml-setup
This file holds the configuration settings for the Jekyll website such as site source folder path and the site destination path. You can find the Jekyll official documentation of configuration [here](https://jekyllrb.com/docs/configuration/).  

|    Config Option    |                        Meaning and usage                           |
|---------------------|:------------------------------------------------------------------:|
| destination         | This is the folder the site will be compiled to.                   |
| permalink           | This is the permalink for blog posts on the site.                  |
| title               | This is the title of the website for use in the head.html include. |
| encoding            | This is simply the encoding jekyll uses when building site pages.  |
| description         | The description of the website for use in the meta description etc. Also disables custom plugins and ignores symbolic links.|
| safe                | This is the site wide kill switch of safe mode on a Jekyll website.|
| search-label        | This is the search label used in the search.linar.org params.      |
| disqus              | This is a boolean value declaring whether disqus is enabled.       |
| disqus_shortname    | This is the shortname that disqus uses to show comments.           |
| url                 | If you are wanting to deploy the site to somewhere otherthan localhost then change this variable to the FQDN of where you are deploying to e.g https://www.96boards.org - note there is no trailing slash here.         |
| exclude             | These are files that are excluded from the build of Jekyll. You can use this if you want to speed up the site generation. For example, if you are only editing the _documentation section of the website simply exclude the other content folders and build with just the _documentation content. |
| google-tag-manager  | This is a site variable which controls the output of Google Tag Manager for use in the China site build which does not allow gtm to be used. |
| social              | This is a site variable that is required by [Jekyll SEO Tag Manager](https://github.com/jekyll/jekyll-seo-tag) which is optional but allows you to output more relevant social media meta tags. |
| twitter             | This is also used by the [Jekyll SEO Tag Manager](https://github.com/jekyll/jekyll-seo-tag)|
| github_username, linkedin_username, google_plus_username, facebook_username, youtube_username and twitter_username | These are used for the footer social media links. |

## 96boards dependencies

1. Ruby Gems listed in Gemfile and \_config.yml

The 96boards Jekyll based website has a few Gems that need to be installed before you can run the Jekyll site locally. In order to install these gems use `$ bundle install` which will install the gems listed in the Gemfile and the \_config.yml file. If you do not have `bundle` installed then download it using `$ gem install bundler`.

## Jekyll Dependencies

Jekyll list the dependencies over at their official installation documentation [here](https://jekyllrb.com/docs/installation/) but in general to run a Jekyll site you need:

* Ruby
* jekyll (Ruby Gem) e.g `$ gem install jekyll`
* bundler (Ruby Gem) e.g `$ gem install bundler`
* GNU/Linux, Unix, or macOS machine

### 1. Ruby
`$ ruby -v`

This will show you the current version of Ruby that you have installed on your machine. The version we are using may well change in the future development of this site but you can always find the latest version being currently used in the [Gemfile](https://stash.git.linaro.org/projects/MAR/repos/96boards.org-static/browse/Gemfile)

#### Install Ruby
To install ruby use your favourite package manager on your host OS or follow the instructions on [Ruby-Lang.org](https://www.ruby-lang.org/en/documentation/installation/)

### 2. Jekyll
`$ jekyll -v`

This command, once executed, will display the current version of Jekyll you have installed. We are using `jekyll 3.4.3` but this may change in the future so it may be useful to note that you can find the current version actively being used in the [Gemfile](https://stash.git.linaro.org/projects/MAR/repos/96boards.org-static/browse/Gemfile) under `gem "jekyll", "3.4.3"`.

#### Install Jekyll
To install Jekyll [Ruby-Lang.org](https://www.ruby-lang.org/en/documentation/installation/)


## Jekyll Commands
1. `$ jekyll serve`
    Enter this command into your terminal to build the site locally and test on a localhost server. `http://localhost:4000` is the location where the Jekyll site will deploy to if it is set in the url and fullpath front matter variables. All errors in requesting images will result in a message being displayed on the terminal window that is running the server.
2. `$ jekyll build`
    * This is the Jekyll command which builds the site ready for deployment and outputs the generated static Jekyll website to the deploy folder path set in the config.yml file e.g. `\_deploy` default destination for a Jekyll site is `\_site`.
3. `$ jekyll build -V`
    * This command is just the same as `$ jekyll build` but you can see a more Verbose approach to how the site is being generated in the build.
4. `$ jekyll serve -V`
    * This command is just the same as `$ jekyll serve` but you can see a more Verbose approach to how the site is being generated.
5. `$ jekyll build --config _config.yml`
    * This is and optional command that may come in useful when changing the configuration of the Jekyll site. This just allows any other config.yml files to be easily swapped in.



# Jekyll Assets
The resources included are as follows:
1. CSS (SASS)
2. Javascript
3. Images

# Website Content
The following fall under website content:
1. Products /products/
2. Projects /projects/
3. Blog Posts /blog/
4. About /about/
5. Compliance /compliance/
6. Specifications /specifications/

## Products
To add a product please visit [this page](products.md)
