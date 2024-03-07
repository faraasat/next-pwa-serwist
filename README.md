# Next PWA @Serwist

### This Example Code is a Part of an Article: Activating PWA in Next.js 13+ App Directory Using @Serwist — Simple Guide

<hr />

##### Live Url: [Deployment](https://next-pwa-serwist.vercel.app/)
##### Article Link: [Medium](https://faraasat.medium.com/activating-pwa-in-next-js-13-app-directory-using-serwist-simple-guide-b84d2a29da9c)

<hr />

### Introduction: 
Progressive Web Apps (PWAs) combine the best of web and native apps, delivering a more app-like experience to users. In this guide, we’ll explore how to make a Next.js app with an App Directory into a PWA using the @serwist library.

### Benefits of PWAs: 
PWAs offer several advantages, including offline access, app-like behavior, push notifications, discoverability, and automatic updates. Notable companies like AliExpress, Twitter Lite, and Forbes have embraced PWAs.

### Adding PWA Support to Next.js:

#### 1. Create the Next.js App:
- Use `npx create-next-app@latest` to set up a new Next.js project.
- Choose prompts for project name, TypeScript, ESLint, Tailwind CSS, src/ directory, and App Router.
#### 2. Install Required Packages:
- Install the following packages: `@serwist/next`, `@serwist/precaching`, and `@serwist/sw`.
#### 3. Configure the Package:
- If using `next.config.mjs`:

  ```Javascript
  import withSerwistInit from "@serwist/next";
  const withSerwist = withSerwistInit({
    cacheOnFrontEndNav: true,
    swSrc: "src/sw.ts",
    swDest: "public/sw.js",
    reloadOnOnline: true,
    disable: process.env.NODE_ENV === "development",
    // ... other options
  });
  export default withSerwist(nextConfig);
  ```

  
- If using `next.config.js`:

  ```Javascript
    const withSerwist = require("@serwist/next").default({
    cacheOnFrontEndNav: true,
    swSrc: "src/sw.ts",
    swDest: "public/sw.js",
    reloadOnOnline: true,
    disable: process.env.NODE_ENV === "development",
    // ... other options
    });
  ```

### Conclusion:
By following these steps, you can activate PWA features in your Next.js app using @serwist, enhancing user experiences and making your app more robust and accessible.

### Result:
![screencapture-next-pwa-serwist-vercel-app-2024-03-07-11_02_41](https://github.com/faraasat/next-pwa-serwist/assets/63093876/7430980e-fecf-4814-a931-73fdf8cf863e)
