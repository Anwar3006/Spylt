# Benefit Section Documentation

This document provides a detailed explanation of the styling and animations used in the `BenefitSection` component.

## `benefit-section`

We use the following styling for the `benefit-section`: `@apply min-h-dvh bg-[#222123] overflow-hidden relative`

-   `min-h-dvh`: This sets the minimum height of the container to `100vh`, which means it will fill at least the entire height of the screen.
-   `bg-[#222123]`: This sets the background color to a custom dark gray color.
-   `overflow-hidden`: This is used to prevent the child elements from overflowing the container.
-   `relative`: We use `relative` because we want to position the child elements of this container relative to the container itself.

## Title Classes

We use the following styling for the titles in this section:

-   `.first-title`: `@apply rotate-[3deg] relative z-10`
-   `.second-title`: `@apply rotate-[-1deg] md:-translate-y-5`
-   `.third-title`: `@apply rotate-[1deg] md:-translate-y-12 relative z-10`
-   `.fourth-title`: `@apply rotate-[-5deg] md:-translate-y-12`

These classes are used to rotate and translate the titles to create a unique, staggered look. The `z-index` is used to ensure that the titles are displayed in the correct order.

## `vd-pin-section`

We use the following styling for the `vd-pin-section`: `@apply md:h-[110vh] h-dvh overflow-hidden md:!-translate-y-[15%] md:mt-0 mt-20`

-   `md:h-[110vh] h-dvh`: This defines the responsive height of the container.
-   `overflow-hidden`: This is used to prevent the child elements from overflowing the container.
-   `md:!-translate-y-[15%]`: This is used to adjust the vertical position of the container on medium and larger screens.
-   `md:mt-0 mt-20`: This is used to adjust the top margin of the container on different screen sizes.

## `play-btn`

We use the following styling for the `play-btn`: `@apply absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 size-[9vw] flex justify-center items-center bg-[#ffffff1a] backdrop-blur-xl rounded-full`

-   `absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2`: This centers the button in the middle of its container.
-   `size-[9vw]`: This sets the width and height of the button to `9vw`, which is a responsive value that depends on the screen width.
-   `flex justify-center items-center`: This uses `flexbox` to center the content of the button.
-   `bg-[#ffffff1a]`: This sets the background color to a semi-transparent white.
-   `backdrop-blur-xl`: This applies a blur to the background of the button.
-   `rounded-full`: This makes the button a circle.
