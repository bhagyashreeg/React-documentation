# Render method

* It is most used method for react powered component which returns a JSX with backend data.
* Rendering is the process of transforming react components into DOM nodes that our browser can understand and display on the screen.
* Example :
\
    import React, { Component } from 'react';
\
    class App extends Component {
\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        render() {
\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            return (
\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                < div>< h1 className="App-title">Welcome to React< /h1>< /div>
\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            );
\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        }
\
    }
\
    export default App;

* We cannot define setState() inside render() function, because setState() changes the state of the application.
