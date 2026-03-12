# Contributing

## Adding a Missing Product

For currently missing products, check out the list of [open issues with the label 'missing product'](https://github.com/matelab-ch/matelab/issues?q=state%3Aopen%20label%3A%22missing%20product%22). To add a new product:

+ Copy the template from `templates/product.yml` into `data`. 
	+ Give it a name in the format of `<brand>_<product>.yml`. 
	+ If you are adding a product in different packaging, name it `<brand>_<product>_<packaging>.yml`.
+ Edit the file and submit your changes via a pull request.
	+ Please also send your source (URL, picture of beverage) for me to verify the data.

## Adding Missing Data to a Product

For currently missing data, check out the list of [open issues with the label 'missing data'](https://github.com/matelab-ch/matelab/issues?q=state%3Aopen%20label%3A%22missing%20data%22). To change existing data:

+ Find the product under `data`. 
+ Edit the file and submit your changes via a pull request.
	+ If with you changes, the file now has all required fields, set `draft` to `false`.
	+ Please also send your source (URL, picture of beverage) for me to verify the data.

## Adding a Store to a Product

+ Find the product under `data`. 
+ Edit the file and submit your changes via a pull request.
	+ For store URLs, make sure to remove any tracking and/or referral identifiers.
	+ Please also send your source (URL, picture of beverage) for me to verify the data.

## Removing/Discontinuing a Product

+ Since this data should be a sort of archive, products should not get fully deleted
+ If a product is no longer available, find the product under `data`. 
+ Edit the file and submit your changes via a pull request.
	+ Set `discontinued` to `true` but **do not remove store links**.
	+ Please also send your source (URL, picture of beverage) for me to verify the data.

## Local Dev Setup

Use this if you want to preview the site locally.

```sh
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

python3 build.py

python3 -m http.server -d output 8081
```
