# commentOnProduct

This function must be called every time a visitor sends a product comment or review.

```js
_ra.commentOnProduct(product_id, callback_function);
```

### executing scripts automatically when the page is loaded

```js
var _ra = _ra || {};

_ra.commentOnProductInfo = {
	"product_id" : product_id
};

if (_ra.ready !== undefined) {
	_ra.commentOnProduct(_ra.commentOnProductInfo.product_id);
}
```
	
## commentOnProduct** function parameters

|    **Parameter**    |    **Type**    |    **Required**    |    **Description**    |
|---|---|---|---|
|  id  |  Number or text  |  Required  |  product id for which the comment is added.  |
|	callback_function	|	Function	|	Optional	|	With this parameter you can define a function that runs itself after the action’s parent function executes	|

## commentOnProduct function examples

#### sending event with callback function
	
```js
_ra.commentOnProduct(100, function() {
	console.log("the informations have been sent");
});
```
	
#### sending event with no callback function
	
```js
_ra.commentOnProduct(100);
```
