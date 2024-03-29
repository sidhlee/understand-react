# React State


## Updating State 

### setState based on previous state
You should pass in a callback instead of object when you are manipulating one state based on any existing state props.
Setting state based on state directly can cause unintended results due to React's batch updating.
```JSX
handleClick() {
  this.setState({
    toggledOn: !this.state.toggledOn
  });
}
```

should be re-written as:

```JSX
handleClick() {
  this.setState((prevState, props) => {
    return ({
      toggledOn: !prevState.toggledOn
    });
  }
}
```
