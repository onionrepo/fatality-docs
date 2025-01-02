## rounding

This enum is used to determine the rounding for rounded shapes.

## tl

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Round top-left corner.

## tr

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Round top-right corner.

## bl

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Round bottom-left corner.

## br

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Round bottom-right corner.

## t

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Round both of the top corners. This produces the same result as using `bit.bor(draw.rounding.tl, draw.rounding.tr)`.

## l

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Round both of the left corners. This produces the same result as using `bit.bor(draw.rounding.tl, draw.rounding.bl)`.

## r

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Round both of the right corners. This produces the same result as using `bit.bor(draw.rounding.tr, draw.rounding.br)`.

## b

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Round both of the bottom corners. This produces the same result as using `bit.bor(draw.rounding.bl, draw.rounding.br)`.

## all

[![Field][This field is a regular field that must be accessed using a dot (.).]rw]

Round all corners. This produces the same result as using `bit.bor(draw.rounding.tl, draw.rounding.tr, draw.rounding.bl, draw.rounding.br)`.