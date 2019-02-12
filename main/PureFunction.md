## Pure function

**Definition**: Pure function is a function which given the same input , will always return the same output and produce no side effects
Examples:

    const addToCart = (cart, item, quantity) => {
    	return {
    		...cart,
    		items: cart.items.concat([{
    			item,
    			quantity
    		}])
    	};
    }
    const originalCart = {
	    items: []
    };
 

    const newCart = addToCart(
	    originalCart,
	    {
		    name: "Digital SLR Camera",
		    price: '1495'
	    },
	    1
    );
    
**Conclusion**:
*A pure function* is functiion which given the same state, always return the same output, and has no side-effects.

***Pure function* *is the simpliest kind of function***. You should prefer them whenever they are practical. They are deterministic, which makes them easy to understand, debug, and test, Determinism also makes them immune to entire class of bugs dealing with shared mutable state, side effects, race conditions, so on.

An expression is ***referrentially  transparent*** if you can replace the expression with its corresponding value without changing the meaning of the program.

***Pure functions*** can be used to optimize software performance. For instance, rendering a view is often an expensive operation, which can be skipped if the data underlying the view has not changed. When pure function are used for view state updates, you can check to see whether or not a view should be rerendered by comparing the previous state to the new state. 
