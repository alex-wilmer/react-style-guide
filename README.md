## Alex Wilmer's Personal React Style Guide

#### Why?

I like my code to look very clean. Probably too clean. But I also think it's very important to write code that can be easily edited. This style guide is designed with these tenets in mind.

  - looks pretty
  - can be easily edited

### Spaces between prop, equals and value.

```jsx
// bad
<Foo
  bar="baz"
/>

// good
<Foo
  bar = "baz"
/>
```

#### Justification

We write `let x = 3`, not `let x=3`. Should be same for props.

### Props on new line. Always.

```jsx
// bad
<Foo bar = "baz" />

// good
<Foo
  bar = "baz"
/>

// good
<Foo
  style = {{
    color: `blue`
  }}
/>
```

#### Justification

Row manipulation is super easy. Not so much for columns.

### Closing angle on new line.

```jsx
// bad
<Foo
  bar = "baz" />

// good
<Foo
  bar = "baz"
/>
```

#### Justification

Way easier to sense component structure.

### Spaces inside JSX curly braces.
```jsx
// bad
<Foo
  bar = {baz}
/>

// good
<Foo
  bar = { baz }
/>

/*
 *  Exception: object curly's don't need extra space.
 */

// bad
<Foo
  bar = { { baz } }
/>

// good
<Foo
  bar = {{ baz }}
/>
```

#### Justification

None. Personal taste.

### Conditional Component Nesting

```jsx
// bad
<Foo>
  { bar && <Baz /> }
</Foo>

// bad
<Foo>
  { bar &&
    <Baz /> }
</Foo>

// getting there
<Foo>
  { bar &&
    <Baz />
  }
</Foo>

// good
<Foo>
  { bar &&
  <Baz />
  }
</Foo>
```

#### Justification

The conditional wrapping should be able to be added or removed without needing to the change the position of the component.

### Iteration

```jsx
<Foo>
  { bar.map(x =>
  <Baz>
    { x }
  </Baz>
  )}
</Foo>
```

#### Justification

Same as above.
