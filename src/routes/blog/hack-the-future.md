---
title: Hack the Future 2022
author: Thibaut Wittevrongel
date: 2022-11-15
cover: https://res.cloudinary.com/tesell/image/upload/c_scale,q_56,w_1279/v1672451642/blog/htf2022_byiyvr.webp
coverDescription: Hack the Future 2022
description: My first hackathon experience at Hack the Future 2022, a hackathon organized by the Cronos Group.
tags: hackathon
---

<script>
    import Image from '$lib/components/Image.svelte';
</script>

<Image imgUrl="https://res.cloudinary.com/tesell/image/upload/c_scale,q_56,w_1279/v1672451642/blog/htf2022_byiyvr.webp" altText="Hack the Future 2022" size="large" />

# My first hackathon experience at Hack the Future 2022

In this blog post, I will go over my first hackathon experience at Hack the Future 2022, a hackathon organized by the Cronos Group. I will go over the challenge, the team I was in and the project we made.

<hr />

## 🚂 The way to Hack the Future

Together with a group of students from Howest we gathered at the train station in Bruges to take the train to Antwerp-Central in the early morning. We were all excited to participate in this hackathon and to see how it would go.

When we arrived at Antwerp-Central, we walked to the venue, Handelsbeurs Antwerpen. We were welcomed by the organizers and received a very nice breakfast.

<Image imgUrl="/images/HackTheFutureEntrance.jpeg" altText="Hack the Future Entrance" size="small" />

## 📝 The Concept

In this hackathon, everyone was split up in groups of 2 people. The group that I was part of consisted out of Djelal Fida and myself (Thibaut Wittevrongel).
Each group had to come up with an original name for their team. We came up with the name "204NoContent".

Next up, every group received their challenge and were assigned a room to work in. In total, you had 5 hours to complete your challenge.

## 📝 The Challenge

Our challenge was called 'Connect Wizards and Muggles'.

The description of this challenge goes as follows:

*"The world is about to perish. We need help, but no human help is sufficient, so magicians had to step in. Using their magic they can save our world (hopefully), but they need to use Earthly spells otherwise it will have no effect in our world! We have already acquired the Earthly spells for you, but the magicians need them in an Ancient language called Pig-Latin. It is your job to translate them and make sure they arrive at the correct destination before it is too late..."*

In this challenge, we had to translate the spells from English to Pig-Latin and send them to the correct destination. If the spell was sent in another language than English, it had to be translated to English first and then into Pig-Latin.

## 📈 The Architecture

<Image imgUrl="/images/HTF-2022.drawio.png" altText="the infrastructure of our challenge."/>

In the image above, you can see the architecture of our challenge. The goal of this challenge was to create the services that were marked in orange and connect them to the services that were connected with the green lines.

## Solving the challenge

The start was a bit slow since we had to figure out how AWS worked, as we had never used it before.

But after a while we got the hang of it and started to work on the challenge. First, we had to figure out how we could send messages from our AWS Lambda function to Teams or SendGrid.

After that we successfully sent messages to the respective destination, we had to figure out how we would translate the messages from English to Pig-Latin. To complete this, we wrote a function that would translate the messages from English to Pig-Latin.

The third step was to check if the message was in English or not. If it was not in English, we had to translate it to English first. To figure out if the message was in English or not, we used the AWS Comprehend service. This would return the dominant language of the message. If the dominant language was not English, we would translate it to English using the AWS Translate Service.

The fourth step was to be able to send our message on a message queue. To do this, we used the AWS SQS service.

The last step was to be able to translate entire sentences, keeping in mind capitalization and punctuation. To do this, we created our own functions to translate the sentences.

To complete the challenge, we used the following technologies:

- AWS Lambda
- AWS SQS
- AWS Comprehend
- AWS Translate
- SendGrid
- Teams
- NodeJS

## 🏆 The Results - 204NoContent - The Winning Team

<Image imgUrl="/images/htf2022_win.jpg" altText="Won the public and jury prize at Hack the Future 2022"/>

We could complete the challenge within time and to our surprise we were the fastest team to complete the challenge. Because of this, we won the challenge! We also won the public prize and received some very nice prizes!

## 📝 Conclusion

This was my first hackathon experience and I really enjoyed it. I learned a lot about AWS and how to use it. I also met a lot of new people and had a lot of fun. I would definitely recommend this hackathon to anyone who is interested in participating in a hackathon.


