---
layout: post
title: National Lecture Series on AI
date: 2025-06-07 19:00:00 +0000
description: Nick Lambson delivers a national lecture on AI
img: national-lecture-series.jpg
fig-caption: 
tags: [education, AI, localization, langops]
categories: [blog]
author: Nick Lambson
---

On Saturday, June 7th, 2025, I was invited to speak at a national lecture series on AI. Speakers included
 - ZHONG Wenming（仲文明）Professor at the Central South University and Dean of the School of Foreign Languages
 - Nick Lambson（兰尼克）Senior Foreign Lecturer at Beijing Language and Culture University and Staff Engineer at MediaLocate
 - GE Zhongjun（葛仲君）Head of International Product Localization at ByteDance
 - GAO Yawei（郭亚文）Associate Professor at Northwest Normal University
 
I delivered a lecture called "Structured Prompt Engineering and Practical Applications in Professional Contexts." The below text is an English translation of a pre-lecture interview conducted by the organizer.

Reposted from WeChat: https://mp.weixin.qq.com/template/article/1749370234/index.html

> Hello, Professor Lambson. Thank you very much for taking the time to accept this interview amidst your busy schedule. The upcoming "Large Language Model Intelligent Post-Editing Practical Workshop" is about to begin, and everyone is eagerly looking forward to the module content that you will lead. You have extensive experience in the localization industry, having participated in language services for many international conferences and being active in the practice of AI and localization. Especially in areas such as leveraging large language models for translation, prompt engineering, and post-editing, your research and teaching have received high praise. We hope that through this interview, students will gain a deeper understanding of your work and better grasp industry trends in preparation for the upcoming course.

## Learn Python

> We understand that you have both studied or taught in the United States and China, and have long been involved in designing courses related to translation technology. With regard to modules on large language models and post-editing, what are the most significant differences in teaching philosophy and training methods between the two countries? Which practices or experiences do you believe would be most valuable for our students to learn from?

When I met Han Lintao at a TAUS conference in 2018, he said he was looking for a foreign teacher to teach localization and Python programming to BLCU students. It was a perfect fit. Teaching Python to translation students seemed normal to me: we were preparing them to become localization engineers, and many indeed have. But as I have gained exposure to other translation programs around the world, I have realized the uniqueness of this approach.
Virtually nowhere else in the world have I seen undergraduate or graduate translation students learn programming to the degree that BLCU’s localization students do. Many doubt the feasibility of this, saying that language students can’t learn computer science.

I disagree! Programming is just another language. And Python is remarkably similar to English itself. Learning programming sharpens your logic and trains you to think systematically. Programming has only become more valuable as AI has gone mainstream. For now, I have little concern that AI will make learning programming obsolete.

My advice: don’t hesitate to learn a bit of Python. Then, you’ll know how to ask AI for what you want. AI can turn your ideas into reality, as long as you know what to ask for.

## Try AI First

> Beyond your solid academic background, we also note your hands-on industry experience, particularly in automating localization workflows. In the era of large language models, how has the post-editing workflow changed compared to traditional service models? In light of these changes, what new skills should translators develop in order to remain competitive?

In 2017, TAUS published _Nunc Est Tempus_, an ebook signaling that _“now’s the time.”_ The industry was on the precipice of a major shift. In that ebook, TAUS mapped out the modern translation pipeline, which combines humans, data, and AI to optimally process each piece of content. 

In this pipeline, TAUS outlined four key roles, which largely hold true today: reviewers, transcreators, engineers, and data analysts.

They envisioned reviewers as not just post-editing machine translated content, but also fine-tuning the systems that produce the raw machine translation.

Transcreators are linguists who translate ideas and business outcomes, not necessarily words. A good example is a slogan or a marketing campaign, which require extra creative effort.

Both reviewers and transcreators got a huge power-up with the advent of LLMs. Tuning a machine translation engine is doable, but not easy. In contrast, prompting an LLM with specific instructions is more straightforward.

Andrej Karpathy, an engineer at Tesla and OpenAI, is credited with the phrase, “The hottest new programming language is English.” Although he said “English,” LLMs also work great with Chinese, especially DeepSeek! LLMs put customization of AI output within reach of anyone who can give instructions using natural language like English or Chinese.

Translators should sharpen their skills in explaining the nuances of a certain translation. Consider using the MQM error typology to specify what you mean. As you explain your rationale, AI systems can learn from your explanations and adopt your sense of judgment.

Transcreators should work with AI as a brainstorming tool. A perfect example is when I was asked to translate into English a slogan for an international conference center: 我们一直在用心！ Slogan translation requires creativity, so what use is AI? A lot, actually!

I engaged in a long, iterative brainstorming session with gpt-4o, trying to find the perfect words. “Give me some options that rhyme, that use the word heart, that have parallel structure, that convey warmth, professionalism, and leadership. And it has to have that special spark.”

After many rounds of revision, I finally landed on something I like: “Stand apart, lead with heart!” In other words, “Be exceptional. Be a leader. Be a warm and diligent person.” It’s not a word-for-word translation. But the English slogan sounds great and accomplishes the business purpose. That’s transcreation, and it was facilitated with AI.

## Structured Prompts

> In the upcoming “LLM + Smart Post-Editing Workshop,” you will focus on structured prompt engineering and AI-assisted post-editing. For many students, these concepts are entirely new. Could you briefly explain your understanding of “structured prompts”? What key role do they play in today’s translation and localization practices?

There are at least five parts to a prompt: instruction, input data, context, output requirements, and constraints. A structured prompt explicitly states each of these parts to the LLM. This clarity enables the LLM to carry out your request with greater fidelity.

However, typing all of those parts for every prompt is time-consuming and laborious. Typically, an AI-powered translation management system will automatically collect the relevant context and output requirements for you, and insert it into your prompt programmatically. In other words, the prompt is simply a template, with placeholders like {terminology} and {translation_memory_matches}, where these placeholders are replaced with actual data that’s relevant to the request.

When having a conversation with an LLM, there are three roles: system, user, and assistant. In production systems, the system prompt contains detailed instructions. The user prompt contains input data. And the assistant role is for the LLM’s response to the user. Both the system prompt and the user prompt start as prompt templates, where placeholders are replaced with relevant data before sending the request to the LLM.

## LangOps

> From an industry perspective, what fundamental changes do you foresee as large language models and smart post-editing continue to evolve? As students, how should we position ourselves, and what new competencies must we cultivate to ensure we are not replaced by AI, but rather can leverage it to advance our careers?

In the 1990s, the translation function was assumed into localization, which, together, with internationalization, constituted a major part of a company’s globalization efforts. Here, we refer to globalization not as the increasing global exchange of goods, people, and ideas, but as the transformation of a domestic company into a global company. The phrase “go global” embodies this idea well.

Just as translation was operationalized as localization in the 1990s, we are now seeing a shift of equal, if not greater proportions. CSA Research, the language industry’s leading independent research firm, declared that in 2023, we entered the “Post-Localization Era.” Now, the emphasis is not so much on delivering a localized product, but on building language systems to support the international experience.

Some have proposed a new term to define the principles and aims of localization in the AI era: LangOps, or Language Operations. This term takes inspiration from similar transformations in IT like DevOps or CloudOps. LangOps has gained a lot of traction since its inception in 2021. Global enterprises are no longer thinking about linear workflows that deliver a localized product. They are now blueprinting and constructing systems that provide a seamless user experience in any language in real-time. This is LangOps. What about language service providers? They are rebranding now as global content service providers. AI and data services make up a growing part of their service offerings.

The word translator does not convey the value that you provide to a business. When you describe yourself as a translator, you put yourself into competition with AI. Recent developments at Duolingo suggest that competing with AI is not a winning strategy.

Instead, I suggest conceptualizing yourself this way:
 - “The brand voice of \[company\] in \[country\]”
 - “User experience advocate for users of \[product\] in \[country\]”
 - “Data-driven language quality analyst for \[language\]”
 - “GenAI implementation strategist for international businesses operating in \[country\]”

The activity of pure human translation is losing value. But translation studies can equip you to become the voice for users of a product in your country. I suggest pairing translation studies with programming and another field like marketing to become a valuable asset to a global business.

## Highlights of the Workshop

> Finally, could you share with the students a few words about the highlights of your module, “Structured Prompt Engineering and Practical Applications,” in the “LLM + Smart Post-Editing Workshop”? What concrete, hands-on breakthroughs can participants expect to gain?

Participants can expect to learn the following skills:
 - How to construct a prompt to optimize results
 - How to implement structured prompts in a production system using Python
 - How to re-use and test your prompts using a prompt registry
 - How to perform translation quality estimation using AI
 - A case study of implementing AI to evaluate quality of English writing

The main emphasis of my course is to show you how AI is implemented in production environments where the following considerations are most important: execution speed, structured output, reusability of prompts, prompt version history, insertion of context into prompt templates, and combination of AI and human work. 

> Once again, thank you to Professor Lambson for taking the time to accept this interview and share insights on the cutting-edge field of "Large Language Models + Intelligent Post-Editing." We hope students can gain a deeper understanding of the course content and industry trends through this dialogue. We also look forward to everyone actively participating in the "Large Language Model + Intelligent Post-Editing Practical Workshop" this Friday, effectively enhancing their skills in Prompt Engineering and AI-assisted post-editing, and witnessing the innovation and transformation in the language service industry together.