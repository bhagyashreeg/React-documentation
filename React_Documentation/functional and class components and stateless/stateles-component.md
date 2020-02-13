# Stateless component

* A stateless components has no state, this means we cant reach *this.state* inside it.
* They always render same thing.
* Example: 
 const regNumber = ({number}) => {
 return (
   <ul>
     {number.map(num => {
       return < li>regesternumber< /li>
     })}
   </ul>
  )
 }
 
* In the above example of [stateless] component is often written as function.
* Making a component stateless will make other component reuse them multiple times.
* They are always reusable.


