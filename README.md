# Tech-Ed

## Review the student's submission

(Optionally) Launch a dev server to run the code within ./src by running npm run start

## Given the following problem statements from the student, what would you say to advise them?

"When I add items to my cart, everything works. Then if I goto the cart page the cart is empty"

- It looks like the cart functions don't have access to the state. This could be because it isn't created by a global variable or a class.
- On further investigation, it looks like cart items are not being stored in local storage correctly. It is displaying as undefined in application console > local storage.
- I would advise them to check the data flow. Is the item being add and collected from storage properly?

## Have best practices been followed?

- Variable names (in cart.js > showCart ()) haven't been named anything relatable which makes it harder to understand.
- in the App.js > generateCatalog function, the variables could be const instead of let.
- All comments should be removed from code, once it's finished.
- Using tbody as an id is bad practice (in cart.html)

## What would you recommend they do to extend this?

- Displaying pictures with the items.
- I would look at other popular website carts (e.g Amazon) and check what functionalities they have:

  > recommended items that other people have bought,
  >
  > editing quantity option
  >
  > save for later

- accessability compliance
- implement with more advanced tech like React, CSS compiler

## Are you able to identify any issues with the codebase?

- It hasn’t got any styles, the style.css file is empty
- Drop-down resets on add to basket. This seems to be because event.target.reset is being called.
- Quantity isn't required. Maybe one should be the default, if the quantity isn't provided.
- Cart doesn't presist between pages.
- Page resets on press of Home button.
- You can add negative quantities.
- In cart.removeItem splice's first argument should be the index, not the item.
- In cart.js the showCart function appends the TR before the TD, although I'm not sure if it makes much difference.
- cart.html + index.html has more than 1 h1 element.
- cart.html + index.html has more than 1 header element.
- Having empty tfoot is unnecessary in cart.html.

## Wireframe for component build

![wireframe](/Wireframe.jpg)
