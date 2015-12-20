# gulp.nunjucks

## Install

    $ npm install gulp.nunjucks --save-dev

## How to use

    var nunjucks = require('gulp.nunjucks');

    var env = nunjucks.configure('dir/to/templates', {
        trimBlocks: true,
        lstripBlocks: true
    });

    gulp.src(src)
        .pipe(data(function (file) {
            return {
                name: 'name',
                version: 'version'
            };
        }))
        .pipe(nunjucks({
            global: 'val/for/all/template'
        }))
        .pipe(gulp.dest('dest'))
