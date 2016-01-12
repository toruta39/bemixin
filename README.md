# bemixin
Minimal helper mixins for BEM user

## Install

```
npm install bemixin --save-dev
```

## Usage

Webpack with sass-loader

```
@import "~bemixin";

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

    @include b(cat) {
      @include e(eye) {
        background-color: gold;
      }
    }
  }
}
```

Output

```
.cat {
  margin: 0 auto;
  width: 50%;
  background-color: white; }

  .cat__eye {
    background-color: blue; }

    .cat__eye--left {
      background-color: gold; }

  .cat--fatty {
    width: 100%; }

    .cat--fatty .cat__eye {
      background-color: gold; }
```
