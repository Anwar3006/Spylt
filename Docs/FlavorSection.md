# Flavor Section Documentation

This document provides a detailed explanation of the styling and animations used in the `FlavorSection` component.

## `flavor-section`

We use the following styling for the `flavor-section`: `@apply min-h-dvh bg-milk`

-   `min-h-dvh`: This sets the minimum height of the container to `100vh`, which means it will fill at least the entire height of the screen.
-   `bg-milk`: This sets the background color to a custom light milk color.

## `flavor-text-scroll`

We use the following styling for the `flavor-text-scroll`: `@apply rotate-[-3deg] md:translate-y-5 border-[.5vw] border-milk absolute z-10`

-   `rotate-[-3deg]`: This rotates the element by `-3` degrees.
-   `md:translate-y-5`: This is used to adjust the vertical position of the element on medium and larger screens.
-   `border-[.5vw] border-milk`: This sets a border with a responsive width and a custom color.
-   `absolute`: This positions the element relative to its parent container.
-   `z-10`: This sets the `z-index` to `10`, which ensures that this element is displayed on top of the other elements in this section.

## `slider-wrapper`

We use the following styling for the `slider-wrapper`: `@apply lg:h-dvh min-h-dvh md:min-h-fit w-full mt-0 md:mt-20 xl:mt-0`

-   `lg:h-dvh min-h-dvh md:min-h-fit`: This defines the responsive height of the container.
-   `w-full`: This sets the width of the container to `100%`.
-   `mt-0 md:mt-20 xl:mt-0`: This is used to adjust the top margin of the container on different screen sizes.

## `flavors`

We use the following styling for the `flavors`: `@apply h-full w-full flex md:flex-row flex-col items-center 2xl:gap-72 lg:gap-52 md:gap-24 gap-7 flex-nowrap`

-   `h-full`: This sets the height of the container to `100%`.
-   `w-full`: This sets the width of the container to `100%`.
-   `flex md:flex-row flex-col items-center`: This uses `flexbox` to create a horizontal layout on medium and larger screens, and a vertical layout on smaller screens.
-   `2xl:gap-72 lg:gap-52 md:gap-24 gap-7`: This is used to adjust the gap between the flavor cards on different screen sizes.
-   `flex-nowrap`: This prevents the flavor cards from wrapping to the next line.

## `drinks` and `elements`

We use the following styling for the `drinks` and `elements`:

-   `.drinks`: `@apply absolute left-1/2 -translate-x-1/2 bottom-0 md:h-full h-80`
-   `.elements`: `@apply absolute md:top-0 md:bottom-auto bottom-10 w-full`

These classes are used to position the images within each flavor card. They are positioned absolutely and their position is adjusted on different screen sizes.
