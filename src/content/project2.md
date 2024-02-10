+++
author="David Evans"
date= "2023-02-10"
linktitle="project2"
title="Project 2"
+++

# Project 2: Web

For this project, the main goal is for you to:

1. Develop a good basic understanding of how the web works and how search engines find content on the web.
2. Create your own website, learning to use raw HTML, version control systems (github), and style sheets (css).

## Getting Started

The website you will create will be hosted using github pages. Github pages has several main advantages as a way of hosting a website (and this is what the course website, [https://computingfor.github.io/](https://computingfor.github.io/), is using. It is _free_, [very reliable](https://www.githubstatus.com/history), scalable (can support around 100GB per month), and (relatively) easy to set up. The main disadvantage, at least compared to a website you host yourself, is that you are giving up control over your content and the web server to github (which is owned by Microsoft). As with any computing service outside your direct control, there is always a risk that it will change in ways that will be unacceptable to you from shutting down to compromising the privacy of your visitors. But, it is a lot of trouble to try and host your own website, and the economies of scale a service like github can take advantage of allow it to provide a high quality service for free to most users. I trust github my most important websites and most of my work data, since it is part of a large company that has a good reputation for not shutting down services arbitrarily and for respecting user data (and github's [former CEO grew up in Charlottesville](https://en.wikipedia.org/wiki/Nat_Friedman) and [Microsoft's Chief Technology Officer](https://en.wikipedia.org/wiki/Kevin_Scott_(computer_scientist)) went to UVA, so they must be trustworthy, at least enough for hosting my websites!). You should make your own decision about which companies to trust with your content, but for this assignment we will provide directions for using github pages and expect this is the best option for everyone in the class. If you do prefer to use something else or self-host, check with me &mdash; if you want to do something that provides at least as much control over your content as github pages does, it will be acceptable (using a form-based hosting provider like wix or squarespace is not an option, though, since those will provide you little understanding of what is actually going on or ability to actually control your website), but youl will need to figure out more on your own.

1. **Create a github account.** Visit [https://github.com/](https://github.com/) and sign up for a free account. Pick your username tastefully &mdash; this will be public, and your website will be at `_username_.github.io` (note that if you do buy a domain name, you can still use github pages to host the site). If you sign up using your `@virginia.edu` account, you will be able to get an academic account that includes some additional free (for students) services, but it isn't necessary for this assignment. 

2. **Create a repository.** You should see a green "Create repository" button to click, or just visit [https://github.com/new](https://github.com/new). To create a website, you must use the name `_username_.github.io` for your repository. For now, we recommend selecting `Public` (instead of `Private`) for this. Be aware that this means that everything you put in the repository will now be visible to anyone on the internet, and once something is on the Internet it cannot ever really be deleted. It is good practice to check the box to `Add a README file` (you will edit this later). You can skip the `Add .gitignore` choice. If you don't selected a license, the default copyright laws apply to the content you create in the repository. If you want to allow others to benefit more from your content, you can select a more permissive license (which is not required for this).

3. **Visit your website!** Open a web browser to `https://_username_.github.io`. You should see your website like this:

<center><img src="/images/mywebsite.png" width=50%></center>

Congratulations! 

You now have a website &mdash; you can share anything you want (subject to github pages' [Terms of Service](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#limits-on-use-of-github-pages), so please no "get-rich-quick schemes, sexually obscene content, and violent or threatening content or activity", but totally fine to run a commercial or politically controversial site this way) with over 5 billion people on the Internet today (as well as billions of future people). 

## Editing your website

If you want people to visit your website, of course, you need some more interesting content than just "My super cool website!".

To get started editing the content, you will use the github web interface. Later, you'll see how to edit content more efficiently and powerfully by creating a clone of the repository to be able to edit on your own laptop instead.

Click "Add File" and select "+ Create new file" to create a new file. Enter `index.html` as the name of the file. By convention, this is the default file that will be displayed by a web browser visiting the webiste.

4. **Edit the `index.html` file to create a simple HTML webpage. 

HTML (HyperText Markup Language) is the core language of the World Wide Web. It provides a way to indicate the structure, style, and content of a webpage.

Here's an example

```html
<html>
<head>
  <title>My Favorite Web Page</title>
</head>
<body>
  <h1>Welcome to My Web Page</h1>

  This page is pretty boring now, but just you wait!
  
</body>  
</html>
```
(You can just cut-and-paste the text above into the github web editor, but feel free to be more creative.)

When you are done, click the `Commit Changes` button (at the top right). It will pop-up a dialog box where you can enter a description of the change, and then click the `Commit Changes` button.

Reload the `https://_username_.github.io` site to see that the content has changed. (Note that it can take several minutes for the changes you make in github to propogate to the website. So, if you still see the old welcome page, wait a few minutes and try reloading it again.)

5. **Make it fancy.** 

The example webpage above has structure tags (`<body>`, closed by `</body>` near the end, which surround the main body content of the page, and `<h1>` which indicates a first-level heading) that give suggestions to the client web browser how the page should appear. There are about 100 different tags in the [HTML Standard](https://html.spec.whatwg.org/multipage/#toc-semantics) that are supported by all major web browsers.







