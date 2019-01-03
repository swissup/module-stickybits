# Stickybits

**This repo is just an integration of original library into Magento 2.**

> Stickybits is a lightweight alternative to position: sticky polyfills. It
> works perfectly for things like sticky headers.

See original repository for more information: https://github.com/dollarshaveclub/stickybits

### Installation

```bash
cd <magento_root>
composer require swissup/module-stickybits
bin/magento module:enable Swissup_Stickybits
bin/magento setup:upgrade
```

### Usage

Basic example:

```js
require(['stickybits'], function (stickybits) {
    stickybits('.sidebar');
});
```

> See all examples at official site: https://github.com/dollarshaveclub/stickybits#basic-usage

Advanced example (works for dynamically added elements):

```js
require([
    'Magento_Ui/js/lib/view/utils/async',
    'stickybits'
], function ($, stickybits) {
    $.async('.sidebar', function (el) {
        stickybits(el, {
            useStickyClasses: true,
            stuckClass: 'is_stuck'
        });
    });
});
```
