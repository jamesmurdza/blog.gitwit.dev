---
title: "Add a feature to an app with an AI prompt"
pubDate: "2023-05-09"
slug: "add-a-feature-to-an-app"
description: "In this article, I will show you how to use an AI helper to co-create a full-stack web app."
hero: "/images/Banner1.png"
tags: ["go"]
layout: "../../layouts/BlogPostLayout.astro"
---

In the last post, you learned how to build and test a simple full-stack app using GitWit. We used one prompt to make an that allows the user to draw doodles within the browser. Now, we will see how we can add a feature to the app!

All of the code generated in this example is also <a href="https://github.com/gitwitapp/doodle-app/" target="_blank">here</a> on GitHub.

## Generate a revision

To create a new revision of a project, click "Make a revision" and enter a prompt. It helps to be specific in how the app should behave when describing a feature. For example "Add a button that when clicked..." rather than "Allows the user to...". For this example, let's add a save feature. Let's try the prompt: "Add a Save button to the page. When the button is clicked, the browser opens a PNG version of the current drawing."

Tip: You can generate the same version multiple times to compare results. Just open the "Make a revision" page in multiple tabs.

<img src="/images/5.gif" />

After less than a minute, GitWit generates a new version of the same repository. More specifically, it creates a new branch on the same repository with one or more new commits. After running a prompt above, there was a new commit adding some JavaScript code to export the current drawing.

## Test the app

As seen in the last post, testing a GitWit project is as simple as opening a GitHub codespace. Assuming we already have a codespace running, we will need to check out the new branch before we can access the new version.

```
git fetch
git checkout add-save-button-to-page
```

The name of the current branch can always be readily found at the top of the project page in GitWit.

<img src="/images/6.gif" />

If the code is correct, we can simply run the app as we did previously to access the new changes.

However, as mentioned earlier, this is not always the case. In this case, the code outputted by GitWit was incomplete, and running the code produced an error. We will see how to debug that error in the next post.

Want to try GitWit? Get started at <a href="https://www.gitwit.dev/">gitwit.dev</a>!