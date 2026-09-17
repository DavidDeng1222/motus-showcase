# Failure-driven iteration

## Case: a plausible box in the wrong place

An early automatic racket candidate placed a high-confidence region near the athlete's face and hand. A score alone could not show whether the region represented the racket head, the grip, clothing texture or background structure.

The revised workflow added three checks:

1. classify a visual region by its semantic role before using it for direction;
2. allow a grip-proximal region to remain visible as tracking evidence without promoting it to a racket-head direction;
3. prevent a rejected 2D anchor from creating a 3D racket reference.

## Result

The source moment remains in the audit trail, the invalid visual anchor is rejected, and the 3D replay does not inherit it. This is a narrower result than claiming universal racket detection, but it is reproducible and inspectable.

## What remains open

- fast rotation and motion blur;
- partial racket visibility;
- athlete overlap and background rails;
- physical validation of racket-face orientation;
- a larger independently labelled evaluation set.

