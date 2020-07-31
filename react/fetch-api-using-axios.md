# Fetch JSON API using axios

Install **axios** using npm

`
npm install --save axios
`

Import **axios** on React project

`
import axios from 'axios';
`

Call axios function using **.get**, **.post**, **.delete** ...
(Source)[https://www.digitalocean.com/community/tutorials/react-axios-react]

```
axios.get(url)
.then(res => {
    const data = res.data;
    this.setState({jsonData: data});

    console.log(this.state.jsonData)
})
.catch((error) => console.log("Can’t access " + url + " response. " + error))
```