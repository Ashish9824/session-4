# session-4

### Task 1: `calculateTotal` Function

```javascript
function calculateTotal(itemPrice, quantity) {
    // Arithmetic operator (*) calculates the total bill
    return itemPrice * quantity;
}

// Example usage:
const price = 450;
const qty = 3;
console.log(`Total Bill: ₹${calculateTotal(price, qty)}`); // Total Bill: ₹1350

```

---

### Task 2: Flipkart-Style Discount Calculator

```javascript
function calculateFlipkartPrice(productPrice, discountPercentage, isMember) {
    // Step 1: Calculate initial discount
    let discountAmount = (productPrice * discountPercentage) / 100;
    let priceAfterDiscount = productPrice - discountAmount;

    // Step 2: Logical check for Flipkart Plus / VIP membership
    if (isMember) {
        // Apply extra 5% discount on the remaining price
        let extraDiscount = (priceAfterDiscount * 5) / 100;
        priceAfterDiscount -= extraDiscount;
    }

    return priceAfterDiscount;
}

// Example usage:
const price = 2000;
const standardDiscount = 10; // 10% base discount

console.log("Non-member price: ₹" + calculateFlipkartPrice(price, standardDiscount, false)); // ₹1800
console.log("Member price (Extra 5% off): ₹" + calculateFlipkartPrice(price, standardDiscount, true));  // ₹1710

```

---

### Task 3: `isEligibleForOffer` Function

```javascript
function isEligibleForOffer(age, orderValue) {
    // Relational operators (>=, >) combined with the Logical AND operator (&&)
    return age >= 18 && orderValue > 500;
}

// Example usage:
console.log(isEligibleForOffer(20, 650)); // true  (Age >= 18 AND Order > 500)
console.log(isEligibleForOffer(16, 800)); // false (Under 18)
console.log(isEligibleForOffer(22, 450)); // false (Order value not above 500)

```

---

### Task 4: Instagram Trending Post Checker

The logical AND (`&&`) operator has higher precedence than the logical OR (`||`) operator. The condition evaluates whether the post has at least 1,000 likes, **OR** both more than 200 comments and at least 50 shares:

```javascript
let likes = 850;
let comments = 250;
let shares = 60;

// Evaluation: (likes >= 1000) || ((comments > 200) && (shares >= 50))
let isTrending = (likes >= 1000) || (comments > 200 && shares >= 50);

if (isTrending) {
    console.log("The post is Trending! 🔥");
} else {
    console.log("The post is not trending yet.");
}

```

---

### Task 5: Pre-Increment vs Post-Increment

* **Pre-increment (`++count`)**: Increments the variable first, then evaluates/returns the new value.
* **Post-increment (`count++`)**: Evaluates/returns the current value first, then increments the variable.

```javascript
let followerCount = 100;

console.log("--- Initial Value ---");
console.log("Starting followerCount:", followerCount); // 100

// 1. Post-increment demonstration
console.log("\n--- Post-Increment (followerCount++) ---");
console.log("Value returned during count++ :", followerCount++); // Logs 100 (returns first, then increments)
console.log("Value after post-increment     :", followerCount);   // Logs 101

// 2. Pre-increment demonstration
console.log("\n--- Pre-Increment (++followerCount) ---");
console.log("Value returned during ++count :", ++followerCount); // Logs 102 (increments first, then returns)
console.log("Value after pre-increment      :", followerCount);   // Logs 102

```
