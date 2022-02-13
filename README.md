# Amazona ECommerce Website

1. Introduction to this course
   1. what you will build
   2. what you will learn
   3. who are audiences
2. Install Tools
   1. Code Editor
   2. Web Browser
   3. VS Code Extension
3. Website Template
   1. Create amazona folder
   2. create template folder
   3. create index.html
   4. add default HTML code
   5. link to style.css
   6. create header, main and footer
   7. style elements
4. Display Products
   1. create products div
   2. add product attributes
   3. add link, image, name and price
5. Create React App
   1. npx create-react-app frontend
   2. npm start
   3. Remove unused files
   4. copy index.html content to App.js
   5. copy style.css content to index.css
   6. replace class with className
6. Create Rating and Product Component

   1. create components/Rating.js
   2. create div.rating
   3. style div.rating, span and last span
   4. Use Rating component

7. Build Product Screen

   1. Install react-router-dom
   2. Use BrowserRouter and Route for Home Screen
   3. Create Homescreen.js
   4. Add product list code there
   5. create ProductScreen.js
   6. Add new route from product details to App.js
   7. Create 3 columns for product image, info and acation

8. Create Node.js Server

   1. run npm init in root folder
   2. Update package.json set type:module
   3. Add .js to imports
   4. npm install express
   5. create server.js
   6. add start command as node backend/server.js
   7. require express
   8. create route for / return backend is ready
   9. move product.js from frontend to backend
   10. create route for /api/products
   11. return products
   12. run npm start

9. Load Products from Backend

   1. edit HomeScreen.js
   2. define products, loading and error
   3. create useEffect
   4. define async fetchData and call it
   5. install axios
   6. get data from /api/products
   7. show them in the list
   8. create Loading Component
   9. create Message Box Component
   10. use them in HomeScreen

10. Install ESLint for Code linking

    1. Install VScode eslint extension
    2. npm install -D eslint
    3. run ./node_modules/.bin/eslint --init
    4. Create ./frontend/.env
    5. Add SKIP_PREFLIGHT_CHECK=true

11. Add Redux to HomeScreen

    1. npm install redux react-redux
    2. Create store.js
    3. initState = {products:[]}
    4. reducer = {state, action} => switch LOAD_PRODUCTS: {products: action.payload}
    5. export default createStore(reducer, initState)
    6. Edit HomeScreen.js
    7. shopName = useSelector(state=>state.products)
    8. const dispatch = useDispatch()
    9. useEffect(()=>dispatch({type:LOAD_PRODUCTS, payload:}))
       10.Add store to index.js

12. Add redux to Product Screen

    1. create product details constants, actions and reducers
    2. add reducer to store.js
    3. use action in ProductScreen.js
    4. add /api/product/:id to backend api

13. Handle Add to Cart Button

    1. Handle Add to Cart in ProductScreen.js
    2. create CartScreen.js

14. Implement Add to Cart Action

    1. create addToCart constants, actions and reducers
    2. add reducer to store.js
    3. use action in CartScreen.js
    4. render cartItems.length

15. Build Cart Screen

    1. create 2 columns for cart items and cart actions
    2. cartItems.length === 0? cart is empty
    3. show item image, name, qty and price
    4. Proceed to checkout button

16. Implement Remove From Cart Action

    1. create removeFromCart constants, actions and reducers
    2. add reducer to store.js
    3. use action in CartScreen.js

17. Connect MongoDB

    1. npm install mongoose
    2. connect to mongodb
    3. create config.js
    4. npm install dotenv
    5. export MONGODB_URL
    6. create models/userModel.js
    7. create userSchema and userModel
    8. create models/productModel.js
    9. create productSchema and productModel
    10. create userRoute
    11. Send sample data

18. Create Sign-in backend

    1. create /signin api
    2. check email and password
    3. generate token
    4. install json web token
    5. install dotenv
    6. return token and data
    7. test it using postman

19. Design SignIn Screen

    1. create SigninScreen
    2. render email and password fields
    3. create signin constants, actions and reducers
    4. Update Header based on user login

20. Create Sample Products In MongoDB

    1. create models/productModel.js
    2. create productSchema and productModel
    3. create productRoute
    4. Seed sample data

21. Implement SignIn Action

    1. create signin constants, actions and reducers
    2. add reducer to store.js
    3. use action in SigninScreen.js

22. Create Register Screen

    1. create API for /api/users/register
    2. insert new user to database
    3. return user info and token
    4. create RegisterScreen
    5. Add fields
    6. Style fields
    7. Add screen to App.js
    8. create register action and reducer
    9. check validation and create user

23. Create Shipping Screen

    1. create CheckoutSteps.js component
    2. create shipping fields
    3. implement shipping constant, actions and reducers

24. Create Payment Screen

    1. create payment fields
    2. implement shipping constant, actions and reducers

25. Design Place Order Screen

    1. design order summary fields
    2. design order action

26. Create Place Order API

    1. createOrder api
    2. create orderModel
    3. create orderRouter
    4. create post order route

27. Implement PlaceOrder Action

    1. handle place order button click
    2. create place order constants, action and reducer

28. Create Order Screen

    1. build order api for /api/orders/:id
    2. create OrderScreen.js
    3. dispatch order details action in useEffect
    4. load data with useSelector
    5. show data like place order screen
    6. create order details constant, action and reducer

29. Add PayPal Button

    1. get client id from paypal
    2. set it in .env file
    3. create route form /api/paypal/clientId
    4. create getPaypalClientID in api.js
    5. add paypal checkout script in OrderScreen.js
    6. show paypal button

30. Implement Order Payment

    1. update order after payment
    2. create payOrder in api.js
    3. create route for /:id/pay in orderRouter.js
    4. rerender after pay order

31. Display User Profile

    1. create user details api
    2. show user information

32. Display Orders History

    1. create customer orders api
    2. create api for getMyOrders
    3. show orders in profile screen
    4. style orders

33. Update User Profile

    1. create user update api
    2. update user info

34. Create Admin View

    1. Create Admin Menu
    2. Create Admin Middleware in Backend
    3. Create Admin Route in Frontend

35. List Products

    1. Create Product List Screen
    2. Add reducer to store
    3. show products on the screen

36. Create Product

    1. build create product api
    2. build Create Product button
    3. define product create constant, action and reducer
    4. use action in Product List Screen

37. Build Product Edit Screen
    1. create edit screen
    2. define state
    3. create fields
    4. load product details
    5. add to routes
38. Update Product

    1. define update api
    2. define product update constant, action and reducer
    3. use action in Product Edit Screen

39. Upload Product Image

    1. npm install multer
    2. define upload router
    3. create uploads folder
    4. Handle frontend

40. Delete Product

    1. create delete api in backend
    2. create delete constants, action and reducer
    3. use it in product list screen

41. Delete Order

    1. create delete order action and reducer
    2. add order delete action to order list

42. Deliver Order

    1. create constant, actions and reducers for deliver order
    2. add order deliver action to order details screen

43. Implement Live Chat With Customers
    1. use socket io to create backend
    2. create chat box component
    3. create support screen
