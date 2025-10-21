# Hero Section Documentation

This document provides a detailed explanation of the styling and animations used in the `HeroSection` component.

## `hero-container`

We use the following styling for the `hero-container`: `@apply relative bg-milk w-screen h-dvh overflow-hidden`

-   `relative`: We use `relative` because we want to position the child elements of this container relative to the container itself, not the entire page. This is crucial for the video background and the `hero-content` to be positioned correctly.
-   `bg-milk`: This sets the background color to a custom color defined in the `@theme` section of `index.css`.
-   `w-screen`: This sets the width of the container to `100vw`, which means it will fill the entire width of the screen.
-   `h-dvh`: This sets the height of the container to `100vh`, which means it will fill the entire height of the screen.
-   `overflow-hidden`: This is used to prevent the child elements from overflowing the container. This is important for the video background, which might otherwise cause scrollbars to appear.

## `hero-content`

We use the following styling for the `hero-content`: `@apply relative z-10 w-full h-full flex flex-col 2xl:justify-center items-center translate-y-10 2xl:pt-0 md:pt-32 pt-24`

-   `relative`: We use `relative` because the parent container is `relative` and we want to place this div relative to the parent container and not the entire page.
-   `z-10`: This sets the `z-index` to `10`, which ensures that the content is displayed on top of the video background.
-   `w-full`: This sets the width of the container to `100%`.
-   `h-full`: This sets the height of the container to `100%`.
-   `flex flex-col 2xl:justify-center items-center`: This uses `flexbox` to center the content both horizontally and vertically.
-   `translate-y-10 2xl:pt-0 md:pt-32 pt-24`: This is used to adjust the vertical position of the content on different screen sizes.

## `hero-title`

We use the following styling for the `hero-title`: `@apply text-dark-brown 2xl:text-[8.5rem] md:text-[6.5rem] text-[3.3rem] font-bold uppercase leading-[9vw] tracking-[-.35vw] 2xl:mb-0 mb-5`

-   `text-dark-brown`: This sets the text color to a custom color defined in the `@theme` section of `index.css`.
-   `2xl:text-[8.5rem] md:text-[6.5rem] text-[3.3rem]`: This defines the responsive font size of the title.
-   `font-bold`: This sets the font weight to `bold`.
-   `uppercase`: This makes the text uppercase.
-   `leading-[9vw]`: This sets the line height to `9vw`, which is a responsive value that depends on the screen width.
-   `tracking-[-.35vw]`: This sets the letter spacing to `-0.35vw`, which is a responsive value that depends on the screen width.
-   `2xl:mb-0 mb-5`: This is used to adjust the bottom margin of the title on different screen sizes.
