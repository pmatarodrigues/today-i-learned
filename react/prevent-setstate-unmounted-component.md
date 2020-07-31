# Prevent setState() on unmounted Component

To prevent the execution of setState on unmounted components, we should just create a variable that gets set as true when the component is mounted, and false when the component unmounts.
This makes it possible for us to verify if the component is mounted or not.

```
class Tests extends Component {
  _isMounted = false;

  constructor(props) {
    super(props);
    this.state = {
      active: []
    }
  }

  componentDidMount() {
    this._isMounted = true;

    axios
      .get('https://pmatarodrigues.com/api/json?language=react')
      .then(result => {
        if (this._isMounted) {
          this.setState({
            active: true,
          });
        }
      });
  }

  componentWillUnmount() {
    this._isMounted = false;
  }
}
```