# Footer Section Documentation

This document provides a detailed explanation of the styling used in the `FooterSection` component.

## `footer-section`

We use the following styling for the `footer-section`: `@apply 2xl:min-h-dvh overflow-hidden relative bg-[#222123]`

-   `2xl:min-h-dvh`: This sets the minimum height of the container to `100vh` on extra-large screens.
-   `overflow-hidden`: This is used to prevent the child elements from overflowing the container.
-   `relative`: We use `relative` because we want to position the child elements of this container relative to the container itself.
-   `bg-[#222123]`: This sets the background color to a custom dark gray color.

## `social-btn`

We use the following styling for the `social-btn`: `@apply border border-[#faeade33] md:size-[5vw] size-14 md:p-0 p-3 flex justify-center items-center rounded-full hover:bg-[#ffffff1a] transition-colors cursor-pointer z-20`

-   `border border-[#faeade33]`: This sets a border with a custom color.
-   `md:size-[5vw] size-14`: This defines the responsive size of the button.
-   `md:p-0 p-3`: This is used to adjust the padding of the button on different screen sizes.
-   `flex justify-center items-center`: This uses `flexbox` to center the content of the button.
-   `rounded-full`: This makes the button a circle.
-   `hover:bg-[#ffffff1a]`: This changes the background color of the button on hover.
-   `transition-colors`: This animates the change in background color.
-   `cursor-pointer`: This changes the cursor to a pointer on hover.
-   `z-20`: This sets the `z-index` to `20`, which ensures that the button is displayed on top of other elements.

## `copyright-box`

We use the following styling for the `copyright-box`: `@apply 2xl:absolute w-full md:px-10 px-5 pt-7 pb-2 bottom-0 text-milk opacity-50 md:text-lg font-paragraph flex gap-7 md:flex-row flex-col-reverse md:justify-between justify-center items-center`

-   `2xl:absolute`: This positions the element absolutely on extra-large screens.
-   `w-full`: This sets the width of the container to `100%`.
-   `md:px-10 px-5`: This is used to adjust the horizontal padding of the container on different screen sizes.
-   `pt-7 pb-2`: This sets the top and bottom padding of the container.
-   `bottom-0`: This positions the element at the bottom of its container.
-   `text-milk`: This sets the text color to a custom light milk color.
-   `opacity-50`: This makes the text semi-transparent.
-   `md:text-lg`: This sets the font size on medium and larger screens.
-   `font-paragraph`: This sets the font family to a custom font defined in the `@theme` section of `index.css`.
-   `flex gap-7 md:flex-row flex-col-reverse md:justify-between justify-center items-center`: This uses `flexbox` to create a responsive layout.
