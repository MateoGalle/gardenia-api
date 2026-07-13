# Gardenia Product Backlog

## Purpose

This document contains the initial product backlog for the Gardenia e-commerce platform.

The backlog is organized into Epics and User Stories. Priorities may change based on client feedback, technical discoveries, and business needs.

---

## Priority Levels

* **Must Have**: Required for the first usable version.
* **Should Have**: Important, but not required for the earliest release.
* **Could Have**: Valuable future enhancement.
* **Won't Have Yet**: Explicitly postponed.

---

# Epic 1: Product Catalog

## US-001 — Browse Products

**As a** customer,
**I want to** browse the available products,
**so that** I can discover Gardenia accessories.

**Priority:** Must Have

### Acceptance Criteria

* The customer can view a list of active products.
* Each product displays its name, price, primary image, and availability.
* Inactive products are not visible to customers.

---

## US-002 — View Product Details

**As a** customer,
**I want to** view the details of a product,
**so that** I can decide whether it meets my needs.

**Priority:** Must Have

### Acceptance Criteria

* The customer can view the product name, description, price, images, and available variants.
* The customer can see whether a variant is in stock.
* The product page displays available colors.

---

## US-003 — View New Arrivals

**As a** customer,
**I want to** access new arrivals easily,
**so that** I can discover Gardenia’s latest products.

**Priority:** Must Have

### Acceptance Criteria

* The platform displays a dedicated New Arrivals section.
* Recently added active products appear in this section.
* The section is accessible from the homepage.

---

## US-004 — View Clearance Products

**As a** customer,
**I want to** access clearance products easily,
**so that** I can find discounted items.

**Priority:** Must Have

### Acceptance Criteria

* The platform displays a dedicated Clearance section.
* Clearance products display their current price.
* Inactive or unavailable products are not displayed.

---

# Epic 2: Product Administration

## US-005 — Create a Product

**As a** Gardenia administrator,
**I want to** create a product,
**so that** it can be displayed in the online catalog.

**Priority:** Must Have

### Acceptance Criteria

* The administrator can enter the product name, description, base price, category, and status.
* The system validates required information.
* The product is stored successfully.
* The product receives a unique identifier.

---

## US-006 — Update a Product

**As a** Gardenia administrator,
**I want to** update product information,
**so that** the catalog remains accurate.

**Priority:** Must Have

### Acceptance Criteria

* The administrator can update editable product information.
* Invalid data is rejected.
* Changes are persisted.
* The product modification date is updated.

---

## US-007 — Deactivate a Product

**As a** Gardenia administrator,
**I want to** deactivate a product,
**so that** unavailable products are hidden without losing their historical information.

**Priority:** Must Have

### Acceptance Criteria

* The administrator can mark a product as inactive.
* Inactive products are hidden from the public catalog.
* Existing order records remain unchanged.

---

# Epic 3: Categories and Product Variants

## US-008 — Manage Categories

**As a** Gardenia administrator,
**I want to** manage product categories,
**so that** products can be organized clearly.

**Priority:** Must Have

### Acceptance Criteria

* The administrator can create and update categories.
* A product can be assigned to a category.
* Duplicate category names are rejected.

---

## US-009 — Manage Product Variants

**As a** Gardenia administrator,
**I want to** create product variants,
**so that** different colors or designs can have their own stock.

**Priority:** Must Have

### Acceptance Criteria

* A product can have one or more variants.
* Each variant has its own SKU.
* Each variant has its own stock quantity.
* A variant can represent one color or a color combination.
* A variant can be activated or deactivated.

---

## US-010 — Manage Product Images

**As a** Gardenia administrator,
**I want to** associate images with products,
**so that** customers can evaluate products visually.

**Priority:** Must Have

### Acceptance Criteria

* A product can have multiple images.
* One image can be marked as the primary image.
* Images have a display order.
* Invalid image references are rejected.

---

# Epic 4: Search and Filtering

## US-011 — Search Products

**As a** customer,
**I want to** search for products,
**so that** I can find specific accessories quickly.

**Priority:** Should Have

### Acceptance Criteria

* Customers can search by product name.
* Search ignores letter casing.
* Only active products are returned.
* A clear response is shown when no products match.

---

## US-012 — Filter Products

**As a** customer,
**I want to** filter products by category, color, price, and rating,
**so that** I can narrow down the catalog.

**Priority:** Should Have

### Acceptance Criteria

* Customers can filter by category.
* Customers can filter by color.
* Customers can filter by a price range.
* Multiple filters can be combined.
* Rating filters will become available when reviews are implemented.

---

# Epic 5: Customer Accounts

## US-013 — Register an Account

**As a** customer,
**I want to** create an account,
**so that** I can access personalized features.

**Priority:** Should Have

### Acceptance Criteria

* The customer can register with valid personal information.
* Email addresses must be unique.
* Passwords are stored securely.
* Invalid registration attempts are rejected.

---

## US-014 — Sign In

**As a** registered customer,
**I want to** sign in securely,
**so that** I can access my account.

**Priority:** Should Have

### Acceptance Criteria

* The customer can sign in with valid credentials.
* Invalid credentials do not reveal sensitive information.
* Successful authentication returns a valid access token.
* Protected operations require authentication.

---

# Epic 6: Wishlist

## US-015 — Add a Product to Wishlist

**As a** registered customer,
**I want to** save a product to my wishlist,
**so that** I can review or purchase it later.

**Priority:** Should Have

### Acceptance Criteria

* Only authenticated customers can use a persistent wishlist.
* A customer can add an active product.
* The same product cannot be added twice.
* Wishlist information remains available in future sessions.

---

## US-016 — Remove a Product from Wishlist

**As a** registered customer,
**I want to** remove a product from my wishlist,
**so that** I can keep my saved items organized.

**Priority:** Should Have

### Acceptance Criteria

* The customer can remove a saved product.
* The operation only affects the authenticated customer’s wishlist.
* Removing a missing item does not corrupt the wishlist.

---

# Epic 7: Shopping Cart

## US-017 — Add an Item to the Cart

**As a** customer,
**I want to** add a product variant to my cart,
**so that** I can prepare an order.

**Priority:** Must Have

### Acceptance Criteria

* Registered customers and guests can use a cart.
* The customer selects a specific product variant.
* The requested quantity cannot exceed available stock.
* Adding the same variant updates its quantity.

---

## US-018 — Update Cart Quantity

**As a** customer,
**I want to** update the quantity of an item,
**so that** my cart reflects what I intend to purchase.

**Priority:** Must Have

### Acceptance Criteria

* Quantities must be greater than zero.
* Quantities cannot exceed available stock.
* Cart totals are recalculated after the update.

---

## US-019 — Remove an Item from the Cart

**As a** customer,
**I want to** remove an item from my cart,
**so that** I can modify my intended purchase.

**Priority:** Must Have

### Acceptance Criteria

* The selected item is removed.
* The cart total is recalculated.
* Removing one item does not affect the others.

---

# Epic 8: Orders and Checkout

## US-020 — Create an Order

**As a** customer,
**I want to** submit my cart as an order,
**so that** I can purchase Gardenia products.

**Priority:** Must Have

### Acceptance Criteria

* Registered customers and guests can create orders.
* Customer and Canadian delivery information is required.
* Order items preserve the price at the time of purchase.
* The order total is calculated by the backend.
* An order status is assigned.
* Stock is validated before the order is confirmed.

---

## US-021 — View Order Details

**As a** customer,
**I want to** view my order details,
**so that** I can verify my purchase information.

**Priority:** Should Have

### Acceptance Criteria

* Registered customers can only access their own orders.
* Order details include items, quantities, prices, total, date, and status.
* Guest order access will require a secure verification mechanism.

---

## US-022 — Process a Secure Payment

**As a** customer,
**I want to** pay through a trusted payment provider,
**so that** I can complete my purchase securely.

**Priority:** Must Have before production launch

### Acceptance Criteria

* Payment information is handled by a verified provider.
* Gardenia does not store raw payment card data.
* An order is only marked as paid after provider confirmation.
* Failed or cancelled payments do not mark the order as paid.

> Payment provider selection is pending.

---

# Epic 9: Localization

## US-023 — Change Platform Language

**As a** customer in Canada,
**I want to** switch between English and French,
**so that** I can use the platform in my preferred language.

**Priority:** Should Have

### Acceptance Criteria

* The user can switch between English and French.
* The selected language applies consistently to the interface.
* Product content translation requirements remain subject to client confirmation.

---

# Epic 10: Reviews

## US-024 — View Product Reviews

**As a** customer,
**I want to** view product reviews,
**so that** I can make a more informed purchasing decision.

**Priority:** Should Have

### Acceptance Criteria

* Product pages display approved reviews.
* Each review shows a rating and optional comment.
* The average rating is calculated from approved reviews.

---

## US-025 — Submit a Product Review

**As a** registered customer,
**I want to** review a product I purchased,
**so that** I can share my experience.

**Priority:** Could Have

### Acceptance Criteria

* Only authenticated customers can submit reviews.
* Purchase verification should be required.
* Ratings must be within the accepted range.
* Moderation rules will be defined later.

---

# Epic 11: Brand and Trust

## US-026 — Display Brand and Legal Information

**As a** customer,
**I want to** see Gardenia’s official brand and legal information,
**so that** I can trust that I am buying from the legitimate business.

**Priority:** Must Have

### Acceptance Criteria

* The footer displays required trademark and legal information.
* Official contact information is visible.
* Links to policies are accessible.
* Official social media links are clearly identified.

---

# Epic 12: Future Enhancements

## US-027 — Access Customer Support

**As a** customer,
**I want to** access support from the platform,
**so that** I can resolve questions or navigation problems.

**Priority:** Could Have

---

## US-028 — Use a Virtual Assistant

**As a** customer,
**I want to** ask a virtual assistant questions,
**so that** I can discover products and receive assistance.

**Priority:** Won't Have Yet

---

## US-029 — Receive Product Recommendations

**As a** customer,
**I want to** receive relevant product recommendations,
**so that** I can discover accessories that match my interests.

**Priority:** Won't Have Yet

---

# Initial Development Order

The initial backend development order will be:

1. Categories
2. Products
3. Product variants
4. Product images
5. Public catalog queries
6. Customer authentication
7. Wishlist
8. Shopping cart
9. Orders
10. Payment integration

This order may change as the product evolves.
