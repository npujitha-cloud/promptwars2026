# promptwars2026
solution for promptwars2026
What I would build
I would focus on inventory accuracy + order rescue, rather than building another customer shopping app.
Product idea: NOVA RESCUE
An AI-powered Order Rescue & Inventory Intelligence platform for NOVA CART.
The core idea:
When NOVA CART is about to lose an order because a product is unavailable, a store rejects it, or delivery is delayed, the system detects the problem and recommends the best action before the customer cancels.
It has three connected parts:
1. Customer side
Suppose I order:
Milk + Bread + Eggs + Medicine
The system detects that the selected store probably doesn't have the milk.
Instead of:

"Sorry, item unavailable → cancel/refund."

It can show:

⚠️ Milk may be unavailable at Store A

Available nearby:

Store B — 450m away

Store C — 700m away

Replace item / Switch store / Continue without item

This directly attacks the 35% of cancellations caused by product unavailability.

2. Store side
Give partner stores a simple dashboard:

Inventory Health

🔴 17 high-risk products

🟡 32 products need verification

🟢 486 products likely accurate

The store doesn't need to manually update thousands of products.

Instead:

"These 12 products are frequently searched but often unavailable."

The store can quickly confirm:

Available / Out of Stock / Update Quantity

This addresses the partner complaint that maintaining inventory is too much work.

3. NOVA CART operations dashboard
This is where your prototype becomes much more impressive.

Show:

Order Risk Monitor

Order	Risk	Reason	Recommended Action
#NC1021	🔴 High	Product unavailable	Find nearby store
#NC1022	🟡 Medium	Delivery delay	Reassign partner
#NC1023	🔴 High	Store rejection	Switch store
#NC1024	🟢 Low	—	Continue

Then the system calculates something like:

Rescue Opportunity: ₹48,600/month

based on potentially recoverable cancelled orders.

That gives you a very clear INPUT → PROCESS → OUTPUT story.

Why this problem is strongly supported by the case
You have several pieces of evidence pointing toward the same underlying issue.

Customer problem
11% orders are cancelled.

35% of cancellations are because products are unavailable.

29% of customers report products becoming unavailable after ordering.

19% repeatedly search for unavailable products.

8% of orders contain substitutions.

6% require refund/support interaction.

Operational problem
Delivery time increased:

29 min → 37 min

Cancellation increased:

6% → 11%

Support tickets increased:

3,100 → 5,900/month

Partner problem
39% say inventory maintenance requires too much effort.

23% sometimes reject orders during busy periods.

18% are considering leaving.

Some stores update inventory only once every 1–3 days.

And there's an important strategic opportunity:

NOVA CART's potential advantage is its 620 independent local stores.

So instead of trying to beat huge competitors purely on discounts and delivery speed, your product can make the local-store network smarter.

That's a much stronger competition story.

Your website could therefore have this structure
NOVA RESCUE
│
├── Command Center
│   ├── Orders at Risk
│   ├── Revenue at Risk
│   ├── Cancellation Rate
│   ├── Inventory Accuracy
│   └── Rescue Rate
│
├── Order Rescue
│   ├── At-risk orders
│   ├── Detect issue
│   ├── Find alternatives
│   └── Recommend action
│
├── Inventory Intelligence
│   ├── Store inventory health
│   ├── High-risk products
│   ├── Search demand
│   └── Stock verification
│
├── Store Dashboard
│   ├── Today's alerts
│   ├── Update inventory
│   └── Demand insights
│
└── Business Impact
    ├── Orders rescued
    ├── Revenue recovered
    ├── Cancellations prevented
    ├── Support tickets avoided
    └── Estimated ROI

And this is where Lovable becomes useful
You don't need to manually create every file from scratch.

You can build this as a proper React/web application in Lovable, then connect/export the project to GitHub.

Your final repository would contain things such as:

nova-rescue/
│
├── src/
│   ├── components/
│   ├── pages/
│   ├── data/
│   └── ...
│
├── public/
├── package.json
├── README.md
├── vite.config.ts
└── ...

Then:

Lovable → GitHub → Repository → Deploy

One important thing
Don't make the Lovable app just a collection of pretty dashboards.

The judges specifically say:

INPUT → PROCESSING / LOGIC → ACTION / RECOMMENDATION / OUTPUT

So your demo should actually let the judge do something.

For example:

Demo
Step 1 — Create/select an order

Customer orders:

Milk
Bread
Eggs

Step 2 — System detects

⚠️ Milk has 73% probability of being unavailable.

Step 3 — System searches

Nearby stores:

Store B — Milk available
Store C — Milk available

Step 4 — System recommends

Switch order to Store B

Step 5 — Click "Rescue Order"

The application changes:

🟢 Order rescued

And your dashboard updates:

Orders Rescued       +1
Revenue Saved        ₹486
Potential Cancellation -1
Customer Experience  Protected
