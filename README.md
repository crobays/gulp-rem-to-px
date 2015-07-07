# gulp-rem-to-px
Gulp plugin to convert rem units to pixels

## Example

    var rem_to_px = require('gulp-rem-to-px')
        ,rename = require('gulp-rename');
    
    gulp.task('ie', function(){
      gulp.src('./style.css'),   
        .pipe(rem_to_px()) // default = 16px
        .pipe(rename('ie.css'))
        .pipe(gulp.dest(./));
    });
    
    gulp.task('ie-12px', function(){
      gulp.src('./style.css'),   
        .pipe(rem_to_px({fontSize: 12})) // set root size to 12px
        .pipe(rename('ie.css'))
        .pipe(gulp.dest(./));
    });
    
    gulp.task('default', ['ie']);
