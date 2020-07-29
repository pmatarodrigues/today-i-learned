# Fetch API

```
let url = "https://pmatarodrigues.com";

fetch(url + "?language=react&key=" + process.env.SECRET_KEY)
.then(response => response.json())
.then((jsonData) => {
    // jsonData is parsed json object received from url
    console.log(jsonData)
})
.catch((error) => {
    // handle your errors here
    console.error(error)
})

```