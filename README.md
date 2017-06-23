# 96boards Jekyll Documentation
The 96boards website is built using Jekyll, a static website generator based on Ruby, which allows the site to be more responsive and increase the performance of the site.

# Jekyll Deployment.
Jekyll uses Ruby to generate the static website so having Ruby installed is a must if you are
trying to build the 96boards site. Before you build the site use the following steps to make sure your environment is setup for a Jekyll build.

## \_config.yml
This file holds the configuration settings for the Jekyll website such as site source folder path and the site destination path.
|    Config Option    |                        Meaning and usage                           |
|---------------------|:------------------------------------------------------------------:|
| destination         | This is the folder the site will be compiled to.                   |
| permalink           | This is the permalink for blog posts on the site.                  |
| title               | This is the title of the website for use in the head.html include. |
| encoding            | This is simply the encoding jekyll uses when building site pages.  |
| description         | The description of the website for use in the meta description etc.|
| safe                | This is the site wide kill switch of safe mode on a Jekyll website.|
| search-label        | This is the search label used in the search.linar.org params.      |
| disqus              | This is a boolean value declaring whether disqus is enabled.       |
| disqus_shortname    | This is the shortname that disqus uses to show comments.           |
| url                 | If you are wanting to deploy the site to somewhere otherthan localhost then change this variable to the FQDN of where you are deploying to e.g https://www.96boards.org - note there is no trailing slash here.         |
| title               | |
| title               | |
| title               | |
| title               | |
| title               | |


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

## Dependencies
### 1. Ruby
`$ ruby -v`

This will show you the current version of Ruby that you have installed on your machine. We are using the ruby version 2.4.0 (ruby 2.4.0p0 (2016-12-24 revision 57164) [x86_64-darwin16]). This version may well change in the future development of this site but you can always find the version being currently used in the [Gemfile](https://stash.git.linaro.org/projects/MAR/repos/96boards.org-static/browse/Gemfile)

#### Install
To install ruby use your favourite package manager on your host OS or follow the instructions on [Ruby-Lang.org](https://www.ruby-lang.org/en/documentation/installation/)

### 2. Jekyll
`$ jekyll -v`

This command, once executed, will display the current version of Jekyll you have installed. We are using `jekyll 3.4.3` but this may change in the future so it may be useful to note that you can find the current version actively being used in the [Gemfile](https://stash.git.linaro.org/projects/MAR/repos/96boards.org-static/browse/Gemfile) under `gem "jekyll", "3.4.3"`.

#### Install
To install Jekyll [Ruby-Lang.org](https://www.ruby-lang.org/en/documentation/installation/)


# Resources
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
To add a product you must
