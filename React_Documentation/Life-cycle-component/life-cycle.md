**Life cycle Components**

*__Categorized into 3 parts:__*

   1. Mounting
   2. updating
   3. Unmounting

# Mounting Method

* The component mounts when it is created and first inserted to the DOM.
* The methods available in this period are:
    1. constructor()
    2. componentWillMount()
    3. render()
    4. componentDidMount()

    **componentWillMount() Hook :**

    * It will be deprecated in React.
    * Constructor will be called pre-render and componentDidMount post-render.
    * The componentWillMount() is called right before the render() is called.
    * The componentWillMount() sits between constructor() and render() which puts in very odd position.
    * When the render() is not called at this point,so nothing can be done with the DOM of the component,since it has not been mounted.
    * API calls are asynchronous and the data might not be returned before the render method gets called.This means that the component might render with empty data atleast once. 

    **componentDidMount() Hook :**

    * This method will available after the component has mounted i.e., after the HTML from render has finished loading.
    * This is the best place to make API calls, at this point the component has been mounted and is available to the DOM  

# Updating method

* Components donot stay in the same state after mounting.
* Sometimes props could change and the component has to be re-rendered.
* 5-updating life cycle methods:
    1. componentWillReceiveProps
    2. shouldComponentUpdate
    3. componentWillUpdate
    4. render
    5. componentDidUpdate

    **1. componentWillReceiveProps method :**
      
      * This method is also set to be deprecated.
      * Props are externally passed into a component by its parent component.If state of the parent component changes,the props passed to a component changes and it has to be updated.
      * The method is called before a component does anything with the new props.This method is called with the new props passed as an arguement.

    **2.shouldComponentUpdate method :**

      * This method is called before the component re-renders after receiving the new set of props.
      * It receives 2 arguements, the next props, and the next state.
      * It is used to know that a components output is not affected by a change of props or state in the component and it should not re-render.
      * It returns true or false.
      * If it is true,it will go ahead and do what it always does and re-render.
      * If it is false,component will not update.

    **3.componentWillUpdate method :**
     
      * It is used to perform preparations before re-rendering occurs.
      * In this we can interact with thingd outside of the React architecture.
      * If we want to do any non-React setup before component renders ,this method can be used.

    **4.componentDidUpdate method :**

      * It is called after any rendered HTML has finished loading.
      * It has 2 arguements -the props and the state.

# Unmounting method

* Components donot stay in the DOM.Sometimes they have to be removed due to changes in the state.
* Unmounting method will help us to handle unmounting of components.
* 2-unmounting methods:
    1. componentWillUnmount()
    2. componentDidCatch()

    **componentWillUnmount method :**

    * It is called right before a componentis removed from the DOM.

    **componentDidCatch method :**

    * Components becomes an error boundary if it defines the componentDidCatch method.
    * In this method,this.setState can be called and used to unhandle javascript error in child component tree.
    