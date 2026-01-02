**Explanation of the Model**

**Preprocessing**
Before the models could work, we had to "translate" the data. Computers don't know what "Fiber Optic" or "Month-to-Month" means. We converted these into 1s and 0s. We also "scaled" the data—this ensures that a large number like $2,000 in Total Charges doesn't drown out a small but important number like 2 months of Tenure.

**The Two Competitors (The Models)**
**Random Forest (The Committee): **This model acts like a committee of 100 experts. Each expert looks at a small piece of the data and votes on whether a customer will stay or leave. "Top Drivers" (The Results) When we look at the Feature Importance from the first model, here is what the model discovered about the customers:

The "Weight" of the Contract: The model found that the type of contract is the strongest signal. It learned that a "Month-to-Month" tag is essentially a "Ready to Leave" tag.

The Tenure "Gravity": The model sees that as time goes on, a customer gets "heavier" and harder to move. It identifies that the lack of history (low tenure) makes a customer very "light" and easy for a competitor to blow away.

**Price Thresholds: **The model isn't just looking at the bill; it's looking for the "breaking point." It found that once the bill crosses a certain threshold (around $70), the risk of churn doesn't just go up—it doubles.It is very accurate because it captures complex, hidden patterns.

**Logistic Regression (The Straight-Talker):** This model looks for direct, linear relationships. It’s like a math formula that says, "For every $10 increase in the bill, the chance of leaving goes up by X%." It is simpler but very reliable.

(The Outcome) The Balancing Scale: Imagine a scale. On one side, we pile up the "Risk" weights (High bills, Month-to-month contract). On the other side, we pile up the "Loyalty" weights (Long tenure, Tech support, Two-year contract).

The 50% Line: If the "Risk" side is heavier, the customer's score crosses the 0.5 (50%) threshold, and the model flags them as "Yes" (Churn).

The Probability Score: What makes this model great for Power BI is that it doesn't just say "Yes" or "No." It tells us exactly how "heavy" the risk side is (e.g., "This customer has a 72% probability of leaving").

**The Comparison Chart (The ROC Curve)**
This graph tells us how good the models are at their job.

The Curve: Think of the top-left corner as the "Perfect Prediction" zone. The closer the lines are to that corner, the more accurate the model is.

The AUC Score: This is the grade out of 1.0. A score of 0.85 (like what you likely see) means the model is making highly informed predictions, significantly better than just guessing.

