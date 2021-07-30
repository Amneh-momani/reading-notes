# React Docs - thinking in React

## We would break a mock into a component heirarchy:

+ 1-We have drawn boxes around every component in the **mock**
+ 2-give every component a name

## single responsibility principle

**The single responsibility principle** a component should only do one thing

_To create a static version of our app that displays ourdata model, we'll need to create components that reuse other components and pass the data using properties.  So the way to pass data from parent to child is **Prop**  and The **state** is only for interaction._

 Once we have a static application we need to add interactivity requires a lot of thinking and not a lot of typing.

Example :

       class ProductCategoryRow extends React.Component {
         render() {
           const category = this.props.category;
           return (
             <tr>
               <th colSpan="2">
                 {category}
               </th>
                    </tr>
           );
         }
       }

       class ProductRow extends React.Component {
         render() {
           const product = this.props.product;
           const name = product.stocked ?
             product.name :
             <span style={{color: 'red'}}>
               {product.name}
             </span>;

           return (
             <tr>
               <td>{name}</td>
               <td>{product.price}</td>
             </tr>
           );
         }
       }


 ##  The three questions you can ask to determine if something is state are :

 + Is it passed in from a parent via props? If so, it probably isn’t state.
+ Does it remain unchanged over time? If so, it probably isn’t state.
+ Can we compute it based on any other state or props in your component? If so, it isn’t state.

## We can identify where state needs to live by these steps:
+ Select each component that displays something based on that state.
+ Find a common owner component **one component above all components that need state in the hierarchy**.
+ Either the common owner or another component higher up in the hierarchy should own the state.
+ If we can’t find a component where it makes sense to own the state so we have to create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.


