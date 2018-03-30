# Seff_CPWeek7
# Project 7 - WordPress Pentesting

Time spent: **X** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1.  Authenticated Stored Cross-Site Scripting via Image Filename
  - [ ] Summary: There was no sanitation in image filenames in WP version 4.2
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.10
  - [ ] GIF Walkthrough: ![](https://github.com/etseff/Seff_CPWeek7/blob/master/NA1.gif)
  - [ ] Steps to recreate: Upload a new image, change the filename to any script, post the image and the script will run.
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/c9e60dab176635d4bfaaf431c0ea891e4726d6e0)
2.  Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL embeds
  - [ ] Summary: There was no sanitation in YouTube embedded links in WP version 4.2
    - Vulnerability types:
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [ ] GIF Walkthrough: ![](https://github.com/etseff/Seff_CPWeek7/blob/master/NA2.gif)
  - [ ] Steps to recreate: Create a new post and add the beginning of a YouTube link, with script instead of the end of the unique URL for a real video. Then, highlight the link and press the link button. Press upload and the script will run.
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8)
3. Unauthenticated Stored Cross-Site Scripting
  - [ ] Summary: Super large comments leave a vulnerability for cross-site scripting
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1 
  - [ ] GIF Walkthrough: ![](https://github.com/etseff/Seff_CPWeek7/blob/master/NA3.gif)
  - [ ] Steps to recreate: Post a comment as a site visitor with over 64 kb of text- in the example, a large chunk of text was copied from a random website. Include desired script in the comment and post the comment and the script will run.
  - [ ] Affected source code:
    - [Link 1](https://klikki.fi/adv/wordpress2.html)
4.  Authenticated Stored Cross-Site Scripting
  - [ ] Summary: There was no sanitation in posts in WP version 4.2
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.3
  - [ ] GIF Walkthrough: ![](https://github.com/etseff/Seff_CPWeek7/blob/master/NA4.gif)
  - [ ] Steps to recreate: Create a post. Write script in the post and upload the post. Visit the post on the website and the script will run.
  - [ ] Affected source code:
    - [Link 1](https://klikki.fi/adv/wordpress3.html)
