# React Context | 

- React Context
  - createContext()
  - Consumer Component
- Context Provider
  - Where to Write?
- Context Flow

# 1. Prop Drilling:
  Props are passed from one Component to another Component that does not need the data but only helps in passing it through the tree is called Prop Drilling.

# 2. React Context:
  Context is a mechanism that provides different Components and allows us to pass data without doing prop drilling.
  2.1 Creating Context:
    Syntax: React.createContext(INITIAL_VALUE)
    It returns an object with different properties to update and access values from the context.
  2.2 Context Properties:
    The Context object provides two properties.
      1 Consumer
      2 Provider
  2.3 How to Access the Value?
    We can access the value in the Context using Consumer Component provided by the Context Object.
    
# 3. Consumer Component:
  Syntax: 
      <ContextObject.Consumer>
        {/*callback function*/}
      </ContextObject.Consumer>
    -> We access the Consumer component using dot notation from the context object.
    ->  We will give a callback function as children for Consumer Component.
3.1 Understanding Syntax
 The callback function receives the current context value as an argument and returns a component or a JSX element.

# 4. Provider:
    Provider Component updates the value of Context.
    When the provider updates context, all the nested consumers of that provider will be re-rendered.
    Updated context value can only be accessed by the consumers nested within the provider.
    Syntax: 
      <ContextObject.Provider value={/* some value */}>
         ...
      <ContextObject.Provider/>
    To update context value, we have to pass it as a prop to the Provider component.
