# Difference between State and Props

**States :**

* In this variables which exists inside the component are not accessed and modified outside the component.
* Example :
    \
    class App extends React.component {
    \
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        state = {
    \
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            name : 'xyz';
    \
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        }
    \
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        render() {
    \
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            return< div>Hello{ this.state.name }< /div>
    \
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        }
    \
    } 

* In this example, we declare a name property inside a component and used in rendering.
* This state is mutable in nature.
# 
**Props :**

* In props we dont render the component again and again with the same data.But, sometimes we change the content inside the component.
* Example :
    \
    class app extends React.component {
    \
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        render() {
    \
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        return< div>Hello{ this.props.name }< /div>
    \
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        }
    \
    }
    \
    < app name = 'xyz'/>
    \
    < app name = 'abc'/> 

* In this simple example we passes the props as attribute and we access them inside our component using *this.props* 
* This is immutable.