### Styled Components の特徴その 1

下のコードの例だと`style`と`hoverStyle`の２つの CSS を分けるロジックがコンポーネントに書かれており、コードが見にくくなってしまいます。

```javascript
render() {
const style = {
  color: `${this.props.themeColor}`,
}
const hoverStyle = {
  color: `${this.props.hoverThemeColor}`
}
  return (
    <button
      onMouseEnter={this.handleHover}
      onMouseOut={this.handleHover}
      style={this.state.isHovered ? hoverStyle : style}
    >
      Click Me!
    </button>
  );
}
```

その一方 Styled Component の場合は、CSS の記述と elements を分割しているのでコンポーネントが見やすいです。

```javascript
//Styled Components の場合
import styled from 'styled-components';
const BrandedButton = styled.button`
  color: ${props => props.themeColor};
  &:hover {
    color: ${props => props.themeHoverColor};
  }
`
render(){
  return (
    <BrandedButton themeHoverColor="pink" themeColor="blue" >
      Click Me!
    </BrandedButton>
  );
}
```

Styled Components を使用することにより、既に存在する JavaScript の値を CSS に加えることが容易になり、さまざまな処理に対応することができるようになるでしょう。

### Styled Components の特徴その 2

The ThemeProvider is used as a wrapper that injects theme props into all of its child components. If you’re using a state library like Redux, you can avoid having multiple connected components request the same properties from state by using the ThemeProvider to pass these props to all your styled components.

We found the ThemeProvider particularly useful when building a ‘configuration’ page, which is essentially a duplicate page that allows a user to customize certain stylistic elements, like colour. We wrapped our configuration page in a ThemeProvider that was referencing a different piece of state than the non-editable portion of the app. That allowed us to reuse all the styled components while also showing the user feedback as they updated their stylistic elements.

### Styled Components の特徴その 3

With Styled Components’ css function, you can use props to conditionally render css, which meant that we no longer had to render conditional class names based on props. This reduces clutter in your components as well as maintains a separation of concerns between CSS and JavaScript.

Take this button, for example:

```javascript
import styled from 'styled-components';
const Button = styled.button`color: ${props => props.isSecondary ? ‘blue’ : ‘white’};`
```

What if we wanted to add a third iteration of this button? It would quickly become difficult with the ternary pattern. With the css function from Styled Components, you can easily add as many conditions as you’d like!

Here, we used Styled Components to give a button different colours depending on its props.

```javascript
// Declaring the styled component
const Button = styled.button`
  color: ‘white’;
  ${props =>
    props.isSecondary &&
    css`
      color: ‘blue’;
    `} ${props =>
    props.isDisabled &&
    css`
      color: ‘grey’;
    `};
`;
```

// Using the disabled iteration of the styled component
<Button isDisabled />
The button is styled to have white text by default, but if an ‘isDisabled’ prop is applied, the color property will be overwritten since it appears later in the style declaration, and the button will be given a colour of grey.

### Styled Components の特徴その 4

4. Testing

We implemented the Jest Styled Components library for our testing in Jest. It makes testing styled components painless by creating consistent class names and allowing you to assert specific CSS rules that might be important to the integrity of your app.

Below is an example of an assertion that Jest Styled Components allow you to make on your component:

expect(button).toHaveStyleRule('color', 'blue');
Pairing these simple assertions with the various states of your app is a powerful pattern to catch visual regressions.

## 参照

[Styled Components: To Use or Not to Use?](https://medium.com/building-crowdriff/styled-components-to-use-or-not-to-use-a6bb4a7ffc21)
