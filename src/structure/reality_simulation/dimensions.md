# Dimensions
A dimensions represents slices of a [Reality](./reality.md), these slices being connected or not. Note that all dimensions share the same [Reality Rules](reality_rules.md). You can imagine the dimensions as being represented by the slices of a bread, side by side, _sometimes connected, sometimes disconnected_.

## Structure
Similar to [Realities](./reality.md), dimensions contain two major things:
- [Dimension Rules](./#dimension-rules)
- [Universes]()

## Dimension Rules
Define the fundamental rules of this dimensions, all being optional and by default ignored if not provided:
- [Size](./dimensions.md#size)
- [Time Scale](./dimensions.md#time-scale)
- [Gravity](./dimensions.md#gravity)

### Size
Floating value that is `1.0` by default. This value represents the **relative size** of a dimension, the concept can be a bit abstract since a [Reality]() does not have any type of size, so how it works?

This rule is used to scale all values inside of the formulas that are related to sizes. This way code that uses `100m` to measure something, will use `50m` if the size is `0.5`.

There is actually a second use for this rule, by default all dimensions are equivalent in position, since they are slices of the same reality, but dimensions with different sizes will have their positions translated to equivalent positions.

Think this way: we have two dimensions, `A` with size `1.0` and `B` with size `2.0`, and there is a entity existing in `A` at the position `(10.0, 10.0, 10.0)`, when `A` goes to `B` (dimensional teleportation) its new positions is going to be `(5.0, 5.0, 5.0)`, because we do `(Size_A / Size_B) * position` to get the relative position. This is not another rule feature per se, but rather another example use, since all the values for all formulas that relate to scale and are used inside the dimension, will use the size rule.

### Time Scale
A floating value very similar to [`Size`](#size), defaults to `1.0` and is recommended to stay the default value unless you know exactly what you are doing. This value is reflected in the [Simulation Speed]() of the dimension. Making things go faster will require more calculations, making things go slower will require less.

There is a plan to make this rule be more useful in the future, but don't expect magical changes, we are doing a complex research on how to best implement time travelling, and if we find a good enough solution this value will be more useful later.

### Gravity
Another floating value that defaults to `1.0`, it is way easier to understand and use, it will affect the scale of gravity. Higher values will increase gravity strength for the entire dimension.
