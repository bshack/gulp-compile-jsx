# gulp-compile-jsx

Compile JSX templates into static html documents

```
npm install gulp-compile-jsx --save
```

## Usage

```
const gulp = require('gulp');
const compileJSX = require('gulp-compile-jsx');

gulp.task('jsx', () => {

    return gulp.src('./*.jsx')
        .pipe(compileJSX())
        .pipe(gulp.dest('./'))

});
```

### gulp-data support

Supports gulp-data to pass in data to be used to populate each individual .jsx file.

https://github.com/colynb/gulp-data
