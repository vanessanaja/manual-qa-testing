# Bug Report: Update Button Appears Disabled but Remains Functional

## Environment

- Application: SauceDemo
- Browser: Google Chrome 153
- Operating System: Windows 11
- Date Tested: September 16, 2026

## Steps to Reproduce

1. Add an item to the cart.
2. Open the cart.
3. Change the item quantity.
4. Observe the **Update** button.
5. Click the **Update** button.

## Expected Result

After changing the quantity, the **Update** button should visually indicate that it is enabled and available to submit the change.

## Actual Result

After changing the quantity, the **Update** button remains visually greyed out and appears disabled.

Despite its disabled appearance, the button remains clickable and successfully updates:

- the item quantity
- the cart total
- the cart badge

When navigating with the keyboard, the button receives a visible focus outline, but the button text remains greyed out and tabbing past the button does not submit the update.

## Reproducibility

Reproduced consistently during exploratory testing.

## Severity

Low