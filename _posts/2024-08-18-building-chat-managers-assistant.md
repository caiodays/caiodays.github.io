---
title: Building a Chat-Based Manager's Assistant: The Journey Begins
description: Building a Chat-Based Manager's Assistant: The Journey Begins
author: Caio Dias
date: 2024-08-18 15:00:00 GMT-0200
categories: [ChiefChat]
tags: [ChiefChat, LLM, Vercel, Chatbot, AI, WhatsApp, Magie]
---

# Building a Chat-Based Manager's Assistant: The Journey Begins

Hey there! Have you heard about [Magie](https://magie.com.br/)? It’s a new app here in Brazil that lets you pay bills, transfer money, and more—all through WhatsApp messages. No flashy interfaces, no complex navigation—just a chat. And honestly, it’s brilliant. This is a shining example of how LLMs are changing the game for app development.

![Desktop View](https://framerusercontent.com/images/L5ftsFstggGR9H9WNQp3SCKbyis.png?scale-down-to=600){: width="277" height="600" }
_Magie on WhatsApp_

Why is this so cool? Well, it’s probably the most natural way to interact with an app. You just chat like you would with a friend, and the app does the rest. Plus, it takes a huge load off the development side—no need to worry about building a complex frontend. The interface is just a conversation, which, let’s face it, is way more intuitive.

But of course, there’s a catch. When your entire app is a chat, how do you keep track of what’s going on? How do you fully understand the state of your app? These are some of the challenges I’m excited to explore.

So, here’s the idea: I’m going to replicate this chat-based interaction style, but with a twist. Instead of managing your bills, this chat is going to be your right-hand assistant as a tech company manager. Want to know how your team allocation looks? Need to check on your 1:1s? Or maybe you need to compile all your 1:1s from the year into a performance appraisal? Or track the evolution of your team’s OKRs? This chat is going to do all that and more.

I’m breaking this down into two parts: (1) how I’m going to develop the app, and (2) how I’m going to generate the LLM responses.

For the development side, I’m diving into some of the coolest new tech out there. First off, I’m a big fan of the developer experience Vercel offers, so that’s where I’m starting. They’ve even got an open-source chat template ready to deploy, which saves me from reinventing the wheel. You can check it out here: [Vercel AI Chatbot](https://github.com/vercel/ai-chatbot).

![Desktop View](https://camo.githubusercontent.com/2885568d02297567020d63bbde49f54ee6f12c9909264f312b2834e702d5ff46/68747470733a2f2f636861742e76657263656c2e61692f6f70656e67726170682d696d6167652e706e67){: width="830" height="430" }
_An open-source AI chatbot app template built with Next.js, the Vercel AI SDK, OpenAI, and Vercel KV._

Now, let’s talk about the LLM. I want this chat to be smart, fast, and capable of calling functions efficiently. Enter [Groq](https://groq.com/)—a company I’ve been following closely. They’ve developed some dedicated hardware for speedy and cost-effective transformer model inference, and they’ve got a custom Llama 3 8B model for function-calling that’s topping the charts in the [Berkeley Function-Calling Leaderboard](https://gorilla.cs.berkeley.edu/leaderboard.html). You can find it here: [Groq Llama 3 Groq 8B Tool-Use](https://huggingface.co/Groq/Llama-3-Groq-8B-Tool-Use).

Using an open-source model like this gives me the flexibility to switch platforms or tweak the model as needed. And if I ever need more power, I can always scale up to a larger version of Llama. Plus, Vercel’s code is already set up to integrate with Groq’s inference, which is a big win.

I like to build things incrementally, delivering something useful in short bursts. So for my V1, I’m keeping it simple: a chat that integrates with Groq and can make an API call to list all the employees of an imaginary company and their teams when asked. I’m calling this app **ChiefChat**—a playful nod to the responsibilities of a Chief of Staff, who keeps everything running smoothly and efficiently behind the scenes. It’s not much, but it’s a start—and it will be open source! Next week, I will post here its code.

Stay tuned as I continue to build and refine ChiefChat. I’m excited to see where this journey takes me—and I hope you’ll join me for the ride!
