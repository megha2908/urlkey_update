# Magento 2: Module that modifies the URL key of a product 
Module that modifies the URL key of a product created/updated only via REST API for including the SKU in the UrlKey, i.e. product-name-{sku}

In  webapi.xml file, I've defined our custom route URL for product update API is /rest/V1/products/updateProduct.
So our final URL will be called as {SITE_URL}/rest/V1/products/updateProduct
I've used updateProduct  method and defined updateProduct() method with update product logic in ProductUpdateManagement.php file.

Your request will look like below,

{
  "products": [
	 {
	      "name":"Test",
	      "sku":"test"  
	 },
	 {
	      "name":"Test2",
	      "sku":"test2"
	 }
    ]
}
