# 2023 Intro Web Assignment

## Description

This project is an assignment of my first go at web development. Using HTML, CSS, and JavaScript. It is a multi page website based around the theme of me. I chose this theme because it gave me a way to put a few of my hobbies and interests into one place to display them to whoever was interested in it. I used a website for this task because it was the best way to display the information I wanted to show. And it was a good practice for future web endeavours. Some of the biggest challenges with this project was learning how to use a framework rather than just vanilla HTML, CSS, and Javascript which I have lightly touched on in the past.

## The Framework

For this project I used the [SvelteKit](https://kit.svelte.dev/ "kit.svelte.dev") framework because it is a lot more powerful and once you are used to it more intuitive from a programming perspective than vanilla web design. The biggest part of using SvelteKit over vanilla is the ability to have components which can be reused to allow for more DRY code.

## How To Use

To run the program first you need to have node packet manager installed. Once that is done inside of the project folder open a terminal and run the `npm i` command (short for `npm install`). Once it has finished installing to run the dev build you can run the `npm run dev -- --open` command and it will open in your browser. Or if you want to run a build of it run the `npm run build` command.

## Known Bugs and Future Plans

Currently the only bug I am aware of is with the Fetching from the Unsplash API. Where sometimes instead of two descriptions the images only come with one. Howwever, from my testing the first description will always come with one. So the code functions around that. If it happened to not come with an image. It would cause an error.

## Unsplash API 

Thank you to the [Unsplash API](https://unsplash.com/ "unsplash.com") for providing a free API for images on the internet. This projects gallery page relies on them for the fish images provided

## Design Document
[Link](https://github.com/Christian-Irvine/svelte_2023_webdev1/blob/master/DESIGN.md)
This is a link to the design document of where I got inspiration from for my website.
