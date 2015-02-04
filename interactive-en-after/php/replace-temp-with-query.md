Let's look at <i>Replace Temp with Query</i> using a simple method as an example.

Replace the variables <code>basePrice</code> and <code>discountFactor</code> one by one with calls to the respective methods.

First make sure that the variables are assigned a value within the method only once.

This is all true in our case, so we can continue.

For the second step, we create a <code>basePrice()</code> method and move the expression forming the <code>basePrice</code> variable to it.

Now we can use a method call instead of the initial expression. Thus we now have a new method and all of the old code still works.

This is the perfect time to replace the variable with a direct method call.

Replace the first variable and then run autotests to make sure that nothing is broken.

Let's start testing.

Perform the following replacement.

Let's start testing.

The previous replacement was the last one, so we can remove the variable declaration.

All is done with the first variable. We can repeat all this to extract <code>discountFactor</code>.

Create a new method…

...use it to initialize the variable and remove old code...

Note how difficult it would have been to extract <code>discountFactor</code> if we had not first replaced <code>basePrice</code> with a method call.

Ultimately the <code>getPrice()</code> method comes to look as follows.

Let's perform the final testing.

The refactoring is complete! You can compare the old and new code if you like.