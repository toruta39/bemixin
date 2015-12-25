# bemixin
Minimal helper mixins for BEM user

## Install

```
npm install bemixin --save-dev
```

## Usage

Webpack with sass-loader

```
@import "~bemixin"

@include b(cat) {
  margin: 0 auto;
  width: 50%;
  background-color: white;

  @include e(eye) {
    background-color: blue;

    @include m(left) {
      background-color: gold;
    }
  }

  @include m(fatty) {
    width: 100%;
  }
}
```

Output

```
.cat {
  width: 50%;
  margin: 0 auto;
  background-color: white; }

  .cat__eye {
    background-color: blue; }

    .cat__eye--left {
      background-color: gold; }

  .cat--fatty {
    width: 100%; }
```
