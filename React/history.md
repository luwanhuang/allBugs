Passing parameters with history push:
```

import { useHistory } from "react-router-dom";

const FirstPage = props => {
    let history = useHistory();

    const someEventHandler = event => {
       history.push({
           pathname: '/secondpage',
           search: '?query=abc',
           state: { detail: 'some_value' }
       });
    };

};

export default FirstPage;

```
Accessing the passed parameter using useLocation from 'react-router-dom':
```
import { useEffect } from "react";
import { useLocation } from "react-router-dom";

const SecondPage = props => {
    const location = useLocation();

    useEffect(() => {
       console.log(location.pathname); // result: '/secondpage'
       console.log(location.search); // result: '?query=abc'
       console.log(location.state.detail); // result: 'some_value'
    }, [location]);

};
```
