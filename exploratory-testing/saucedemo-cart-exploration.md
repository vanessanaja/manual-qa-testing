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

### Cart Quantity and Update Behavior

- Changed product quantity from `1` to `2`.
- Quantity updated correctly.
- Cart total updated correctly.
- Changed quantity to `222`.
- Quantity and total updated correctly.
- Changed quantity to `0`.
- Item was removed from the cart.
- Cart badge updated correctly.
- The **Update** button remains visually greyed out after quantity changes, but clicking it still updates the cart successfully.
- Keyboard focus adds a black outline to the Update button, but tabbing past the button does not submit the update.

### Cart Notes

- Entered text into the cart notes field.
- Updated the cart.
- Note remained after page refresh.
- Note also remained after leaving the cart and returning.
- Notes appear to persist correctly.

### Multiple Items

- Added shoes to the cart.
- Added the jacket as a second item.
- Cart badge correctly displayed `2`.
- Individual item prices and total amount were correct.
- **Continue Shopping** returned to the product area successfully.

### Checkout Validation

- Checkout displayed the correct items and total.
- Invalid email format was rejected.
- ZIP code validation recognized a mismatch between state and ZIP code.
- Invalid phone area code was rejected.
- Expiration month greater than `12` was rejected.
- Expiration year in the past was rejected.
- A misspelled city name (`Los Angels`) was accepted without validation.
- The state/region selector included Micronesia as an option.

### Payment Simulation

- Entering the documented approved-transaction value completed checkout successfully.
- Simulated declined transaction returned:
  `There was an issue processing your payment. Try again or use a different payment method.`
- Simulated pathway failure returned the same payment-processing error message as the declined transaction.