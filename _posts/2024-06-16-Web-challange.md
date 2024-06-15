---
layout: post
title:  "RenderQuest"
---

## Hello Everyone
Today we will be doing RenderQuest.

RenderQuest is a HackTheBox challenge categorized under web tasks. It's considered moderately straightforward in difficulty, making great opportunty to learn about Template Injections

![image](https://github.com/Unc3nny02/unc3nny02.github.io/assets/127601349/97596be8-b015-4717-9747-df09c86531ee)

##CHALLENGE DESCRIPTION

You’ve found a website that lets you input remote templates for rendering. Our task is to exploit this system’s vulnerabilities to access and retrieve a hidden flag. 

![image](https://github.com/Unc3nny02/unc3nny02.github.io/assets/127601349/5eb9cc00-1389-4eb3-9c3e-3d73abf96369)


In the requirements file, there's a main.go file. This file contains all the request parameters for when you visit the given IP and port. When you access it, you'll see a webpage with a parameter input field.

We can use a webhook here because it allows us to enter an external link. This way, we can build queries externally, and the program will execute them.

Why?

Let's check the source code to understand how the program runs everything after clicking the "Render Now" button.

![image](https://github.com/Unc3nny02/unc3nny02.github.io/assets/127601349/feee76cb-2c4c-450f-bf8f-737bd3ada18f)

we will build the request accordingly using

https://webhook.site/

Let's try the FetchServerInfo first and test if it works or not

So first we need to create file called index.tpl and inside of the file

![image](https://github.com/Unc3nny02/unc3nny02.github.io/assets/127601349/8ad2b9b1-c947-4a2e-8e8c-a2c07b373fee)

and we need to transfer this file using python server 

Next we need to set up ngrok

![image](https://github.com/Unc3nny02/unc3nny02.github.io/assets/127601349/2b68339f-3fcf-4b8b-9a17-f7969b152079)

and we have to naviage using our ngrok link:

![image](https://github.com/Unc3nny02/unc3nny02.github.io/assets/127601349/5776585f-b9f8-4aa2-b7b2-0e7a2f9a0a5f)

and we can see we successfull to view the file, additionally we see flaga5b739980b.txt which is our flag.

Although this challange was quite straightforward but it was deffintely interesting. Hopelly You learned something new

Happy Hacking :)


