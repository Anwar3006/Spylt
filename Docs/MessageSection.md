# Message Section Documentation

This document provides a detailed explanation of the styling and animations used in the `MessageSection` component.

## `message-content`

We use the following styling for the `message-content`: `@apply bg-[#7f3b2d] text-milk min-h-dvh overflow-hidden flex justify-center items-center relative z-20`

-   `bg-[#7f3b2d]`: This sets the background color to a custom dark brown color.
-   `text-milk`: This sets the text color to a custom light milk color.
-   `min-h-dvh`: This sets the minimum height of the container to `100vh`, which means it will fill at least the entire height of the screen.
-   `overflow-hidden`: This is used to prevent the child elements from overflowing the container.
-   `flex justify-center items-center`: This uses `flexbox` to center the content both horizontally and vertically.
-   `relative`: We use `relative` because we want to position the child elements of this container relative to the container itself.
-   `z-20`: This sets the `z-index` to `20`, which ensures that this section is displayed on top of the previous sections.

## `msg-wrapper`

We use the following styling for the `msg-wrapper`: `@apply 2xl:text-[8.5rem] md:text-8xl text-5xl font-bold uppercase leading-[9vw] tracking-[-.35vw] flex flex-col justify-center items-center md:gap-24 gap-14`

-   `2xl:text-[8.5rem] md:text-8xl text-5xl`: This defines the responsive font size of the text.
-   `font-bold`: This sets the font weight to `bold`.
-   `uppercase`: This makes the text uppercase.
-   `leading-[9vw]`: This sets the line height to `9vw`, which is a responsive value that depends on the screen width.
-   `tracking-[-.35vw]`: This sets the letter spacing to `-0.35vw`, which is a responsive value that depends on the screen width.
-   `flex flex-col justify-center items-center`: This uses `flexbox` to center the content both horizontally and vertically.
-   `md:gap-24 gap-14`: This is used to adjust the gap between the text elements on different screen sizes.

## `msg-text-scroll`

We use the following styling for the `msg-text-scroll`: `@apply rotate-[3deg] 2xl:translate-y-5 -translate-y-5 absolute z-10 border-[.5vw] border-[#7f3b2d]`

-   `rotate-[3deg]`: This rotates the element by `3` degrees.
-   `2xl:translate-y-5 -translate-y-5`: This is used to adjust the vertical position of the element on different screen sizes.
-   `absolute`: This positions the element relative to its parent container.
-   `z-10`: This sets the `z-index` to `10`, which ensures that this element is displayed on top of the other elements in this section.
-   `border-[.5vw] border-[#7f3b2d]`: This sets a border with a responsive width and a custom color.
