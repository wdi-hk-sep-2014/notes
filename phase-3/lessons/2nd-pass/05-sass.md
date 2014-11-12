# SASS

Syntactically Awesome Style Sheets, used by Rails as default way to simiplify works in CSS.

## Objective

To preview the use of SCSS, which is a preprocessor of CSS. Thus, everything will turn back to CSS in runtime. So why?

1. Variables
2. Nesting
3. Partial / Import
4. Mixins
5. Extend
6. Operators

For us, we will take a look on the first two.

## Steps

1. Open a file with `.scss` extension, e.g. `welcome.css.scss`
2. Add a variable `$nav-top: 50px`
3. Add the SCSS syntax
4. Why do we use variable?

```
body {
  padding-top: $nav-top;
}
```

1. Add some classes to our board, `timetable` outside, `week` per row, and `day` per cell
2. Add the `number` class to the first column of every row
3. Now define the CSS rule to `number` using specific CSS selector all the way from `timetable` to `week` to `number`
4. Do the same for `timetable` to `week` to `day`
5. Add a `div` inside every `day` cell, and give a width and height
6. Why do we use nested form?

```
.timetable {
  .week {
    .number {
      /* ... */
    }
    .day {
      /* ... */
    }
  }
}
```

## Successful Completion

- You should be able to start CSS coding using SASS
- You will be able to apply some variables
- You will be able to apply some nested form of SASS

## Reference Links

- [SASS](http://sass-lang.com/)
- [Why SASS and SCSS](http://thesassway.com/editorial/sass-vs-scss-which-syntax-is-better)
