### How to write code

#### 1. Never repeat your code
When some code appears in multiple places, try to make it shareable. It's very important to make a change instantly by modifying single place instead of modifying multiple places, and this will reduce the chance of bugs from omitted change. It applies not only to code but also to variables for colors or attributes. To make the code shareable, you can use many approches such as function, [closure/higher order function](https://levelup.gitconnected.com/closures-first-class-and-higher-order-functions-2dc97dc89cd8) or [HOC](https://reactjs.org/docs/higher-order-components.html) for react components.

#### 2. Understand the task before write code
You should understand what the task is about and what should you do. Many developers start to write code without understanding of them. Especially try to understand the task from the user's perspective. It will help you to understand context better in the project level.

#### 3. Make code short as much as you can
Try to make code short. It will help other developers working together to easily understand the code you wrote. Modulerize your code with functions or class method even though it's used in single place. It will improve the readablity of your code.

##### Before
```javascript
const customer = new Person();

const productsSorted = products.sort(
  (product1, product2) =>
    product1.value / product1.price - product2.value / product2.price
);

var bestProduct;

if (productsSorted.length > 0) {
  bestProduct = productsSorted[0];
} else {
  throw new Error("No product found");
}

customer.balance -= bestProduct.price;
customer.purchasedProducts = [...customer.purchasedProducts, bestProduct];
```

##### Refactored
```javascript

const customer = new Person();

const bestProduct = customer.getBestProduct(products);

if (bestProduct) {
  customer.purchase(bestProduct)
} else {
  throw new Error("No product found");
}
```

#### 4. Test, test and test
Don't keep the bugs which anyone can find with a single try. It makes you less reliable as a developer as well as the team. Any change you've made can lead unexpected bug so you should have a test at least once for the core functionalities even if you didn't make a change for them. Writing test script for the core functionalities is good way to prevent potential bug from the change.
