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

### DOCTYPE

By default the a HTML5 DOCTYPE is added to the created html files. You can specify a custom DOCTYPE like this:

```
gulp.task('jsx', () => {

    return gulp.src('./*.jsx')
        .pipe(compileJSX({
            doctype: '<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">'
        }))
        .pipe(gulp.dest('./'))

});
```

If you do not want to have a DOCTYPE added you can disable it like this:

```
gulp.task('jsx', () => {

    return gulp.src('./*.jsx')
        .pipe(compileJSX({
            doctype: false
        }))
        .pipe(gulp.dest('./'))

});
```

### gulp-data support

Supports gulp-data to pass in data to be used to populate each individual .jsx file.

https://github.com/colynb/gulp-data
