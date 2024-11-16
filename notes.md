# Xora UI/UX SaaS Website Development Notes

## Introduction

- I am setting up this solution as part of learning and familiarizing the approaches used while building a SaaS UI application.
- I am taking Reference from :
  - Youtube : https://youtu.be/ukiGFmZ32YA
  - GitHub : https://github.com/adrianhajdin/xora/blob/main/README.md

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
