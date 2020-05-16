# Instalando
``` 
easy_install woocomerce
``` 
# Test
```  
from woocommerce import API
import pprint

wcapi = API(
    url="http://localhost", # Your store URL
    consumer_key="ck_cba815db58bc81faa7d630be9866b18edafacf3d", # Your consumer key
    consumer_secret="cs_e202df477f177c70a42825a48290f394c182126c", # Your consumer secret
    wp_api=True, # Enable the WP REST API integration
    version="wc/v3" # WooCommerce WP REST API version
)
pprint.pprint(wcapi.get("orders").json())
```  
