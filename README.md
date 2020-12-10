# Guess the capital game

## How to start

Create your React project using: `npx create-react-app todo`.

Change to your app directory with `cd` and run your project with `npm start`


## 1. Preparing the game

In the App.js, you need to call the countries api: https://restcountries.eu/rest/v2/all and store it in your state, you could do that in `componentDidMount`.
As you will see it is an array of different objects. Each object contain the country properties, later on we will use the name and capital properties.
You should create another component: `Game` and send as props what you have stored there.

## Bonus!

If you scroll a bit on this API response, you might notice that there are some countries without a capital. This could lead to errors later on our application. Think of a logic to *filter* those countries without a capital before storing them in our state

## 2. Set up a landing page for the game

In your Game.js component, you need to show:
  - A section with some text about the game logic.
  - A button to start the game

  > **HINT**: You can use the component state to store a property named gameStatus that will contain at what state your game is: 'start', 'playing' or 'finished'.

## 3. Rendering some countries and capitals

Since you receive an array of countries with capitals, you should think of a logic to display a name of a country and 4 different capitals (one needs to be correct). Something like this:

![ToDo](https://i.imgur.com/9eEiBes.png)

  > **HINT**: This could be shown in your 'playing' state.

## 4. Create the game logic

Next step should be what will happen if the user guess right or wrong.
Again it is up to you, personally my approach was that if the user guess right it will move to the next one and if he guess wrong, nothing happens (yet, later that user will be loosing points or time).
So the only option to move forward is to guess the capital.

  > **HINT**: You should create a onClick method for each capital and control on that onClick if the selected option is equal to the correct one.



## 5. Create the game over condition

At this point, you should be able to go to the next set of country and capitals if you guess the capital so we need to create a condition to finish that game. Feel free to use any idea, here you have 3 options:

### Game over option 1: Number of turns played

You can control how many capitals the user has guessed and show a `game over` section when that user reaches a certain number.
i.e. You can play with 15 countries, at number 15 you will get to that end of the game screen


### Game over option 2: Add points and turns system

You could implement a point system where each guess of the user will come with some points.
If the user guess right the capital, you could some points and if he doesn't you can decrease those points.

You could create a game over condition that the user needs to reach X amount of points and in that game over screen, you will show how many turns were needed.


### Game over option 3: Countdown system

You could implement a countdown timer that will start when the game starts. At the beginning you have X seconds and you can play until this timer gets to 0 seconds.
You can also add points and even add or decrease seconds if the user gets a wrong capital

## Play again option

At the end, you can add in that game over screen the option to play again. This should reset all points, counters, etc that the user had and show the `playing` mode again.
