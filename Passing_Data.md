# Passing data to Children

## Button with callback
```
render() {
  return (
    <div>
      <PlusButton count={this.state.count} increaseCount={(count) => this.setState({count})}/>
    </div>
  );
}
```
***which will envoke***
```
const PlusButton = ({count, increaseCount}) => {
  return(
    <button onClick={() => increaseCount(count + 1)}>+</button>
  )
};
```

