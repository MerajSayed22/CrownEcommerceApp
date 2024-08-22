Crown Clothing E-commerce App \n
Crown Clothing is a fully responsive e-commerce web application built using React.js. The app allows users to browse and purchase various clothing items, manage their shopping cart, and securely process payments via Stripe. The application is styled using SCSS to provide a modern and clean user interface.

Features
Browse Products: Users can view clothing items categorized by types.
Add to Cart: Add items to the cart and adjust quantities.
Checkout: Secure payment processing using the Stripe Payment Gateway.
User Authentication: Sign up and log in with email and password or Google account.
Responsive Design: The app is fully responsive, providing a seamless experience across devices.
State Management: Managed using Redux for better performance and scalability.
Tech Stack
Frontend: React.js
Styling: SCSS (Sass)
State Management: Redux
Routing: React Router
Forms: React Hook Form
Payment Gateway: Stripe API
Getting Started
Follow the instructions below to set up the project locally.

Prerequisites
Ensure you have the following installed:

Node.js (v14 or later)
npm or yarn for managing dependencies
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/MerajSayed22/CrownEcommerceApp.git
cd CrownEcommerceApp
Install dependencies:

Using npm:

bash
Copy code
npm install
Or using yarn:

bash
Copy code
yarn install
Set up environment variables:

Create a .env file in the root directory and add your Stripe keys:

env
Copy code
REACT_APP_STRIPE_PUBLIC_KEY=your_stripe_public_key
Run the development server:

Using npm:

bash
Copy code
npm start
Or using yarn:

bash
Copy code
yarn start
The app should be running on http://localhost:3000.

Available Scripts
npm start: Runs the app in development mode.
npm build: Builds the app for production.
npm test: Runs the test suite.
Project Structure
bash
Copy code
CrownEcommerceApp/
├── public/
├── src/
│   ├── assets/               # Images and fonts
│   ├── components/           # Reusable components (e.g., buttons, cards)
│   ├── pages/                # Pages for each route (e.g., homepage, shop, checkout)
│   ├── redux/                # Redux-related files (actions, reducers, store)
│   ├── scss/                 # SCSS files for styling
│   ├── App.jsx               # Main app component
│   ├── index.js              # Entry point of the application
├── .env                      # Environment variables for Stripe API
├── .gitignore
├── package.json
├── README.md
Stripe Integration
This app uses the Stripe API to handle payments. To integrate Stripe:

Sign up for a Stripe account here.
Retrieve your public and secret API keys from the Stripe dashboard.
Set up the Stripe public key in your .env file as mentioned above.
Use react-stripe-js to handle secure payment processing.
Example Code for Stripe Integration
javascript
Copy code
import { loadStripe } from '@stripe/stripe-js';
import { Elements } from '@stripe/react-stripe-js';
import CheckoutForm from './components/CheckoutForm';

// Load Stripe public key
const stripePromise = loadStripe(process.env.REACT_APP_STRIPE_PUBLIC_KEY);

function App() {
  return (
    <Elements stripe={stripePromise}>
      <CheckoutForm />
    </Elements>
  );
}

export default App;
SCSS Styling
The project is styled using SCSS to organize styles efficiently with the use of variables, mixins, and nesting. You can find the SCSS files inside the src/scss/ directory.

To add new SCSS styles, import them into the corresponding components or global styles.

Example SCSS Structure
bash
Copy code
src/scss/
├── base/         # Base styles (e.g., typography, resets)
├── components/   # Component-specific styles
├── pages/        # Page-specific styles
├── variables.scss # SCSS variables (e.g., colors, fonts)
Example SCSS Code
scss
Copy code
// src/scss/variables.scss
$primary-color: #4a90e2;

body {
  background-color: $primary-color;
  font-family: 'Open Sans', sans-serif;
}
Contributing
Fork the repository
Create a new feature branch (git checkout -b feature/feature-name)
Commit your changes (git commit -m 'Add feature')
Push to the branch (git push origin feature/feature-name)
Open a pull request
License
This project is licensed under the MIT License - see the LICENSE file for details.
