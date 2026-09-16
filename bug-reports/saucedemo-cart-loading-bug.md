# Bug Report: Cart Navigation Fails After Adding Item

## Environment

- Application: SauceDemo
- Browser: Google Chrome 153
- Operating System: Windows 11
- Date Tested: September 16, 2026

## Steps to Reproduce

1. Open a jacket product.
2. Change the size to Medium.
3. Change color to Red
4. Add the item to the cart.
5. Confirm the cart badge updates to `1`.
6. Click **My Cart**.

## Expected Result

The cart should open and display the selected item.

## Actual Result

After the item is added, an indefinite loading spinner appears.

Clicking **My Cart** causes the spinner to disappear, but the cart does not open.

Clicking **My Cart** again causes the spinner to reappear.

Refreshing the page clears the spinner. After the refresh, clicking **My Cart** successfully opens the cart.

## Severity

Medium

## Reproducibility

Reproduced 3 out of 3 attempts.