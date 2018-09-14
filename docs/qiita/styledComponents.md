### Styled Components の特徴その１

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

Styled Components の場合

```javascript
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

## 参照

[Styled Components: To Use or Not to Use?](https://medium.com/building-crowdriff/styled-components-to-use-or-not-to-use-a6bb4a7ffc21)
