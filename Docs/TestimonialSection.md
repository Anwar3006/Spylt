# Testimonial Section Documentation

This document provides a detailed explanation of the styling and animations used in the `TestimonialSection` component.

## `testimonials-section`

We use the following styling for the `testimonials-section`: `@apply bg-milk relative w-full h-[120dvh]`

-   `bg-milk`: This sets the background color to a custom light milk color.
-   `relative`: We use `relative` because we want to position the child elements of this container relative to the container itself.
-   `w-full`: This sets the width of the container to `100%`.
-   `h-[120dvh]`: This sets the height of the container to `120vh`. The extra height is to accommodate the parallax scrolling effect.

## `pin-box`

We use the following styling for the `pin-box`: `@apply flex items-center justify-center w-full ps-52 absolute top-1/2 -translate-y-1/2`

-   `flex items-center justify-center`: This uses `flexbox` to center the content both horizontally and vertically.
-   `w-full`: This sets the width of the container to `100%`.
-   `ps-52`: This adds a padding to the start of the container.
-   `absolute top-1/2 -translate-y-1/2`: This centers the container vertically.

## `vd-card`

We use the following styling for the `vd-card`: `@apply md:w-96 w-80 flex-none md:rounded-[2vw] rounded-3xl -ms-44 overflow-hidden lg:relative absolute border-[.5vw] border-milk`

-   `md:w-96 w-80`: This defines the responsive width of the card.
-   `flex-none`: This prevents the card from growing or shrinking.
-   `md:rounded-[2vw] rounded-3xl`: This defines the responsive border radius of the card.
-   `-ms-44`: This adds a negative margin to the start of the card, which creates the overlapping effect.
-   `overflow-hidden`: This is used to prevent the child elements from overflowing the card.
-   `lg:relative absolute`: This is used to adjust the positioning of the card on different screen sizes.
-   `border-[.5vw] border-milk`: This sets a border with a responsive width and a custom color.
