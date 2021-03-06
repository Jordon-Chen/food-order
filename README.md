# food-order

A react-based app to order food online.

Usage:

User can order the amount of food they want in the menu and check out their order in the cart.

Demo: [http://jordon-chen.github.io/food-order](http://jordon-chen.github.io/food-order)

### Installation

```
npm install
npm start
```

Learning: [useRef](https://reactjs.org/docs/hooks-reference.html#useref), [React.forwardRef()](https://reactjs.org/docs/forwarding-refs.html), [React Context](https://reactjs.org/docs/context.html), [array.reduce()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce), [useReducer](https://reactjs.org/docs/hooks-reference.html#usereducer), [array.filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter), [useEffect](https://reactjs.org/docs/hooks-reference.html#useeffect), [useState](https://reactjs.org/docs/hooks-reference.html#usestate)

Implementation:

- This app consists of 4 components: UI, Layout, Meals, and Cart.
- In the UI folder, we customize our Input, Card, and Modal components.
- In the Layout folder, we set up the header, cart button, and the main image.
- In the Meals folder, we create mealItem, display mealItems, and create a form to add mealItem.
- When getting value from the custom Input component, we use `useRef` and `React.forwardRef()` to do so.
- In the Cart folder, we create a modal to show the cart, use `React Context` to manage the cart, and listing all meals in the cart.
- If it is preferred to show the amount of all meals instead of the number of kinds of meals, use `array.reduce()` to do that. For example, if 2 spaghetti and 3 burger are in the cart, we want to show "5" meals instead of "2" meals.
- Before adding meal to the cart, make sure to confirm that whether the item has been added to cart. If the item has been in the cart, add the amount to that item instead of adding a whole new item to the cart.
- Before removing meal from the cart, make sure to confirm that whether the item is the last one in the cart. If the item is the last one in the cart, remove the whole item from the cart instead of subtract the amount directly.
- In applying complex logic to the items in the cart, `useReducer` is a great Hook to do so.
- When removing item from the cart, `array.filter()` is a good way to keep the meals we want.
- When applying bump animation to the cart button, use `useEffect` and `useState` to manage the animation css class to the button.
