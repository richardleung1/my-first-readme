# My-First-README

Repo explaining readme

## Steps to Install on local computer
1. Go to [repo](https://github.com/SEI-ATL/tic-tac-toe) on Github profile
2. `fork` and `clone` repo
3. Clone to local machine
```text
git clone
```
4. Go to `tic-tac-toe` directory
5. Open `index.html` in browser
```text
open index.html
```

```javascript
elements.forEach(element => {
    element.addEventListener('click', eachMove, { once: true})
});


function eachMove(event) {
    let spot = event.target;
    let currentTurn = playerTurn ? "O": "X";
    spot.innerHTML = currentTurn;
    checkWin();
    swapTurns();
    checkDraw();
}

function swapTurns () {
    playerTurn = !playerTurn;
}

function checkWin() {
    if (one === two && two === three && three !== '') {
        winMessage();
    } else if (four === five && five === six && six !== '') {
        winMessage();
    } else if (seven === eight && eight === nine && nine !== '') {
        winMessage();
    } else if (one === four && four === seven && seven !== ''){
        winMessage();
    } else if (two === five && five === eight && eight !== ''){
        winMessage();
    } else if (three === six && six === nine && nine !== '') {
        winMessage();
    } else if (one === five && five === nine && nine !== '') {
        winMessage();
    } else if (three === five && five === seven && seven !== '') {
        winMessage();
    }
}

function checkDraw() {
    moves++;
    if (moves === 9) {
        alert('This game is a draw.')
    }
}

function winMessage() {
    if (playerTurn) {
        alert('X is the winner!')
    } else {
        alert('O is the winner!')
    }
};
```


```css
body {
  text-align: center;
  margin: 0;
}

.board {
  width: 100vw;
  height: 50vh;
  display: grid;
  justify-content: center;
  justify-items: center;
  align-content: center;
  align-items: center;
  grid-template-columns: repeat(3, auto);
}

.spot {
  width: 100px;
  height: 100px;
  border: 2px solid black;
  font-size: 90px;
}
```


```html
<h1>Welcome to Tic Tac Toe</h1>
<div class="board" id="board">
  <div class="spot" id="1"></div>
  <div class="spot" id="2"></div>
  <div class="spot" id="3"></div>
  <div class="spot" id="4"></div>
  <div class="spot" id="5"></div>
  <div class="spot" id="6"></div>
  <div class="spot" id="7"></div>
  <div class="spot" id="8"></div>
  <div class="spot" id="9"></div>
</div>
<button type="reset">Reset</button>
```


| functions | Description |
| ----------- | ----------- |
| eachMove() | call functions every move |
| swapTurn() | changes the boolean value to change turns |
| checkWin() | check if a player has won every move |
| checkDraw() | check if the game is a draw |
| winMessage() | display alert message if a player has won |
