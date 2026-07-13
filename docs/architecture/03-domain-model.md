# Gardenia Domain Model

## Purpose

The purpose of this document is to identify the main business entities of the Gardenia platform before any database or software implementation begins.

The Domain Model focuses on the business itself rather than on technical implementation.

---

# Core Domain

Gardenia is an e-commerce platform specialized in women's accessories.

The business revolves around products, customers, shopping experiences, and orders.

---

# Main Entities

## Product

Represents a product sold by Gardenia.

A product describes the accessory itself independently of its available colors or inventory.

Examples:

- Handmade Bracelet
- Leather Bag
- Necklace

### Responsibilities

- Store product information.
- Belong to a category.
- Have one or more variants.
- Have one or more images.
- Receive customer reviews.

---

## Product Variant

Represents a purchasable variation of a product.

Examples:

- Handmade Bracelet - Red
- Handmade Bracelet - Blue
- Leather Bag - Black

Each variant owns its own inventory.

### Responsibilities

- Store stock quantity.
- Store SKU.
- Store availability.
- Reference one product.

---

## Category

Represents a logical classification for products.

Examples:

- Bracelets
- Bags
- Earrings

---

## Product Image

Represents an image associated with a product.

A product can have multiple images.

One image may be designated as the primary image.

---

## Customer

Represents a customer using the platform.

Customers may purchase products and maintain personalized information.

Future versions will support authentication.

---

## Wishlist

Represents a customer's saved products.

Only authenticated customers can have persistent wishlists.

---

## Wishlist Item

Represents a saved product inside a wishlist.

---

## Shopping Cart

Represents products a customer intends to purchase.

Both guests and registered users may own a shopping cart.

---

## Cart Item

Represents a product variant inside the shopping cart.

Stores:

- Variant
- Quantity
- Unit price snapshot

---

## Order

Represents a completed purchase.

Orders preserve historical information even if products later change.

---

## Order Item

Represents an individual purchased product.

Stores:

- Variant
- Quantity
- Purchase price

---

## Review

Represents customer feedback for products.

Stores:

- Rating
- Comment
- Creation date

Future versions may restrict reviews to verified purchases.

---

# Domain Relationships

Category

↓

Products

↓

Product Variants

↓

Cart Items

↓

Order Items

Customer

↓

Wishlist

↓

Wishlist Items

Customer

↓

Shopping Cart

↓

Orders

Customer

↓

Reviews

---

# Initial Business Rules

The following business rules have been identified.

BR-001

A product must belong to one category.

BR-002

A product must contain at least one active variant before becoming available.

BR-003

Each product variant manages its own stock.

BR-004

Inactive products are not visible to customers.

BR-005

Wishlist requires an authenticated customer.

BR-006

Shopping carts are available for guests and registered customers.

BR-007

Orders preserve product prices at purchase time.

BR-008

Stock cannot become negative.

BR-009

Only active variants can be purchased.

BR-010

Reviews belong to products.