# Hooks

* Hooks are new addition in react.
* Example :
\
    import React, { useState } from 'react';
\
    function Example() {
\
        const [count, setCount] = useState(0);
\
        return (
\
            < div>
\ 
            < p>You clicked {count} times< /p>
\
            < button onClick={() => setCount(count + 1)}>
\
            Click me
\
            < /button>
\
            < /div>
\
        );
\
    }

* This *useState* is the first hook.
* Hooks are backward compatible.
* Hooks is a function that "hook into" react state and life cycle.
* It wont work inside classes