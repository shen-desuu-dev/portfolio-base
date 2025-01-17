for the image part just do "/name_of_the_image.png_or.jpg"
this is where we edit our information ./src/types/config.ts

```js
import type {
  NavBarLink,
  SocialLink,
  Identity,
  AboutPageContent,
  ProjectPageContent,
  BlogPageContent,
  HomePageContent,
} from "./types/config";

export const identity: Identity = {
  name: "", // your name
  logo: "/logo.png",
  email: "", // your email
};

export const navBarLinks: NavBarLink[] = [
  {
    title: "Home",
    url: "/",
  },
  {
    title: "About",
    url: "/about",
  },
  {
    title: "Projects",
    url: "/projects",
  },
  {
    title: "Blog",
    url: "/blog",
  },
];

export const socialLinks: SocialLink[] = [
  {
    title: "",
    url: "",
    icon: "mdi:your_image_name",
    // external is when it should create another tab
  },
];

// Home (/)
export const homePageContent: HomePageContent = {
  seo: {
    title: "", // your name
    description: "", // your personal description
    image: identity.logo,
  },
  role: "Your role",
  description: "", // your general information
  socialLinks: socialLinks,
  links: [
    {
      title: "My Projects",
      url: "/projects",
    },
    {
      title: "About Me",
      url: "/about",
    },
  ],
};

// About (/about)
export const aboutPageContent: AboutPageContent = {
  seo: {
    title: "About | Your Name",
    description: "", // general description again
    image: identity.logo,
  },
  subtitle: "Some information about myself",
  about: {
    description: ``, // Describe yourself
    image_l: {
      url: "", // you can do /logo_name.png or .jpg
      alt: "Left Picture",
    },
    image_r: {
      url: "", // you can do /logo_name.png or .jpg
      alt: "Right Picture",
    },
  },
  work: {
    description: ``, // What you do for work
    items: [
      {
        title: "Your job title",
        company: {
          name: "Freelance",
          image: "/logo.png",
          url: "", // your url
        },
        date: "2021 - Present",
      }, // this can be repeated
    ],
  },
  connect: {
    description: `I'm always interested in meeting new people and learning new things. Feel free to connect with me on any of the following platforms.`, // Markdown is supported
    links: socialLinks,
  },
};

// Projects (/projects)
export const projectsPageContent: ProjectPageContent = {
  seo: {
    title: "Projects | Your Name",
    description: "Check out what I've been working on.",
    image: identity.logo,
  },
  subtitle: "Check out what I've been working on.",
  projects: [
    {
      title: "Project 1",
      description: "Project 1 Description",
      image: "", // you can do /logo_name.png or .jpg
      year: "", // the year
      url: "", // url to website or page
    },
  ],
};

// Blog (/blog)
export const blogPageContent: BlogPageContent = {
  seo: {
    title: "Blog | Your Name",
    description: "Thoughts, stories and ideas.",
    image: identity.logo,
  },
  subtitle: "Thoughts, stories and ideas.",
};
```