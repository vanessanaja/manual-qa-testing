# SauceDemo Cart Exploratory Testing

## Test Area

Shopping cart functionality.

## Test Goal

Explore the add-to-cart and cart navigation flow and identify unexpected behavior.

## Environment

- Application: SauceDemo
- Browser: Google Chrome 153
- Operating System: Windows 11
- Date Tested: September 16, 2026

## Exploratory Notes

### Add Product to Cart

- Opened a jacket product.
- Changed the size to Medium.
- Added the product to the cart.
- Cart badge updated to `1`.
- An indefinite loading spinner appeared after the item was added.

### Cart Navigation Behavior

- Clicking **My Cart** caused the spinner to disappear, but the cart did not open.
- Clicking **My Cart** again caused the spinner to appear again.
- Refreshing the page caused the spinner to disappear.
- Cart badge remained at `1`.
- Clicking **My Cart** after the refresh successfully opened the cart.

## Session Result

The add-to-cart action successfully updated the cart badge, but the application entered an unexpected loading state afterward.

The cart contents were preserved, and normal cart navigation was restored after refreshing the page.