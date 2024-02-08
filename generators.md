### Generators
Depth-first (preorder) search of a binary tree
```javascript
function binaryTreeNode(value) {
  let node = { value }
  node[Symbol.iterator] = function* depthFirst() {
    yield node.value;
    if (node.leftChild) yield* node.leftChild;
    if (node.rightChild) yield* node.rightChild;
  }
  return node;
}
```

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
