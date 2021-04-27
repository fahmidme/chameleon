# Chameleon Frontend Test

To run the project, download this repository, install the node modules, and run `yarn start`.

## Question Answers

### How are you today? 😊

I am doing good. Thank you for asking.

### 1. Please fix any obvious issues you see with the dropdown.

1. I was wielding my coding magic wand trying to calm a storm, and then realized the problem with the `constructor` bug was only that the spelling was wrong.

2. For this dropdown to be used in any practical setting, `export default ExampleNav` had to be stated.

3. The render function for the `DropdownItem` class had to have a return statement.

4. For the `toggle` function to work properly, it had to be binded to the class.

5. The dropdown item children had to have a conditional statement to make sure it is only shown when it is open.

6. The toggle function had to set the new value based on negation of the old value.

### 4. If we wanted to sync this dropdown selection to the server with app.sync('PATCH', 'user', { dropdown_1_state: {true,false} }) where would this be included?

It depends. We can put it inside the toggle function. Making it asynchronous should be considered, as it will keep the user experience seamless.

### 5. If we wanted to pass children (like this example) OR a Promise that resolves to an array of items what changes should be made? (just a sentence or two or some code is ok).

This also depends, especially on the use case of the children. Any references to the props should be addressed using `this.props...`. In the case of accessing the label for example, it can be done in parts of the code using `this.props.label`. In the case of an array resulting from a Promise, where the array must be accessible as soon as possible, we can store the result of the Promise in the state. This is not ideal because this may give scaling issues. Always resolving the Promise when it is needed will ensure consistency across all systems.
