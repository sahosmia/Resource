```js
/** @type {import('tailwindcss').Config} */
export default {
  content: ["./index.html", "./src/**/*.{js,ts,jsx,tsx}"],
  theme: {
    extend: {
      colors: {
        light: "#ffffff",
        main: "#274C5B",
      },

      backgroundImage: {
        "hero-pattern": "url('/img/banner/hero.png')",
      },
    },

    fontFamily: {
      roboto: ["Roboto"],
      yellowtail: ["Yellowtail"],
      opensans: ["Open Sans"],
    },

    screens: {
      sm: "640px", // => @media (min-width: 640px)
      md: "768px", // => @media (min-width: 768px) 
      lg: "1024px", // => @media (min-width: 1024px)
      xl: "1124px", // => @media (min-width: 1280px)
      "2xl": "1480px", // => @media (min-width: 1280px)
    },

    container: {
      center: true,
      padding: "2rem",
    },
  },
  plugins: [],
};

```
