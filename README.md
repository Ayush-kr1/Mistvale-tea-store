# 🍵 Mistvale Tea Co.

> **Hill-grown tea, honestly made.**

A responsive one-page online tea store created as part of the **MeroxIO Web Developer Interview Assessment**.

---

## 📌 About the Project

**Mistvale Tea Co.** is a modern one-page online tea store designed to provide a clean, responsive, and user-friendly shopping experience.

The project was developed as part of the MeroxIO Web Developer Assessment. The main focus was to improve the existing storefront, fix functional and business-logic issues, improve the UI/UX, implement shopping functionality, optimize images, and add accessibility and SEO improvements.

The website follows the required Mistvale Tea Co. brand direction:

**Brand:** Mistvale Tea Co.  
**Tagline:** Hill-grown tea, honestly made.  
**Founded:** 2019

---

## 🎯 Project Goals

The main goals of the project were:

- Improve the overall website design
- Create a professional tea-store experience
- Fix existing functional bugs
- Implement reliable shopping-cart functionality
- Improve product discovery
- Add search, filtering and sorting
- Implement coupon and shipping rules
- Handle sold-out products correctly
- Add delivery pincode checking
- Improve accessibility
- Improve SEO
- Optimize website imagery
- Make the website responsive across desktop and mobile
- Keep the implementation within the assessment constraints

---

## ✨ Features

### 🛍️ Product Store

The website includes a complete product browsing experience.

Features include:

- Product listing
- Product images
- Product names
- Product descriptions
- Product prices
- Product ratings
- Product categories
- Product badges
- Search
- Category filtering
- Sorting
- Product quick view
- Stock handling
- Sold-out handling

---

## 🔎 Product Search

Users can search for tea products using the search field.

The search functionality works together with the product filtering and sorting system.

The implementation also handles asynchronous search responses so that an older response does not overwrite the result of a newer search request.

### Search flow

```text
User Search
     ↓
Search Request
     ↓
Matching Product IDs
     ↓
Product Filtering
     ↓
Category Filter
     ↓
Sorting
     ↓
Product Rendering


## 📌 Project Overview

Mistvale Tea Co. is a modern online tea-store interface designed to provide a simple and user-friendly shopping experience.

The project focuses on:

- Responsive UI/UX
- Product browsing
- Search, filtering and sorting
- Shopping cart functionality
- Product quick view
- Coupon validation
- Shipping calculation
- Pincode delivery checking
- FAQ accordion
- Newsletter signup
- Accessibility
- SEO optimization
- Optimized product imagery

## 🛠️ Technologies Used

- HTML5
- CSS3
- Vanilla JavaScript
- Google Fonts
- LocalStorage
- WebP images
- SVG

No jQuery or frontend framework is used.

### Shopping Cart
- Add products to cart
- Increase/decrease quantity
- Maximum 5 units per product
- Stock-based quantity validation
- Remove products
- Total quantity cart count
- Cart persistence using LocalStorage

### Coupon

The store supports:

`WELCOME10`

Rules:

- 10% discount
- Minimum eligible subtotal: ₹399
- Maximum discount: ₹150
- Case-insensitive coupon code
- Gift products are excluded
- Discount cannot be stacked

### Delivery

- Pincode serviceability check
- Delivery estimate
- Invalid pincode handling
- Free shipping threshold
- Shipping fee calculation

### UX & Accessibility

- Responsive desktop and mobile layout
- Keyboard-friendly interactions
- Visible focus states
- ARIA attributes
- Accessible FAQ accordion
- Image alt text
- Reduced-motion support
- Toast/status messages

### SEO

The project includes:

- SEO-friendly title
- Meta description
- Canonical URL
- Open Graph metadata
- Twitter metadata
- Structured data
- Product schema
- FAQ schema
- Organization/OnlineStore structured data

## 📁 Project Structure

```text
mistvale-tea-store/
│
├── images/
│   ├── logo.svg
│   ├── hero-banner.webp
│   ├── p101.webp
│   ├── p102.webp
│   ├── p103.webp
│   ├── p104.webp
│   ├── p105.webp
│   ├── p106.webp
│   ├── p107.webp
│   └── p108.webp
│
├── index.html
├── NOTES.md
└── PROMPTS.md
