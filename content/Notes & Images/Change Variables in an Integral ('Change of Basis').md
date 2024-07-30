#TODO Pasted from ChatGPT

To change variables in an integral, you can use a technique called variable substitution or change of variables. The idea is to replace the original variable of integration with a new variable to simplify the integral. Here are the general steps:

1. **Choose a New Variable**: Select a new variable to replace the original variable in the integral. The choice of the new variable should be based on making the integral easier to work with. Common choices include \(u\), \(t\), \(s\), or any other letter you prefer.

2. **Determine the Relationship**: Find a relationship between the new variable and the original variable. This relationship is often expressed as \(u = g(x)\), where \(u\) is the new variable, and \(g(x)\) is a function of the original variable \(x\). This function should be chosen so that it simplifies the integral.

3. **Calculate the Differentials**: Compute the differential \(du\) in terms of the new variable \(u\). This is done using the chain rule:

   \[
   du = g'(x) \, dx
   \]

4. **Change the Limits**: If you are dealing with definite integrals, also change the limits of integration from the original variable to the new variable. This step is crucial when changing variables.

5. **Substitute**: Substitute the new variable \(u\) and its corresponding differential \(du\) into the integral.

6. **Simplify and Integrate**: After substitution, you should have a new integral in terms of the new variable \(u\). Simplify the integrand as much as possible. Then, integrate with respect to \(u\).

7. **Change Back (if necessary)**: If you want the final result in terms of the original variable, use the relationship \(u = g(x)\) to change back to the original variable after integrating.

Here's a simple example to illustrate the process:

Original Integral: \(\int x e^{x^2} \, dx\)

1. Choose a New Variable: Let \(u = x^2\).

2. Determine the Relationship: \(u = g(x) = x^2\).

3. Calculate the Differentials: \(du = 2x \, dx\).

4. Change the Limits: Not applicable for this indefinite integral.

5. Substitute: Replace \(x^2\) with \(u\) and \(dx\) with \(\frac{du}{2x}\):

   \(\int e^u \frac{1}{2x} \, du\)

6. Simplify and Integrate: The integral becomes \(\frac{1}{2} \int \frac{e^u}{x} \, du\).

7. Change Back (if necessary): If you want the result in terms of \(x\), you can use the original relationship \(u = x^2\) to replace \(u\) with \(x^2\) in the final answer.

Remember that the choice of the new variable and the relationship \(u = g(x)\) is crucial for simplifying the integral effectively.