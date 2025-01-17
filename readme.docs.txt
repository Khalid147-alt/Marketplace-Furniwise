[Client Browser]
    |
    --> [Frontend (Next.js 15 in TypeScript with Tailwind CSS)]
           - Pages:
               - Home
               - Product Listing
               - Product Details
               - Cart
               - Checkout
               - Admin Dashboard (optional)
           - Features:
               - Dynamic routing
               - SEO optimizations
               - Responsive design
    |
    --> [APIs Layer (Middleware)]
           - Endpoints:
               - GET /products (Fetch product listings)
               - GET /products/:id (Fetch product details)
               - POST /orders (Place an order)
               - GET /orders/:id (Fetch order details)
               - POST /reviews (Submit a review)
           - Security:
               - Authentication (JWT or OAuth for user login)
               - Rate limiting to prevent abuse
    |
    --> [Sanity CMS Backend]
           - Schemas:
               - Product: { id, name, price, description, stock, images, category, tags }
               - Category: { id, name, slug }
               - Order: { id, customerDetails, productList, totalAmount, status }
               - User Review: { id, productId, rating, comment, userId }
           - Real-time content updates
           - Admin panel for managing products and categories
    |
    --> [Sanity Database (Document-Based NoSQL)]
           - Stores:
               - Product data
               - Category data
               - Orders
               - User reviews
    |
    --> [Third-Party Integrations]
           - **Stripe**: For secure payment processing
               - Webhooks for payment confirmation
               - Payment methods: Credit/debit cards, wallets
           - **Shipment Tracking APIs**: DHL, FedEx, or local courier APIs
               - Track orders and update shipment status
           - **SendGrid**: For email notifications
               - Order confirmation emails
               - Shipping updates
