# Woodenzone Website Prompt

Paste this into an AI website builder or coding assistant to recreate the Woodenzone homepage. Add your own product photos in the `images/` folder.

---

## Prompt

Build a single-page, responsive e-commerce homepage for **WOODENZONE**, a wooden furniture, lighting, home décor and kitchenware manufacturer in Saharanpur, India. Use one self-contained `index.html` file (HTML, CSS and vanilla JavaScript, no frameworks).

### Brand details
- Name: Woodenzone
- Tagline: "Crafted by Nature, Made for You."
- Phone / WhatsApp: +91 8077625193
- Email: mywoodenzone@gmail.com
- Instagram: @woodenzone
- Location: Saharanpur, India
- Primary button text: "Shop the Collection"

### Visual style
Premium, warm, natural and handcrafted. Not a generic furniture store.

| Token | Hex |
|---|---|
| Ivory (page background) | #FAF6EE |
| Cream | #F1E9DA |
| Beige | #E4D6BF |
| Walnut | #6B4A32 |
| Dark chocolate (text, buttons) | #2E1F16 |
| Muted gold (accents) | #B08D4C |
| Natural wood | #A9794F |

- Headings: Cormorant Garamond (serif). Body: Inter (sans-serif).
- Rounded buttons, arch-shaped hero image, soft rounded product images.
- Subtle motion only: one fade-in on the hero, hover underline on nav links, small lift on cards. Respect `prefers-reduced-motion`.

### Page sections (in order)
1. **Sticky header:** text wordmark "WOODENZONE" (gold on "ZONE"), links to Furniture, Lighting, Home Decor, Kitchenware, New Arrivals, About Us, Contact, plus Search and a Wishlist counter. Hamburger menu on mobile.
2. **Hero:** headline "Crafted by Nature, Made for You.", subheading "Timeless wooden creations for beautiful everyday living.", buttons "Shop the Collection" and "Explore Collection". Large arch-shaped lifestyle photo on the right.
3. **Shop by category:** four cards (Furniture, Lighting, Home Decor, Kitchenware) with a short line each. Swipeable row on mobile. The Lighting card jumps to the Table Lamps filter.
4. **Made for Modern Living (product grid):** filter chips: All, Chairs, Side Tables, Console Tables, Sofas & Tables, Table Lamps. Three-column grid on desktop, one column on mobile.
5. **Why Woodenzone?** (dark walnut section, four columns): Natural Materials, Skilled Craftsmanship, Made in Saharanpur, Built for Everyday Living.
6. **From Wood to Your Home:** short story text, a showroom photo, and chips for Wood selection, Cutting, Shaping, Sanding, Finishing, Quality inspection. Mention that Woodenzone works with exporters and established companies while developing its own premium collection.
7. **Newsletter:** "Bring Natural Beauty Home." with email field and Subscribe button.
8. **Footer:** dark walnut, with Shop, Company and Contact columns.
9. **Floating "WhatsApp us" button** (bottom right) linking to `https://wa.me/918077625193`.

### Product cards
Each card shows: square or 4:5 photo, wishlist heart, product name, SKU (if any) and category, short description, "Price on request", and an **Enquire** button. Clicking the photo opens it large in a `<dialog>` lightbox (click anywhere to close). The Enquire button opens WhatsApp with a message already filled in: "Hi Woodenzone, I'd like to enquire about the {product name} ({SKU})."

Store products in a JavaScript array: `[name, sku, description, category, imageIndex]`.

### Behaviour
- Filter chips show and hide cards by category.
- Heart toggles the wishlist and updates the counter in the header. A small toast message confirms each action.
- Newsletter form shows a "Thanks for subscribing" toast (no backend).
- No cart or checkout. Orders happen through WhatsApp.

### Responsive and quality
- Mobile-first layout. Breakpoint at 900px.
- Handle device safe areas (`viewport-fit=cover`, `env(safe-area-inset-*)`).
- Visible keyboard focus, alt text on images, lazy-load product images.

### Images
Use files from `images/`. Do not hotlink. Product photos should be warm, natural and consistent with the palette above.

---

## Ideas for next steps
- Add real prices, a cart and checkout (for example Razorpay or Stripe).
- Add individual product pages with dimensions, material and care instructions.
- Add photos for Home Decor and Kitchenware.
- Add an Instagram gallery and customer reviews.
- Connect the newsletter form to an email service.
