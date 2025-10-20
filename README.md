# Spylt - An Awwwards winning website

Build a professional, award-winning website using React, TailwindCSS, and GSAP with detailed animations, reusable clean code, and advanced techniques for creating cinematic transitions and parallax effects.

## Setup

- npm create vite@latest splyit
- npm install tailwindcss @tailwindcss/vite
- Download the public folder and the index.css file above into your codebase
- npm i gsap @gsap/react react-responsive

## Coding

### Components

#### Navbar

- The navbar contains a single logo image. We want the navbar to be ontop of the pages also we give it responsive padding to push the content away from the topleft corner. based on the conditions we give it these styles.
  - We give some responsive size constraints to the logo image also
- View [here](src/components/Navbar.jsx)

#### Hero Section

- We give the section a classname of `bg-main-bg` which is a custom css we have defined within our index.css file.
  - We give the nested div a classname of `hero-container`, a custom css
    - In a nested img, we get the hero-img from public/images. We want to center this image at the bottomCenter and give it responsive scale: `absolute left-1/2 bottom-0 -translate-x-1/2 object-auto scale-100 md:scale-150`
  - For the main content of the hero section, we give a classname of `hero-content opacity-0`. We will animate it to opacity 100 using gsap later.
    - In a nested div, we give a classname of `overflow-hidden`, this is important as we will use gsap to animate it later, giving it a reveal effect.
      - In a nested h1 tag, we give a classname of `hero-title`.
    - In a nested div, we give a classname of `hero-text-scroll`, this div will take a clipPath. We will animate the clipPath to reveal the text in this div. So we get the clipPath: a rectangle whose stating point is the center, which we will animate outward to reveal the text within
      - A nested div with classname `hero-subtitle`
        - An h1 tag
    - We give an h2 tag
    - In a div tag, we give a classname of `hero-button`
      - A button

##### Text Reveal Animation

- We will use the useGSAP hook, this means we dont have to manually cleanup the animation state. This basically tells React to "animate these things after the component mounts"
  - First we animate the `hero-title` using a SplitText because we want an animation where each character appears one by one, applying a slight delay to each.
  - Then we create a timeline with a delay of 1 second meaning the animation will wait for 1 second before starting.
  - Then we use the timeline to animate the hero-content to a desired state. This first to: will move the text from the bottom towards the top a bit and with an opacity of 1 to show it
  - Then the next to will target the `hero-text-scroll`: we want to reveal the text in the clipPath so we animate it from it's current state to a full rectangle, we give it a duration of 1 second so the animation lasts that long, we also want this animation to start earlier than the rest so we add a "-=0.5" as a second parameter to the second to. This will make the second to start at 0.5secs before the end of the first animation's to because the first to naturally starts at 0.5 secs. They will start at the sametime
  - Now we want to animate the `hero-title` chars. we will use from this time and not to because we want this animation to be the initial state. So we will target the titleSplit.chars we created earlier using the SplitText plugin: we use yPercent of 200 so each char starts at 200% below it's final state, then a stagger to make each char wait for 0.02 secs, then an ease effect.
  - Next we want to create an animation for the entire `hero-section` and tie it to the scrollbar such that when we scroll up the entire section moves from a rectangle to a different shaping giving it s nice scroll effect: We create a new timeline for it and use the ScrollTrigger plugin object because the animation will be triggered by the scroll. we start the animation at 1% top, meaning start this when the top of the hero section hits the top of the viewport but we push the hero section top down by 1% so this will be triggered when we begin to scroll up and we end when the bottom of the section hits the top of the viewport. Then we use scrub to tie the animation to the scrollbar. We also have to go to App.jsx to register the ScrollTrigger plugin for this to work
  - Now, the real animation, we want to rotate the entire section by 7 degrees, scale it down by 10% and slide it down by 30 and ease. This gives it a nice effect. So we will animate from the current state to this state on scroll

#### Message Section

- A section with classname `message-content`
  - A div with classname `container mx-auto flex-center py-28 relative`
    - A div with classname `size-full`
      - A div with classname `msg-wrapper`
        - An h1 tag, with classname `first-message`
        - A div with classname `msg-text-scroll`
          - A div with classname `bg-light-brown md:pb-5 pb-3 px-5`
            - An h2 tag with classname `text-red-brown`
        - An h1 tag with classname `second-message`
    - A div with classname `flex-center md:mt-20 mt-10`
      - A div with classname `max-w-md flex-center px-10 overflow-hidden`
        - A p tag

##### ScrollSmoother Plugin

- Now let us add some animation to this section. As usual, the useGSAP hook
  - We want to split the first message and second message so we will again use SplitText here as well but this time we want to split based on words not chars. We also do same for the p tag within the `message-content` and for this we want to animate the words and lines then we add a lineClass called `paragraph-line` to be applied to each line of the paragraph
  - We animate the words of firstMsgSplit from the low opacity to 100% of the color.
  - We add a scrollTrigger to tie the animation of the words to scrollbar. We will trigger the animation when we scroll to the `message-content`, starting it when the top of the section scrolls to the center of the laptop screen(viewport), and ending it by moving the end 30% from the top and to end when that aligns with the laptop center so the animation is fast.
  - We animate the words of the secondMsgSplit also, but this time we move the scrollTrigger start from top of the div(if we leave it at top of the div it will also be trigger like the first, we only want it to be triggered when the first wordSplit animates) to the top of the h1 of the `second-message`.
  - Now we animate the `.msg-text-scroll`, first we create a timeline for it with a delay and a scrollTigger what will start when the top of it's div get to the 60% of the viewport
  - Then we will animate it from the current state to: with a duration of 1 second, we will use a clipPath to animate that reveal effect
  - Then we create a timeline for the `message-content p`(timeline because we want it's animation to start after previous animations end), we define the scrollTrigger on this to start when the top of this div hits the center of the viewport
  - Next, we animate this timeline using the from: we want the words to start 300% below it's current postion, rotated at 3 degrees(meaning it will start at 3degrees away from 180 to 180degrees), with a duration of 1 and a stagger for each word at 0.02 and an ease in.Out

#### Flavors Section

- Create a section with classname of `flavor-section`
  - A div with classname that is flex responsive(row for lg; col for normal), items center with full height and relative
    - We render the div with classname of flex-none so the title doesnt shrink or scale, a responsive with and height and a margin-top for md screens and up. for xl screens reset the margin-top to 0.
      - Within it we render the <FlavorTitle/>, a component we create beneath this one. A div with classname of `general-title`

##### Horizontal Scrolling

#### Nutrition Section

- Create a section with a classname of `nutrition-section`.
  - An img

#### Benefit Section

- Create a section with a classname of `nutrition-section`.

#### Scroll-Sync Clip-Path, Reveal Animation

#### Scroll-Sync Video, Reveal Animation

#### Testimonial Section

##### Pinning Multiple Elements
