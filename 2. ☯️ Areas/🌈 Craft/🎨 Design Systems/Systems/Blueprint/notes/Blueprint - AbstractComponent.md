[[Palantir Blueprint]]

https://github.com/palantir/blueprint/blob/develop/packages/core/src/common/abstractPureComponent2.ts

# AbstractComponent

[[2021-05-22]]

`AbstractComponent` is used as a foundation for Blueprint's Components, providing enhanced functionality to React's base `Component` class. Just like React's Component classes, `AbstractComponent` provides both `Pure` and regular versions of this class.

## Version 2

The current implementation (`202105220927`) relies on a newer and standardized `AbstractComponent2`.
Noticeable differences would be that `AbstractComponent2` includes fully React 16+ lifecycle methods as well as `requestAnimationFrame` and `timeout` methods.
