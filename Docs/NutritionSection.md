# Nutrition Section Documentation

This document provides a detailed explanation of the styling and animations used in the `NutritionSection` component.

## `nutrition-section`

We use the following styling for the `nutrition-section`: `@apply min-h-dvh 2xl:h-[120dvh] overflow-hidden relative` and a radial gradient background.

-   `min-h-dvh 2xl:h-[120dvh]`: This defines the responsive height of the container.
-   `overflow-hidden`: This is used to prevent the child elements from overflowing the container.
-   `relative`: We use `relative` because we want to position the child elements of this container relative to the container itself.

The background is a radial gradient that goes from `#f3ece2` to `#dcccb0`.

## `big-img`

We use the following styling for the `big-img`: `@apply w-full absolute 2xl:h-full md:h-2/3 h-1/2 left-0 bottom-0 object-bottom 2xl:object-contain object-cover`

-   `w-full`: This sets the width of the image to `100%`.
-   `absolute`: This positions the image relative to its parent container.
-   `2xl:h-full md:h-2/3 h-1/2`: This defines the responsive height of the image.
-   `left-0 bottom-0`: This positions the image at the bottom left of its container.
-   `object-bottom 2xl:object-contain object-cover`: This defines how the image should be resized to fit its container.

## `nutrition-title`

We use the following styling for the `nutrition-title`: `@apply 2xl:max-w-4xl xl:max-w-2xl md:py-0 py-3 md:pb-5 pb-0 lg:pb-0 md:text-center text-[#513022]`

-   `2xl:max-w-4xl xl:max-w-2xl`: This defines the responsive maximum width of the title.
-   `md:py-0 py-3 md:pb-5 pb-0 lg:pb-0`: This is used to adjust the padding of the title on different screen sizes.
-   `md:text-center`: This centers the text on medium and larger screens.
-   `text-[#513022]`: This sets the text color to a custom dark brown color.

## `nutrition-text-scroll`

We use the following styling for the `nutrition-text-scroll`: `@apply rotate-[-3deg] border-[.5vw] border-[#e3d3bc] text-nowrap opacity-0 md:-mt-32 -mt-24`

-   `rotate-[-3deg]`: This rotates the element by `-3` degrees.
-   `border-[.5vw] border-[#e3d3bc]`: This sets a border with a responsive width and a custom color.
-   `text-nowrap`: This prevents the text from wrapping to the next line.
-   `opacity-0`: This makes the element transparent. The opacity is animated with GSAP.
-   `md:-mt-32 -mt-24`: This is used to adjust the top margin of the element on different screen sizes.

## `nutrition-box`

We use the following styling for the `nutrition-box`: `@apply absolute md:bottom-16 bottom-5 w-full md:px-0 px-5`

-   `absolute`: This positions the element relative to its parent container.
-   `md:bottom-16 bottom-5`: This is used to adjust the bottom position of the element on different screen sizes.
-   `w-full`: This sets the width of the container to `100%`.
-   `md:px-0 px-5`: This is used to adjust the horizontal padding of the container on different screen sizes.

## `list-wrapper`

We use the following styling for the `list-wrapper`: `@apply bg-[#fdebd2] rounded-full border-[.5vw] border-[#e8ddca] mx-auto max-w-7xl md:py-8 py-5 md:px-0 px-5 flex justify-between items-center`

-   `bg-[#fdebd2]`: This sets the background color to a custom light yellow color.
-   `rounded-full`: This makes the container a circle.
-   `border-[.5vw] border-[#e8ddca]`: This sets a border with a responsive width and a custom color.
-   `mx-auto`: This centers the container horizontally.
-   `max-w-7xl`: This sets the maximum width of the container.
-   `md:py-8 py-5 md:px-0 px-5`: This is used to adjust the padding of the container on different screen sizes.
-   `flex justify-between items-center`: This uses `flexbox` to space the elements evenly and center them vertically.
