# Astro Social Share

Social media share buttons for your Astro site 

![npm](https://img.shields.io/npm/v/astro-social-share)

## Features
* No dependencies or external scripts
* Share buttons for:
  * Facebook
  * Hacker News
  * LinkedIn
  * Reddit
  * Twitter
  * WhatsApp
* Icons included from https://simpleicons.org/

## Demo
[Example](https://mckerlie.com/posts/improving-the-sharing-experience-in-astro)

## Install

`npm i astro-social-share`

## Usage

Simple, include all links

```js
import { SocialShare } from "astro-social-share";

<SocialShare
    description="Description of the page/post"
    via="YourTwitterAccount"
    title="Page Title"
/>
```

If you'd like to customize the share bar you can import the individual buttons and pass them into the `<SocialShare />` component.

```astro
---
import { 
  FacebookShareButton,
  HackerNewsShareButton,
  LinkedInShareButton,
  RedditShareButton,
  TwitterShareButton,
  WhatsAppShareButton,
  SocialShare
} from "astro-social-share";

const BUTTONS = [TwitterShareButton, FacebookShareButton]
---

<SocialShare
    buttons={BUTTONS}
    description="Description of the page/post"
    via="YourTwitterAccount"
    title="Page Title"
/>
```

## Using your own icons

If you'd like to pass in your own icons you can do so through the individual components.

```astro
---
import { 
  FacebookShareButton,
  TwitterShareButton,
} from "astro-social-share";

---

<FacebookShareButton>
  <svg>...</svg>
</FacebookShareButton>

<TwitterShareButton
    description="Description of the page/post"
    via="YourTwitterAccount"
    title="Page Title"
>
  <img ... />
</TwitterShareButton>
```

## Using your own CSS

If you'd like to style the share bar and icons you can pass in a global <style> component to a slot named `astro-social-share-css`

```astro
<SocialShare
    description="Description of the page/post"
    via="YourTwitterAccount"
    title="Page Title"
>
<slot name="astro-social-share-css">
  <style is:global>
    .astro-social-share {
        margin: 20px 0px;
        height: 24px;
    }
    .astro-social-share a {
        text-decoration: none;
        margin-right: 10px;
    }
    .astro-social-share svg {
        height: 24px;
    }
  </style>
</slot>
```

