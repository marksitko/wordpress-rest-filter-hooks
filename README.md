# Execution order of some WordPress Rest filter hooks:

### 1. rest_pre_dispatch()
```php 
/**
 * @link https://developer.wordpress.org/reference/hooks/rest_pre_dispatch/
 */
function custom_callback_function( $result, $server, $request ) {
    return $result;
}
add_filter( 'rest_pre_dispatch', 'custom_callback_function', 10, 3);
```


### 2. rest_request_before_callbacks()
```php
/**
 * @link https://developer.wordpress.org/reference/hooks/rest_request_before_callbacks/
 */
function custom_callback_function( $response, $handler, $request ) {
    return $response;
}
add_filter( 'rest_request_before_callbacks', 'custom_callback_function', 10, 3);
```


### 3. rest_dispatch_request()
```php
/**
 * @link https://developer.wordpress.org/reference/hooks/rest_dispatch_request/
 */
function custom_callback_function( $dispatch_result, $request, $route, $handler ) {
    return $dispatch_result;
}
add_filter( 'rest_dispatch_request', 'custom_callback_function', 10, 4);
```


### 4. rest_request_after_callbacks()
```php
/**
 * @link https://developer.wordpress.org/reference/hooks/rest_request_after_callbacks/
 */
function custom_callback_function( $response, $handler, $request ) {
    return $response;
}
add_filter( 'rest_request_after_callbacks', 'custom_callback_function', 10, 3);
```


### 5. rest_post_dispatch()
```php
/**
 * @link https://developer.wordpress.org/reference/hooks/rest_post_dispatch/
 */
function custom_callback_function( $result, $server, $request ) {
    return $result;
}
add_filter( 'rest_post_dispatch', 'custom_callback_function', 10, 3);
```


### 6. rest_request_parameter_order()
```php
/**
 * @link https://developer.wordpress.org/reference/hooks/rest_request_parameter_order/
 */
function custom_callback_function( $order, $type, $request ) {
    return $order;
}
add_filter( 'rest_request_parameter_order', 'custom_callback_function', 10, 3);
```


### 7. rest_pre_serve_request()
```php
/**
 * @link https://developer.wordpress.org/reference/hooks/rest_pre_serve_request/
 */
function custom_callback_function( $served, $result, $request, $server ) {
    return $served;
}
add_filter( 'rest_pre_serve_request', 'custom_callback_function', 10, 4);
```

### 8. rest_pre_echo_response()
```php
/**
 * @link https://developer.wordpress.org/reference/hooks/rest_pre_echo_response/
 */
function custom_callback_function( $result, $server, $request ) {
    return $result;
}
add_filter( 'rest_pre_echo_response', 'custom_callback_function', 10, 3);
```