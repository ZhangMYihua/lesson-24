A selector is a function that accepts Redux state as an argument and returns data that is derived from that state. Selectors can provide performance optimizations to your application and can also help you encapsulate your global state tree
Two types of selectors

1st is called input selector that doesnt use create slector 
  function that gets whole state and returns a slice of it
    one layer deep usually

2nd output selector that does create selector and input selctors to build themselves
  createSelector takes to