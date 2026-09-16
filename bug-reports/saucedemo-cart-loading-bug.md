# Bug Report: Cart Navigation Fails After Adding Item

## Environment

- Application: SauceDemo
- Browser: Google Chrome 153
- Operating System: Windows 11
- Date Tested: September 16, 2026

## Steps to Reproduce

1. Open a product.
2. Select product options as needed.
3. Add the item to the cart.
4. Confirm the cart badge updates.
5. Observe that an indefinite loading spinner appears after the item is added.
6. Click **My Cart**.

## Expected Result

The item should be added to the cart without leaving the application in a loading state, and clicking **My Cart** should open the cart.

## Actual Result

After the item is added, an indefinite loading spinner appears even though the cart badge updates correctly.

Clicking **My Cart** causes the spinner to disappear, but the cart does not open.

Clicking **My Cart** again causes the spinner to reappear.

Refreshing the page clears the spinner. After the refresh, clicking **My Cart** successfully opens the cart.

The cart contents and cart badge remain correct throughout.

If **Checkout** is clicked while the spinner is active, the application successfully navigates to the checkout page with the correct items and total amount.

## Reproducibility

Reproduced consistently across 5+ attempts and with more than one product.

## Severity

Medium
