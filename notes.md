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
  import React from 'react'

    const App = () => {
    return (
        <h1 className="text-3xl font-bold underline">
        Hello world!
        </h1>
    )
    }

    export default App
  ```
- Bring public folder from [Assets](https://github.com/adrianhajdin/xora/blob/main/README.md#-assets) and replace existing public folder.
- Update index.html to change favicon and update page title for SaaS landing page
