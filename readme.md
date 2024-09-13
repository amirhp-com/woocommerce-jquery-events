
# WooCommerce jQuery Events

WooCommerce provides a variety of useful jQuery events that allow you to trigger custom actions on your store. By leveraging these events, you can easily customize your store’s behavior and enhance the shopping experience.

## Table of Contents
- [Basic Usage](#basic-usage)
- [WooCommerce jQuery Events](#woocommerce-jquery-events)
  - [Cart and Checkout Events](#cart-and-checkout-events)
  - [Order Meta Box Events](#order-meta-box-events)
  - [Product Variation Meta Box Events](#product-variation-meta-box-events)
  - [Product Meta Box Events](#product-meta-box-events)
  - [Settings Events](#settings-events)
- [Sample Usage](#sample-usage)
- [Disclaimer](#disclaimer)

## Basic Usage

To use these events, you can listen for them using the following structure:

```javascript
$(document.body).on('woocommerce_event', function() {
    // Your custom function
});
```

Simply replace `'woocommerce_event'` with the desired event from the list below.

## WooCommerce jQuery Events

### Cart and Checkout Events

- `adding_to_cart`: Triggered after the quantity or add-to-cart button is clicked.
- `added_to_cart`: Triggered after a product is added or removed from the cart.
- `removed_from_cart`: Triggered after a product is removed from the cart.
- `update_checkout`: Triggered when the checkout page needs to be updated.
- `init_checkout`: Triggered after the user accesses the checkout page.
- `price_slider_updated`: Triggered after the WooCommerce price slider is updated.
- `wc_fragments_loaded`: Triggered after cart fragments (e.g., mini-cart) are loaded.
- `wc_fragment_refresh`: Triggered when the cart fragments need to be refreshed.
- `wc_fragments_refreshed`: Triggered after cart fragments have been refreshed.
- `wc_fragments_ajax_error`: Triggered after an error occurs while refreshing cart fragments.
- `wc_cart_button_updated`: Triggered after the cart button is updated.
- `cart_page_refreshed`: Triggered after the cart page is updated.
- `cart_totals_refreshed`: Triggered after the cart totals are refreshed.
- `updated_wc_div`: Triggered after various WooCommerce-related updates.

### Order Meta Box Events

- `quantity_changed`: Triggered when the quantity of the order item line changes.
- `order-totals-recalculate-before`: Triggered before sending Ajax request to recalculate totals.
- `order-totals-recalculate-success`: Triggered after the totals recalculate Ajax request succeeds.
- `order-totals-recalculate-complete`: Triggered after the recalculation request completes.
- `items_saved`: Triggered after clicking on "Save" and Ajax request is sent.
- `refund_quantity_changed`: Triggered when you change the quantity of a product to be refunded.

### Product Variation Meta Box Events

- `wc-enhanced-select-init`: Triggered when variations are loaded.
- `woocommerce_variations_loaded`: Triggered after loading variations via Ajax.
- `woocommerce_variations_saved`: Triggered after saving changes to variations via Ajax.
- `woocommerce_variations_save_variations_button`: Triggered after clicking the "Save changes" button.
- `woocommerce_variations_save_variations_on_submit`: Triggered after clicking the "Update" button.
- `woocommerce_variations_added`: Triggered after adding a variation.
- `woocommerce_variations_removed`: Triggered after removing a variation.
- `woocommerce_variations_input_changed`: Triggered after changing input fields of the variation.
- `woocommerce_variations_defaults_changed`: Triggered after changing the default form values.

### Product Meta Box Events

- `woocommerce-product-type-change`: Triggered when the product type is changed.
- `woocommerce_added_attribute`: Triggered after adding a product attribute.
- `reload`: Triggered after reloading the variations panel.

### Settings Events

- `updateMoveButtons`: Triggered after sorting payment or shipping methods.

## Sample Usage

Here’s a basic example of how to use WooCommerce jQuery events in your store:

```javascript
$(document.body).on('added_to_cart', function() {
    console.log('Product has been added to the cart!');
});
```

This code logs a message to the console when a product is added to the cart.

## Disclaimer

> [!IMPORTANT]
> Please note that not all of these events have been fully tested, and some may not work as expected. If you encounter any issues or have suggestions for improvements, feel free to contribute.

