
## Input

```javascript
// @validateRefAccessDuringRender
function Component(props) {
  const ref = useRef({inner: null});
  ref.current.inner = props.value;
  return ref.current.inner;
}

```


## Error

```
Found 2 errors:

Error: Ref values (the `current` property) may not be accessed during render. (https://react.dev/reference/react/useRef)

error.invalid-set-and-read-ref-nested-property-during-render.ts:4:2
  2 | function Component(props) {
  3 |   const ref = useRef({inner: null});
> 4 |   ref.current.inner = props.value;
    |   ^^^^^^^^^^^ Ref values (the `current` property) may not be accessed during render. (https://react.dev/reference/react/useRef)
  5 |   return ref.current.inner;
  6 | }
  7 |

Error: Ref values (the `current` property) may not be accessed during render. (https://react.dev/reference/react/useRef)

error.invalid-set-and-read-ref-nested-property-during-render.ts:5:9
  3 |   const ref = useRef({inner: null});
  4 |   ref.current.inner = props.value;
> 5 |   return ref.current.inner;
    |          ^^^^^^^^^^^^^^^^^ Ref values (the `current` property) may not be accessed during render. (https://react.dev/reference/react/useRef)
  6 | }
  7 |
```
          
      