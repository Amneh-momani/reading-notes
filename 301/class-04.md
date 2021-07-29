# React Docs - Forms

 **Controlled Components** It's any element which included inside the Form tag  **< input>, < textarea>, and < select>** and his value is controlled by react so the mutable state kept in the state property of components and only updated with **setState()**.
 
 Example :

         render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Name:
          <input type="text" value={this.state.value} onChange={this.handleChange} />
        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }

  Note: _We Should update the state with their responses as soon as they enter them  because we have to give them a chance to make sure from their responses and they will see and relize if it correct and as they want but if we wait to store the users responses from the form into state when they submit the form then we will not give them a chance to change it._


  we target what the user is entering if we have an event handler on an input field by :

             handleChange(event) {
         this.setState({value: event.target.value});
       }

after decideing the name of that field in the form .



# The Conditional (Ternary) Operator Explained

we use a **ternary operator** because we could do the same exact if condition work in just one line of code.

Rewrite the following statement using a ternary statement:

        if(x===y){
         console.log(true);
          } else {
         console.log(false);
          }


By ternary operator :

x === y ? console.log(true) : console.log(false);

