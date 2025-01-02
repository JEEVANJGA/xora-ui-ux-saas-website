# Xora UI/UX SaaS Website Development Notes

## Introduction

- I am setting up this solution as part of learning and familiarizing the approaches used while building a SaaS UI application.
- I am taking Reference from :
  - [Youtube](https://youtu.be/ukiGFmZ32YA)
  - [GitHub](https://github.com/adrianhajdin/xora/blob/main/README.md)

## Steps

### Step-1

- Setup react solution with vite
- run `npm create vite@latest`
- choose `./` when project name is asked to setup the solution in same working directory.
- choose React as framework, javascript as variant
- run `npm i` to install packages

### Step-2

- Refactor App component to simplify structure and remove unused elements
- Add Tailwind CSS and PostCSS dependencies to package.json
  - run `npm install -D tailwindcss postcss autoprefixer`
- Add PostCSS and Tailwind CSS configuration files
  - run `npx tailwindcss init -p`

### Step-3

- Configure your template paths : Add the paths to all of your template files in your tailwind.config.js file.
  - Copy content from [**tailwind.config.js**](https://github.com/adrianhajdin/xora/blob/main/README.md#%EF%B8%8F-snippets) and update in the local tailwind.config.js file.
- Add the Tailwind directives to your CSS : Add the @tailwind directives for each of Tailwind’s layers to your ./src/index.css file.
  - Copy content from [**index.css**](https://github.com/adrianhajdin/xora/blob/main/README.md#%EF%B8%8F-snippets) and update in the local index.css file.
- Start using Tailwind’s utility classes to style your content.

  ```jsx
  import React from "react";

  const App = () => {
    return <h1 className="text-3xl font-bold underline">Hello world!</h1>;
  };

  export default App;
  ```

- Bring public folder from [Assets](https://github.com/adrianhajdin/xora/blob/main/README.md#-assets) and replace existing public folder.
- Update index.html to change favicon and update page title for SaaS landing page

### Step-4

- Add react-scroll dependency to package.json
  - `npm install react-scroll`
- Implement Header component and update App structure
- Add clsx dependency to package.json.
  - `npm i clsx`

### Step-5

- Add Header
- Refactor Header component to include responsive navigation and toggle functionality
  - Uses useState to manage the state of the navigation menu (isOpen).
  - Renders a fixed header with a logo and navigation links.
  - Uses `clsx` to conditionally apply classes based on the `isOpen` state.
  - Contains a navigation menu with links to "Features", "Pricing", "FAQ", and "Download".
  - Includes a button to toggle the navigation menu on smaller screens.
  - Displays background images for decorative purposes.

### Step-6

- Add Hero section and Button component with Marker
  - Created a new Hero component to serve as the hero section of the landing page.
  - Imported React, Element and Link from react-scroll, and Button from the components directory.
  - Added a section with specific padding classes for different screen sizes.
  - Used Element from react-scroll to create a scrollable section named "hero".
  - Included a container div with a maximum width and relative positioning.
  - Added a caption with the text "Video Editing".
  - Added a heading with the text "Amazingly Simple" and various responsive styles.
  - Added a paragraph describing the XORA AI Video Editor.
  - Included a LinkScroll component to smoothly scroll to the "features" section when the button is clicked.
  - Added a Button component with an icon and text "Try it now".

### Step-7

- Add Features Component
  - Created a new Features component to display a list of features.
- Imported Dependencies:
  - Imported React from "react".
  - Imported Element from "react-scroll".
  - Imported features from the constants file.
  - Imported Button from the components directory.
- Implemented Features Section:
  - Added a section element to contain the features.
  - Used Element from react-scroll to create a scrollable section named "features".
  - Added a container div with specific classes for styling.
  - Used a ul element to list the features.
  - Mapped over the features array to dynamically create li elements for each feature.
  - Each li element includes:
    - An icon image with specific styles.
    - A title displayed as a heading with specific styles.
    - A decorative vertical line.
    - A border that changes on hover.
- These changes enhance the landing page by adding a visually appealing features section that dynamically displays feature information from the constants file.

### Step-8
- Enhance Header component with scroll detection and dynamic styling
- Add react-countup dependency for animated number counting
  - run `npm i react-countup`

### Step-9

- Add Pricing Component
  - Created a new Pricing component to display different pricing plans.
  - Imported necessary dependencies such as React and clsx.
  - Implemented the Pricing component with the following features:
    - A section to contain the pricing plans.
    - Conditional rendering of background elements.
    - Dynamic styling based on the index of the pricing plan.
    - Display of plan logos with different sizes and positions.
    - Structured layout for each pricing plan with specific styles.
- Integrate Pricing Component into App
  - Imported the Pricing component into the main application file (e.g., App.jsx).
  - Added the Pricing component to the application's component tree to ensure it is rendered on the page.
- Update Header Navigation Link to Lowercase
  - Modified the Header component to update the navigation links to use lowercase text.
  - Ensured that the navigation links are consistent with the desired styling and format.

### Step-10

- Add react-slidedown dependency
  - run `npm i react-slidedown --legacy-peer-deps`
- Add Faq Component
  - Created a new Faq component to display frequently asked questions.
  - Imported necessary dependencies such as React and Element from react-scroll.
  - Imported the faq data from the constants file.
  - Imported the FaqItem component.
  - Implemented the Faq component with the following features:
    - A section to contain the FAQ items.
    - Used Element from react-scroll to create a scrollable section named "faq".
    - Divided the FAQ items into two columns for better layout and readability.
    - Used the faq array to dynamically create FaqItem components for each FAQ item.
    - Added a vertical line between the two columns for visual separation.
    - Added a heading and a subheading to the FAQ section.
  - Added FaqItem Component:
    - Created a new FaqItem component to display individual FAQ items.
    - Imported necessary dependencies such as React.
    - Imported SlideDown from react-slidedown to add slide-down animation for the FAQ answers.
    - Implemented the FaqItem component with the following features:
      - A container for each FAQ item.
      - Displayed the question and answer for each FAQ item.
      - Added styles for better readability and visual appeal.
      - Used SlideDown to animate the display of the answer when the question is clicked.
  - Installed react-slidedown Package:
    - Added react-slidedown to the project dependencies.
    - Ran `npm install react-slidedown` to install the package.
  - Integrated Faq Component into App:
    - Imported the Faq component into the main application file (e.g., App.jsx).
    - Added the Faq component to the application's component tree to ensure it is rendered on the page.
  - Updated Header Navigation Link to Include FAQ:
    - Modified the Header component to include a navigation link to the FAQ section.
    - Ensured that the navigation link is consistent with the desired styling and format.

### Step-11

- Add Testimonials Component
  - Created a new Testimonials component to display user testimonials.
  - Imported necessary dependencies such as testimonials from the constants file and TestimonialItem from the components directory.
- Implement Testimonials Section
  - Added a section element to contain the testimonials.
  - Used a container div with specific classes for styling.
  - Added a heading and a subheading to the testimonials section.
  - Divided the testimonials into two columns for better layout and readability.
  - Used the testimonials array to dynamically create TestimonialItem components for each testimonial.
  - Each TestimonialItem component includes:
    - The testimonial text.
    - The author's name and other relevant details.
    - Specific styles for better readability and visual appeal.
- Integrate Testimonials Component into App
  - Imported the Testimonials component into the main application file (e.g., App.jsx).
  - Added the Testimonials component to the application's component tree to ensure it is rendered on the page.

  ### Step-12

  - Add Download Component
    - Created a new Download component to provide download options for different platforms.
    - Imported necessary dependencies such as Element from react-scroll, links and logos from the constants file, and Marker from the components directory.
  - Implement Download Section
    - Added a section element to contain the download options.
    - Used Element from react-scroll to create a scrollable section named "download".
    - Added a container div with specific classes for styling.
    - Included a logo and a description paragraph.
    - Created a list of download links for different platforms using the links array.
    - Styled each download link with specific classes and included the Marker component for visual enhancement.
    - Added a preview image for the download section.
    - Created a list of partner logos using the logos array.
  - Integrate Download Component into App
    - Imported the Download component into the main application file (e.g., App.jsx).
    - Added the Download component to the application's component tree to ensure it is rendered on the page.