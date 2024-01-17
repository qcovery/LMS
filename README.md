# LMS
This module adds the option to create and manage semester reserves.

## Usage
Integrate the module in the `modules` directory of VuFind and activate it by adding `LMS` to `VUFIND_LOCAL_MODULES`.  
When adding the module manually make sure to copy and adapt the config file and copy/symlink the theme.  

Add the following lines to your `cart.phtml` template:
```php
<!-- Module LMS -->
<div style="float:right;">
    <?=$this->render('cart/cart-lms-export.phtml', []) ?>
</div>
<? if ($this->cart()->isLmsActive()): ?>
    <div style="display: inline-block;">
        <?=$this->transEsc('ELSE hint cart')?>
    </div>
<? endif; ?>
<!-- Module LMS -->
```
