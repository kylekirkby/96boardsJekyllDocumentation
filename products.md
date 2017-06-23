# 96boards Products

96boards products are now stored in the Jekyll collection `_product`. The content of this file is the markdown displayed on the product page on the website. The permalink however relates to an entry in the database  - `_data/product_db.yml` which then contains multiple variables which describe each product uniquely and is then output through liquid in site pages.

## Adding a product to the site.

### Create new folder for product
In order to add a new product to the site first you must navigate to the `_product` Jekyll collection which is located in the root of the site. In this folder there are a few specification sub folders that you should be aware of.

* CE
* EE
* IE
* Mezzanine
* Accessories

These are where you will add your new product folder. Depending on the product you are adding navigate to the correct specification folder. Once inside create your new product folder along with an images sub folder and README.md

* \_product/
    * CE/
        * New96board/
            * images/
                * newboardimage.png
            * README.md

### Add the required front matter variables <a name="product-front-matter"></a>
Jekyll uses front matter, which is yaml structured data that sits at the front of Jekyll files. This describes the page in question through permalinks, titles and layouts etc. Below is a table of the required front matter for products.

|    Front Matter Variable    |                Meaning and usage                           |
|-----------------------------|:----------------------------------------------------------:|
| title                       | This is used for the `<title>` of the website. This is also used in _includes as a reference for the page title.               |
| layout                      | This is the layout that Jekyll will use when building the product page. The layout to use is product-display-page (this may later be ommitted by the developers for simplicity)                |
| permalink                   | This is path that the page will reside on when Jekyll builds the site. Changing this changes where the page will be when generated and deployed. The current convention is `/product/ProductName/` |
| description                 | This is the description of the page used in the meta description tag |



```
---
title: Bubblegum-96
layout: product-display-page
permalink: /product/bubblegum-96/
description: |-
    Bubblegum-96 Board based on Actions Semi S900 Processor
---
```

This is an example of the front matter used in the BubbleGum 96 board page.
