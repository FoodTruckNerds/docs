# How to Set Up Tailwind

Tailwind can be used in 2 main ways: using a public CDN (content delivery network) over the internet, or installing Tailwind in the project folder.

## Option A: Use a public CDN

Include this in the <head> section of the HTML: `<script src="https://cdn.tailwindcss.com"></script>`. When you import the script, Tailwind's script scans your HTML file and imports the individual Tailwind CSS classes your page uses. Importing from CDN is recommended for testing and drafting. Final production should use local Tailwind. This option requires you to use Tailwind from the HTML file. Using lots of Tailwind will cause your HTML file to get visually messy and large. A cleaner way to do this is using Tailwind in your CSS file with your own class names that combine Tailwind classes. To do this, use option B.

```html
<html>
   <head>
      <script src="https://cdn.tailwindcss.com"></script>
   </head>
   <body>
      <div class="insert tailwind classes here separated by spaces">
         <div> Stuff </div>
         <div> Stuff </div>
      </div>
   </body
</html>
```

## Option B: Install Tailwind in the project

Installing Tailwind locally provides faster loading, guarantees your website looks the same, even if Tailwind releases an update that changes their classes, and lets you clean up your HTML by moving the Tailwind classes into your CSS file and creating custom classes that combine Tailwind classes into logical components. When you use the `@import` command in the CSS file, Tailwind scans your HTML and CSS files and generates a new Tailwind CSS file that contains only the subset of features you use from Tailwind, ensuring that your website loads only what you need.

Prerequisites:

- Install Node.js
- Reboot VSCode if open, to reload PATH variables that Node installer modified.
- Open a terminal in the project main directory.
- Install using the instructions for the CLI option below (tailored for our project).

Installation Processes:

1. [CLI (for use with raw HTML, CSS, JS):](https://tailwindcss.com/docs/installation/tailwind-cli)

   - Run `npm install tailwindcss @tailwindcss/cli`
   - Copy `@import "tailwindcss";` into the top of your style.css file to be able to use Tailwind directly in your CSS styles, then you can build your own complex classes or components using Tailwind, and mix and match with regular CSS.
   - Build the Tailwind CSS file using the CLI interface: `npx @tailwind/cli -i ./styles.css -o ./tailwind/styles.css` IMPORTANT: This file has to be rebuilt every time you change your 'styles.css'. You can use the --watch flag to make the command keep listening for changes. It will stay running in the terminal: `npx @tailwind/cli -i ./styles.css -o ./tailwind/styles.css --watch`

2. [Vite (for frameworks like Laravel, SvelteKit, React Router, Nuxt, SolidJS, etc):](https://tailwindcss.com/docs/installation/using-vite)

3. [PostCSS (for frameworks like Next.js and Angular):](https://tailwindcss.com/docs/installation/using-postcss)
