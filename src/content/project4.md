+++
author="David Evans"
date= "2024-04-17"
linktitle="project4"
title="Project 4: Generative AI"
+++

The main goals of this project are for you to:

1. Gain some experience using generative AI tools and learn about their capabilities and limitations.
2. Develop an augmented chat bot to save the world (or at least produce something fun).

<div class="yellowbox">

**Collaboration and Resources.** For this assignment, you may work on your own or in a team of up to three people. If you work with others, your team should turn in one assignment with all team members names on it and every team member should be fully involved and completely understand everything you submit.

Feel free to search the web for helpful resources and use generative AI tools in any way you wish (but to document any uses outside the ones requires for this assignment). If you use other resources to help answer any of the problems, you should document the resources you used and explain how you used them.
</div>

<div class="gap"></div>

## Getting Started

For this project, you will need an account on [poe.com](https://poe.com). (Recall that this project is the _default_ &mdash; if you have an idea for something different you would like to do instead, talk to me and it may be an option.)


Poe provides an interface to many generative AI tools, including most state-of-the-art large language models (e.g., Claude-3 Opus, GPT-4, Mistral Large), lower quality but cheaper to use models (e.g., GPT-3.5 ("ChatGPT"), Gemini, Llama, etc.), as well as image generation models (e.g., Dall-E-3, StableDiffusionXL), and the ability to create your own augmented chat bots (which you will explore in this project).

Although we encourage everyone to create their own poe accounts, if you are doing the project together with a team you can use one shared account for this. Creating a poe.com account (which is free, but requires providing an email and phone number). To use the better language models (which is required for this assignment), though, you will also need to pay for a subscription (you may be able to get a free one-week trial) which is $19.99/month. If this is a hardship for you, please reach out to me (I can provide a limited number of free accounts for anyone who asks, or an alternative if necessary).

With the Poe interface, you can select the model to use by selecting the "More" button at the right (about the chat box entry window). 

<div class="problem">

**Problem 1.** Think of a query (prompt) to use to try out the language models. Try your prompt using Poe's interface on at least these language models: GPT 3.5-Turbo ("ChatGPT"), GPT 4, Claude-3 Opus, and Llama-2-7b. These interfaces are _conversational_, so after the initial response you should follow-up. If the model's initial responses were bad, use follow-up prompts to try and lead it to a good answer. If the model's initial response is good, try to use follow-up prompts to get it to a bad answer.

For your response, you don't need to include transcripts of all your chats, but explain the prompt you used, and your observations about the different chat bots.
</div>

## Hallucinations

It is popular these days to say chat bots "hallucinate", when they generate plausible responses to questions that are not based on any actual facts, and seem to demonstrate creative imagination at fabrication. (Of course, this is just an outcome of the way the chat bots are trained, which you should understand from Classes 25 and 26.)

It is easy to get ChatGPT and similar chat bots to "hallucinate", but requires more creativity to make the best recent chat bots (Claude-3 Opus and GPT-4) "hallucinate".

<div class="problem">

**Problem 2.** For warm up, generate an example where GPT-3.5 Turbo ("ChatGPT") hallucinates. Then, try to generate an example where GPT-4 or Claude-3 Opus hallucinates.
</div>

## Image Generation

For these problems you can use any AI image generation tool you want, but we recommend trying Dall-E-3 (OpenAI's model) and StableDiffusionXL in Poe.

<div class="problem">

**Problem 3.** Generate an image you like using an AI image generation tool. You will find that adding a lot of text to the prompt often improves the image, and that you can steer the image generation with requests about the style of image you want. Optionally, add the image to your website.
</div>

Image generation can produce artistic (at least to my eyes!) and sometimes useful images, but it very difficult to get them to produce something specific.

<div class="problem">

**Problem 4.** (Challenging!) Use an AI image generation tool to produce an image that contains exactly eight people. They can be doing anything you want and in any setting, but there has to be exactly eight people in the image.
</div>

(If you don't succeed at this, its okay to give up once you've made enough attempts to be convinced this is really difficulty. I've tried quite a bit but have not succeeded at getting an image with exactly 8 people in it. If you do find it too easy to satisfy this challenge, try to generate an image showing [a soccer player taking a penalty kick](https://poe.com/s/xkPCoUAREHqawHGhiUNx), [a correct chess board](https://poe.com/s/LWs0L1vWeQl3hfHPGy63), [a correct image of the Rotunda](https://dailyprogress.com/news/local/education/uva-shares-error-riddled-ai-generated-art-of-its-own-campus-to-promote-eclipse-watch/article_5ffb9838-f5f2-11ee-b15d-b77259468870.html), or any other specific thing you would like.)

<center><img src="/images/airotundaimage.webp" width="60%"><br>

Image from [invitation to President Ryan's eclipse watch party](https://twitter.com/presjimryan/status/1777066473355182116?ref_src=twsrc%5Etfw)
</center>

## Making an Augmented Chat Bot

For the last part of this project, your goal is to make an interesting (or maybe even useful!) augmented chat bot.

You can do this in Poe by clicking the "Create bot" button at the top left of the interface.

Then, to create your bot you will need to provide an instruction Prompt and Knowledge Base. The knowledge base can be any documents that you want the bot to use in generating its responses. You can also select the base model (e.g., Claude-3 Opus, GPT-4, but feel free to try any you want, including image generation models) for your bot. (If you select one of the subscriber access models like GPT-4 for your bot, only people with Poe subscriptions will be able to use it, but otherwise you can make your bot public and visible to any Poe user.)
  
<div class="problem">

**Problem 5.** Create an interesting augmented chat bot. Your bot should be able to do something that cannot be done as well with a good unaugmented model. 
</div>

To submit this problem, you can either *demo* your bot in class on May 2 and, or you can provide a written dscription of your bot and how you built it. 

In addition, you should make your bot public and submit a link to your bot (in the Canvas discussion for this project), unless you have a reason to want to keep your bot private in which case you should explain why you want to keep your bot private and provide a few transcripts showing its behavior.





