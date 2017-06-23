# 96boards Products

96boards products are now stored in the Jekyll collection `\_product`. The content of this file is the markdown displayed on the product page on the website. The permalink however relates to an entry in the database  - `_data/product_db.yml` which then contains multiple variables which describe each product uniquely and is then output through liquid in site pages.

## Adding a product to the site.

### Create new folder for product
In order to add a new product to the site first you must navigate to the `\_product` Jekyll collection which is located in the root of the site. In this folder there are a few specification sub folders that you should be aware of.

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
