# Astro Social Share

Social media share buttons for your Astro site

## Features
* No dependencies, external scrips
* Share buttons for:
  * Facebook
  * Hacker News
  * LinkedIn
  * Reddit
  * Twitter
* Icons included

## Demo
[Demo site](https://mckerlie.com/posts/migrating-your-blog-from-hugo-to-astro)

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

You can also import individual buttons

```js
import { 
  FacebookShareButton,
  HackerNewsShareButton,
  LinkedInShareButton,
  RedditShareButton,
  TwitterShareButton
} from "astro-social-share";

<TwitterShareButton 
    description="Description of the page/post"
    via="YourTwitterAccount"
/>
<FacebookShareButton />
<HackerNewsShareButton title={title}/>
<FacebookShareButton />
<RedditShareButton title={title} />
```