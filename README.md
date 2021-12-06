composer require osiset/laravel-shopify

php artisan vendor:publish --tag=shopify-config

add in UserModel:
use Osiset\ShopifyApp\Contracts\ShopModel as IShopModel;
use Osiset\ShopifyApp\Traits\ShopModel;
class User extends Authenticatable implements IShopModel
use ShopModel;


For more info:
https://github.com/osiset/laravel-shopify/wiki/Installation

NGROK:
ngrok http http://laravel-shopify-osiset.local
