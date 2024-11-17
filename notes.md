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