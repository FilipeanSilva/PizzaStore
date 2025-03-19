# Pizza Restaurant - Vue.js

A simple pizza ordering application built using **Vue.js**. This project allows users to browse a menu of pizzas, add them to a shopping cart, update the quantities, and see the total price dynamically.

## Features
- 📜 **Dynamic Menu**: Displays a list of pizzas with names, prices, and images.
- 🛒 **Shopping Cart**: Users can add, remove, and update pizza quantities.
- 💰 **Live Price Calculation**: The total cost updates automatically.
- 🎨 **Styled UI**: Uses Bootstrap for layout and a custom CSS design.
- 🚀 **Vue.js Reactive Data**: Efficient state management with Vue.

## Technologies Used
- **Vue.js 3**
- **HTML5 & CSS3**
- **JavaScript (ES6+)**
- **Bootstrap 5**


## Installation & Setup
Since this project is built using Vue.js, no installation is required. Simply clone the repository and open `index.html` in your browser.

```sh
# Clone the repository
$ git clone git@github.com:FilipeanSilva/PizzaStore.git
$ cd pizza-vue-app

# Open index.html in your browser
```

## Usage
1. Open the **Pizza Restaurant** page.
2. Browse the menu and click "Add to Cart" on any pizza.
3. Modify the quantities using `+` and `-` buttons in the cart.
4. The total price updates automatically.

## Vue.js Code Breakdown
### Data Properties
```javascript
data() {
  return {
    menu: [...], // List of pizzas
    cart: [], // Stores selected pizzas
  };
}
```

### Methods
- `addPizza(id)`: Adds a pizza to the cart or increases its quantity.
- `reduceItem(id)`: Decreases the quantity or removes the pizza.
- `getTotalPrice()`: Computes the total cart price dynamically.

### Example Vue.js Integration
```html
<div v-for="item in menu" :key="item.id">
  <h5>{{ item.name }}</h5>
  <button @click="addPizza(item.id)">Add to Cart</button>
</div>
```