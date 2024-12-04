Task:
    - Modeling customers’ fit feedback and Give the Fit feed back prediction.

Possible challenge:
    - resolve label imbalance issues
    - subtle user fit semantics

Body-related features:
    bust size (converted into numerical values for cup size and band size)
    weight (converted to numerical)
    height (converted to numerical, e.g., 5'8" → 68 inches)
    body type (encoded as categorical variables)

item-related features:

    item_id (categorical encoding to represent items uniquely)
    category (encoded categorically)
    size (numerical size of the item rented)

User context features:
    age (numerical)
    rented for (categorical encoding, e.g., vacation, party)

Review context:
    rating (numerical)
