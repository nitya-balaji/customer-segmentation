# Customer Segmentation for Targeted Marketing - ML Project

## Project Overview

This project applies unsupervised machine learning to a grocery store's customer dataset to identify distinct behavioural and demographic segments. Rather than relying on broad, untargeted campaigns, the segmentation allows the business to tailor its marketing strategy to each customer group, improving relevance and driving higher ROI.

This end-to-end project pipeline in Python includes:

- **Data cleaning & feature engineering** — preprocessed raw customer data and created new features including total spend, household size, customer tenure, and age
- **Dimensionality reduction (PCA)** — reduced the feature space to 3 components capturing 53% of total variance. The first component reflects purchasing power and the second captures household life stage
- **Optimal cluster selection** — applied the Elbow Method to identify 4 as the ideal number of clusters
- **Agglomerative Clustering** — assigned all customers to one of 4 segments using hierarchical clustering
- **Visualisation** — projected final cluster assignments into 3D PCA space to confirm clean separation between groups

---

## Cluster Profiles

### Cluster 0 — Mid-Income Parents

**Cluster Description:**
- Income around $62K with an average total spend of $881
- Nearly all are parents (98%), with 1–2 children and households of about 3 people
- Older customers (around 61 years) who shop comfortably across both in-store and online channels
- Somewhat deal-aware, picking up promotions occasionally but not actively driven by them

**Recommended Approach:**
- Family-focused loyalty programs and seasonal bundle promotions (e.g., back-to-school, holiday meal kits) are well-suited to this group
- They shop across channels, so coordinated email and in-store campaigns will reach them effectively
- They have enough income to spend more. Gradually introducing premium product recommendations alongside their regular purchases is a realistic upsell path

---

### Cluster 1 — Low-Income Young Families

**Cluster Description:**
- Lowest income of all segments ($31K) and very low average spend ($119)
- Despite visiting the website more than any other segment (6.8x/month), they have the lowest purchase conversion rate
- Roughly 75% are parents, mostly with younger children, in smaller households (around 2.4 people)
- Minimal campaign engagement with nearly zero promotions accepted on average

**Recommended Approach:**
- High-production campaigns will not pay off here, so keep investment lean
- Their high web visit frequency is an opportunity. Target them with homepage deal banners, cart abandonment flows, and digital weekly flyers
- Messaging should lead with clear, concrete savings on everyday essentials rather than brand or lifestyle angles

---

### Cluster 2 — High-Income Childless Customers

**Cluster Description:**
- Highest income ($77K) and by far the highest average spend ($1,401)
- Almost entirely childless (1% are parents), living alone or with a partner in small households (around 1.6 people)
- The most campaign-responsive segment, averaging 0.77 accepted promotions, but the least deal-driven (lowest deal purchase rate)
- Low web engagement with a strong preference for shopping in-store and through catalog

**Recommended Approach:**
- Do not rely on discounts. They buy without them and discounting only erodes margin
- Premium product categories (specialty meats, imported wines, artisan goods) are the natural focus for this segment
- Catalog and in-store are the right channels. Invest here rather than digital
- Exclusive experiences such as tasting events or early access to new products will reinforce loyalty and justify premium pricing

---

### Cluster 3 — Low-Income Large Families

**Cluster Description:**
- Every customer is a parent (100%), with the largest average household size of any cluster (3.44 people, 1.76 children)
- Income ($43K) is slightly higher than Cluster 1, but spend is nearly as low ($132) given the financial demands of a large family
- Older demographic (around 61 years) with very low engagement across promotions and deals

**Recommended Approach:**
- Bulk and multi-buy deals on staple items directly address both their volume needs and budget constraints
- Kid-focused categories like snacks, breakfast foods, school lunches, and quick-prep meals are high relevance and worth building promotions around
- Keep messaging straightforward and savings-focused. Complex or premium campaigns will not connect with this group

---

## Strategic Takeaways

- **Spend is driven by income and household composition, not age** — Cluster 2 is not the youngest, yet spends 10x more than the lowest clusters. Disposable income and the absence of children are the real predictors.
- **Parenthood structurally limits spending** — Clusters 0, 1, and 3 are all parent-heavy and all spend a fraction of Cluster 2. This is a household economics constraint, not a marketing problem.
- **High web visits without purchases signals price sensitivity, not disengagement** — Clusters 1 and 3 have the highest web visits per month but the lowest spend. They need savings-forward messaging at the point of browsing, not re-engagement campaigns.
- **Campaign responsiveness is concentrated in Cluster 2** — they accept nearly 4x more promotions than any other group. Blanket campaigns are largely wasted on the remaining three segments.
- **Recency is not a useful targeting signal** — all four clusters return at nearly the same cadence (around 49 days). Cluster membership is a far richer variable for campaign planning than recency alone.

---

## Business Recommendations

1. **Prioritise Cluster 2** for premium campaigns, catalog investment, and in-store experiences. This is where marketing spend returns the most.
2. **Shift Clusters 1 and 3 to low-cost digital tactics** such as deal banners, cart recovery emails, and value-led flyers rather than broad campaign spend.
3. **Use Cluster 0 as an upsell target.** They have the income and shopping habits to spend more. Loyalty rewards and premium product recommendations are a realistic path to a higher basket size.
4. **Stop distributing catalogs to Clusters 1 and 3.** Catalog purchase rates are near zero for these segments. Reallocate that budget toward digital retargeting for them and more catalog investment for Cluster 2.
5. **Retire recency as a primary targeting signal** and replace it with cluster membership for all future campaign planning.
