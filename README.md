# GAME_Guess-My-Number

## Table of contents
* [General info](#general-info)
* [Screenshots](#screenshots)
* [Technologies](#technologies)
* [Contact](#contact)

## General info
Projekt wykonany w ramach kursu udemy.
Opis: Gra znajdz ukrytą liczbę.
Należy znaleść liczbę od 1-20 !!!
Spróbuj !!!

## Screenshots
![Example screenshot](./src/image/project_3.jpg)

## Technologies

   * HTML 5
   * CSS 3
   * Sass
   * JavaScript

## Code Examples

"use strict";

document.querySelector(".check").addEventListener("click", function () {
  const guess = Number(document.querySelector(".guess").value);

  if (!guess) {
    // document.querySelector('.message').textContent = ` No number !`;
    displayMessage(`⛔️ No number ! `);
  } else if (guess === secretNumber) {
    // document.querySelector('.message').textContent = ` Correct number !`;
    displayMessage(`Correct number !`);
    document.querySelector(".number").textContent = secretNumber;
    document.querySelector("body").style.backgroundColor = "#60b347";
    document.querySelector(".number").style.width = "30rem";
    if (score > highScore) {
      highScore = score;
      document.querySelector(".highscore").textContent = highScore;
    }
  } else if (guess !== secretNumber) {
    if (score > 1) {
      displayMessage(guess > secretNumber ? "🔺 Too high!" : " 🔻 Too low!");
      score--;
      document.querySelector(".score").textContent = score;
    } else {
      displayMessage("💥 You lost the game!");
      document.querySelector(".score").textContent = 0;
    }
  }
});


## Contact
Created by me - feel free to contact me!
