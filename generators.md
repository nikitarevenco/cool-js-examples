### Generators
Outputs all 52 cards of a deck of cards with their respective symbol.
```javascript
cardDeck = ({
  suits: ['♣️', '♦️', '♥️', '♠️'],
  court: ['J', 'Q', 'K', 'A'],
  [Symbol.iterator]: function* () {
    for (let suit of this.suits() {
      for (let i = 2; i <= 10; i++) yield suit + i;
      for (let c of this.court) yield suit + c;
    }
  }
})
```
