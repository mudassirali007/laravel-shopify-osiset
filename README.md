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
To point ngrok to a local url:
1. ngrok authtoken <YOUR_AUTHTOKEN> e.g <token> (located in c:/users/<user>/.ngrok2/ngrok.yml) 
2. ngrok http -host-header=rewrite laravel-shopify-osiset.local:80
ngrok http http://laravel-shopify-osiset.local
OR
ngrok http localhost

.env:
paste shopify app keys
SHOPIFY_API_KEY=
SHOPIFY_API_SECRET=