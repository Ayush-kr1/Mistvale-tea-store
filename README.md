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