# React Component Life Cycle
1. **Mounting**, when the component is being initialized and put into the DOM for the first time
2. **Updating**, when the component updates as a result of changed state or changed props
3. **Unmounting**, when the component is being removed from the DOM

![Component life cycle diagram](/react/react_diagram-lifecycle-flow.png)


## Related methods
| Stage | Methods |
| ----- | ------- |
| Mounting | `constructor()`, `render()`, `componentDidMount()` |
| Updating | `render()`, `componentDidUpdate()`|
| Unmounting | `componentWillUnmount()` |

* `componentDidMount()`: good for side effects after rendering (runs one time only).
* `componentDidUpdate(prevProps)`: mount-phase setup
* `componentWillUnmount()`: clean up a side-effect of a component.
