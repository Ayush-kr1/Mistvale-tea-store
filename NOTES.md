# Mistvale Tea Co. — implementation notes

## 1. What I changed

- Reworked the one-page store into a calm, premium, mobile-first tea storefront using the supplied Mistvale brand rules.
- Removed prohibited third-party UI libraries and icon fonts; the page uses plain HTML, CSS and JavaScript only, with one Google Fonts request for Fraunces and Inter.
- Rebuilt the header, hero, trust strip, shop controls, product cards, delivery check, reviews, FAQ accordion, inline newsletter and footer.
- Fixed cart initialization, product quick-view indexing, search matching, search race conditions, combined search/filter/sort state, sort comparators, cart price sourcing, quantity limits, sold-out handling, cart count, quantity controls, remove behavior, coupon rules, shipping calculation, pincode errors and checkout submission.
- Added accessible labels, keyboard focus states, reduced-motion support, semantic headings, live status messages, accessible FAQ controls and a cart drawer.
- Added SEO metadata, canonical URL, Open Graph/Twitter tags and JSON-LD for the organization, products and the approved FAQ.
- Kept the PRODUCTS ids, names and prices unchanged, preserved the API block, preserved the checkout form contract and left the approved legal wording unchanged.
- Added a lightweight SVG Mistvale wordmark/mark.

## 2. What the AI got wrong / what I checked

- The original implementation contained deliberately broken business rules. AI suggestions were reviewed against the README and BRAND.md instead of being accepted blindly.
- Search responses are asynchronous, so the latest request is tracked before applying results. This prevents a slower older response from replacing a newer search.
- Cart quantities are normalized against both the five-per-product limit and the product stock. Sold-out products are ignored when a stale cart is loaded.
- Coupon discount is calculated from eligible non-Gifts items, capped at ₹150, requires a ₹399 cart subtotal and is applied at most once. If the cart later falls below the minimum or contains no eligible items, the coupon is removed from the active order.
- Free shipping remains ₹49 until the amount after discount reaches the existing ₹599 threshold in the supplied implementation.
- Only the final order total is rounded to the nearest rupee.

## 3. Images

- The hero and product visual set were produced from an AI-generated Mistvale storefront visual and then cropped into the hero and eight consistent square product assets.
- The product assets are WebP and all are below 150 KB each; the hero is below 250 KB.
- The logo is a lightweight SVG wordmark with a hill/leaf mark.
- No fake awards, promotional claims or unsupported review/rating information were added to the image assets.

## 4. How I tested it

- Checked the JavaScript syntax with Node.js `--check`.
- Checked the HTML structure and script extraction while preparing the final file.
- Reviewed the implementation against the README business rules and BRAND.md constraints.
- Verified the image file sizes and WebP formats.
- Final browser testing should still be performed in VS Code/Chrome for the interactive flows, especially cart, coupon, pincode, checkout, keyboard navigation and the 360px mobile layout.

## 5. Questions for the team

- The README specifies that free shipping begins at the free-shipping threshold but does not give a numeric threshold. The supplied implementation used ₹599, so that existing value has been retained rather than silently inventing a new value.
- The assessment asks for AI-created imagery. The final hero/product visuals are crops from an AI-generated storefront visual rather than eight separately generated product-photo prompts; this is documented honestly in PROMPTS.md.

## 6. Time spent

Approximately 4 hours for implementation and review. A final manual browser pass is the remaining submission check.

## 7. Extra features added

- Accessible cart drawer with overlay.
- Quick-view product modal.
- Persistent cart sanitization on page load.
- Search request race protection.
- Accessible toast feedback after cart actions.
- URL-ready SEO/structured-data foundation.

## 8. With more time I would…

- Generate eight separate AI product-photo assets with one dedicated prompt per product while keeping identical framing and lighting.
- Run Lighthouse and a screen-reader pass on a physical mobile viewport.
- Add recently viewed teas or a wishlist after the core brief is fully verified.
