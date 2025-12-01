---
layout: post
title: Exploring the LangOps Tech Stack at Chongqing Jiaotong University
date: 2025-11-22 09:00:00 +0800
description: Talking about the technologies that power "Language as a Feature" in the Post-Localization Era.
img: chongqing_1.jpg
fig-caption: 
tags: [langops, localization, ai, automation]
categories: [blog]
author: Nick Lambson
---

On November 22, 2025, I joined the Forum on Building a New Ecosystem for Intelligent Language Service Talent Development through Industry-Academia-Research Integration at Chongqing Jiaotong University to explore the key technology components of systems that power **Language as a Feature**. The topic is closely related with [LangOps](https://langops.org/), Global Content Solutions Providers, and the Post-Localization Era. Below is a summary of my presentation.

## From Language as a Service to Language as a Feature

The language industry is undergoing a fundamental shift. Traditionally, language has been offered as a service through Language Service Providers (LSPs). This model is project-based: organizations contract with LSPs or translators to translate specific documents or assets. Each translation request becomes a project, involving handoffs between clients, project managers, and linguists, all with set deadlines. Delivery times, pricing (usually calculated per word or per page), and quality checks are negotiated for each project. Translation is typically seen as a cost center—something to be managed, scheduled, and budgeted for.

In the AI era, language is increasingly embedded as an always-on feature within digital products and platforms. There are no "projects"—translation and localization happen automatically, in real time, and in any language the user requires. There are no handoffs or deadlines, and translation is not priced per word but included as part of the overall system or subscription. Language capabilities become embedded features that enable customers to interact and transact globally, without additional operational friction. This approach transforms language from a labor-dependent service to an integrated feature that enhances the international user experience.

[CSA Research](https://csa-research.com/) calls companies who enable the "Language as a Feature" approach Global Content Solutions Providers or GCSPs.

## Real-World Examples of Language as a Feature

During the Myanmar earthquake response, language was a crucial feature that enabled effective rescue operations. Using an AI-powered Emergency Language Service Platform built on [Deepseek](https://www.deepseek.com/)'s large language model by BLCU's Han Lintao, China Search and Rescue used real-time translation, speech recognition, place name mapping, and image analysis, all tailored for disaster scenarios. This system broke down language barriers between Chinese, Burmese, and English speakers—even working well offline and in noisy environments. This example goes beyond language as a service to language as a feature of a system, designed to accomplish a specific outcome. [LangOps Myanmar case study](https://langops.org/case-studies/)

Another example of language as a feature is augmented reality glasses which listen to dialogue, translate it in real-time, and display it on the lenses in front of your eyes. Users don't pay per word for this translation service. They just pay a substantial price for the initial product, and that initial revenue covers the user's lifetime costs for translation.

## Twelve Transitions from Language as a Service to Language as a Feature

The transition from language as a service to language as a feature is marked in many ways. By understanding these twelve transitions, students and educators will be better prepared to support the needs of companies who require the "Language as a Feature" approach in the AI era.

1. **Statistical and Neural MT → LLM translation**
2. **Quality assurance tools → Quality estimation scores and reports**
3. **Post-editing of MT → Automatic post-editing (APE)**
4. **CAT tools and TMS → Under-the-hood TMS**
5. **Segment-based translation memory → Full-text semantic lookup via embeddings**
6. **Terminology database → Knowledge graphs**
7. **Per-word pricing model → Subscription model**
8. **Publish in traditional methods → Deliver content via multilingual chatbot**
9. **Assume source to target → Generate multilingual content from scratch**
10. **Traditional file formats → The rise of Markdown**
11. **Publish content for humans → Publish content for AI agents**
12. **Text, audio, and video are isolated → Multimodal convergence**

Let me explore some of these transitions in detail.

## LLM Translation: MT Aggregators, Prompt Registries, and Metaprompting

### MT Aggregators

An MT aggregator is a tool that unifies different LLMs like GPT 5.1 and Claude Sonnet 4 and MT engines like DeepL and Google into a single interface for streamlined communication with the translation management system. This makes it easy to customize what models, engines, and prompts are used for each client and each language pair. The French may prefer DeepL. The Americans may prefer GPT 5.1. The Japanese may prefer Claude. An MT aggregator gives the options and simplifies the complexity.

### Prompt Registries

A prompt registry is a database of the history of a prompt, and also a dashboard for comparing the output between versions. For example, take the source text "China is developing its space technology at a steady pace." Version 1 of the prompt might ask for a formal and bureaucratic tone. It's too formal, so in version 2, you ask AI to give you a translation in a warm and friendly tone. And finally, in version 3, you decide that the prompt should have a standard and professional tone. You can compare the output of the prompts in a prompt registry.

### Metaprompting

Metaprompting is asking AI to revise your prompt based on annotations of previous output.

Let's say I ask AI to translate from Chinese into English, preserving unique cultural aspects. The translation comes out, and it has a sense of foreignization: Sun Wukong, Jingu Bang, qi, and Bingtang Hulu.

I wish to modify the translation to: The Monkey King, Golden Staff, energy, and candied hawthorn skewers. I then provide the Chinese source, the original English translation, and the revised English translation to the AI and ask it to revise my original prompt, taking into account the revisions to the translations.

It then generates a new prompt for me: "Translate from Chinese into English using a domestication strategy to maximize comprehension."

## Quality Estimation: Scores and Reports

Quality estimation is AI prediction of translation quality, usually with no reference translation. The first form of quality estimation called direct assessment generates a score from 0-100. It's not 100% reliable, but it's consistent enough to serve as a useful heuristic for finding problematic translations.

Another use of quality estimation is to annotate errors based on the [MQM](https://themqm.org/) error typology. A result might show error categories like Style - Word choice, Terminology/Locale, Accuracy - Mistranslation, and Fluency - Grammar, each with severity levels and suggested translations.

## Automatic Post-Editing

Automatic post-editing is the automatic revision of machine translation by AI. It works best when the MT has been generated by a different engine than the automatic post-editing model. For example, if a translation was generated by Google, it may have an error. That error is reflected in the translation's low QE score and presence of an error in the quality report.

The translation, its score, and its quality errors are sent to a different AI model, which will implement any changes to produce a higher quality translation. Automatic post-editing isn't a perfect process, but it can consistently improve translation quality a little bit.

On the scale of a whole project, automatic post-editing can help improve low-scoring translations. High scoring translations from MT can be automatically approved, whereas low-scoring translations from MT can go to automatic post-editing, or to a human post-editor. The final goal is to bring the translation quality up to the required level.

## Under-the-Hood Translation Management Systems

Traditional computer-assisted translation (CAT) tools and translation management systems (TMS) are becoming outdated. Instead, we see the emergence of what I call "under-the-hood" translation management systems.

When you drive a car, you see a simplified interface. But when the mechanic opens the hood, the many parts of the car become visible. Most of a car's function is handled "under-the-hood," out of sight of the user.

Translation Management Systems are taking on similar characteristics to cars: a simplified interface behind the wheel, and a collection of automated features under-the-hood.

I call them under-the-hood TMSs, but sometimes they are called "language factories" or "headless TMSs." These systems operate behind the scenes using APIs, sending content seamlessly between content management systems, translation management systems, and AI systems. Only when human input is needed does the system present a task for a human. [Blackbird.io](https://blackbird.io/) is a company that builds the kind of technology that makes this possible.

## Semantic Search with Embeddings

Traditional translation memories store segments of source text and their translations. They're useful but limited. They are segmented, and they are limited to textual matching. Translation memories fail when looking up text with similar meaning, simply because the text doesn't match.

But with embeddings and semantic search, it's now possible to move beyond translation memory. Let me show you an example. Let's take the source text: "China is steadily developing space technology." This text can be stored as a document, then converted into an embedding, which is a sequence of numbers. Then, when you have a query, like "Chinese tech for exploring the stars gets better every day," you can also convert the query to an embedding, and find other embeddings that are mathematically close. Because the distance between the embeddings is low, the database would return the original text as a result.

Embeddings enable AI models to locate and use semantically similar content, not just literal matches. This is a big shift beyond segment-level translation memory and it's an important part of "Language as a Feature."

## Knowledge Graphs

Have you ever searched for something and seen a sidebar with information? I searched for info about the Great Wall, and Google showed me some data. This data is not someone's opinion, this is verified data from a knowledge graph.

A knowledge graph is a database. Except it doesn't store information in tables, rows and columns, but instead, in nodes and relationships. Knowledge graphs solve one major weakness of LLMs: hallucination. LLMs make up things that aren't true. Knowledge graphs solve that problem. They ground the AI response in real, verified facts.

What's more, knowledge graphs can contain multilingual labels. That means they can be used in place of terminology databases. The advantage of using a knowledge graph instead of a term base is that knowledge graphs connect multilingual terms with wider knowledge throughout the company, making it much more valuable to humans and AI. At least one company has been actively involved in building multilingual knowledge graph systems, and that's [Coreon](https://www.coreon.com/).

I build my knowledge graphs using [Neo4j](https://neo4j.com/) and [Arrows.app](https://arrows.app/).

![Chongqing Forum](/assets/img/chongqing_2.jpg)

## New Delivery Models

### Subscription Model

The pricing model of Language as a Service usually involves per-word pricing, pay-as-you-go, and unpredictable budgeting. Creating quotes, invoices, and purchase orders for every project creates a lot of administrative overhead.

In contrast, supporting Language as a Feature can be billed as a subscription. It would include translation of a couple million words per year, and it would simplify budgeting and processing. For example, an annual subscription of $120,000 might include 2 million "word" credits per year, where AI translation consumes 0.5 "word" credit and human translation consumes 1 "word" credit.

### Multilingual Chatbots

When I attended [tcworld China](https://www.tcworld.info/) in Shanghai in 2023, I saw a presentation from Huawei where they showed the evolution of technical manuals from paper manuals to online knowledge bases, to in-vehicle AI-driven voice assistants.

This is remarkable because it shows that the way that companies communicate to their customers is changing. Now, instead of browsing through knowledge bases or websites, customers can chat with a multilingual AI voice assistant. What's more, the voice assistant is equipped to actually take action: to turn on the air conditioning, to lock the vehicle, or to defrost the windows.

### Multilingual Content Generation

Now, some companies are even questioning the assumption that the best way to talk to international customers is translation. The preference for translating from a source text is just an assumption, one that's no longer necessary if AI can generate content simultaneously in multiple languages. Multilingual content generation bypasses translation entirely. That being said, it's still necessary to have a native speaker expert take responsibility for the multilingual content.

## New Formats: Markdown and Publishing for AI

### The Rise of Markdown

A large amount of translation volume comes from technical documentation. And a new philosophy for publishing technical documentation has emerged within the past years, called [docs as code](https://www.writethedocs.org/guide/docs-as-code/). Essentially, writers publish documentation in the same way they publish code. They use a format called [Markdown](https://markdown.cn/docs/intro) and a version control system called Git.

Markdown looks like a text file when you're writing it, but it looks like a web page when you're viewing it. It's a very popular, universal file format. Headings are preceded by hash signs. Bold text is surrounded by two asterisks.

What's remarkable about Markdown is that it's the native language of LLMs. Prompts written in Markdown are more effective than other prompts. LLMs natively respond in Markdown format. When you chat with [ChatGPT](https://chat.openai.com/) or [DeepSeek](https://www.deepseek.com/) and you see headings, lines, lists, and bold text, you're seeing Markdown.

Markdown is both human readable and structured, which makes it perfectly optimized for Large Language Models.

### Publishing for AI Agents

You know the word "netizens," as people who use the internet right? Well now, netizens are not just humans, but also AI agents. AI agents are browsing the internet, reading web pages, and taking action based on what they see.

With this in mind, we need to understand that we are no longer publishing content or translations for just humans, but for AI agents too.

Agents need content that is modular, hierarchical, precise, literal, consistent, unambiguous, explicit, concise, and tagged with metadata.

One form of publishing content for AI agents is called an [llms.txt](https://llmstxt.site/) file. It's essentially a summary of your site in Markdown format. When an AI agent visits your website, they first read the llms.txt file to understand what to do with it. This makes it much easier for an LLM to work with your content, find what they need, and help customers.

### Multimodal Convergence

In the past, text, image, audio, and video content has been translated entirely separately. Multimodal AI breaks that assumption. A single AI model can now read and create text, image, audio, and video in a single step. That means we need to re-consider how we translate and localize images and audio-visual content.

![Chongqing Forum](/assets/img/chongqing_3.jpg)

## Takeaways: Recommendations for Students and Educators

By focusing on the twelve areas that I've outlined, we'll be able to support language as a feature, where multilingual support is an always-on embedded feature, available in real time. Providers will grow from language service providers to global content solutions providers.

My recommendations are not authoritative or comprehensive, they are just friendly suggestions.

### Reframe Your Value (Language Focus)

If you aim for a career as a translator with a primary focus on language instead of technology, I invite you to reframe your value.

In my view, the core value of the human contribution is not language production, but trust.

Human oversight is indispensable in industries that run on human trust: law, medicine, government, business.

Focus on skills that have trust at the core: subject matter review and interpreting. Also consider multimedia skills, which are increasingly in-demand.

Acquire core knowledge in your domain. Then, study the fundamentals of trust: culture, style, negotiation, ethics, and policy.

### Become the Voice and Skill Up (Language + Technical Focus)

If you aim for a career equally focused on language and technology, become the voice in your locale for your market.

Let's take an example: you work for Chinese electric vehicle manufacturer [Zeekr](https://zeekrlife.com/), and your job is to publish multilingual content for European customers. Understand European car buyers. Understand what they want to see and hear. And become the voice of Zeekr in Europe.

Next, understand how AI works with linguistic data. To do this, you need to practice prompt engineering. Try Metaprompting: ask AI to revise your prompt based on pairs of original and revised text.

To make AI responses more factual, connect with knowledge graphs.

To work more smoothly with AI, use Markdown.

### Take a Systems Approach (Technical Focus)

If you have a strong technical focus, my advice to apply Markdown and knowledge graphs still applies.

But in addition to prompt engineering, you should practice context engineering, which shapes the information an LLM considers when generating a response. Figure out how to inject relevant terminology, style guidelines, and translation memory matches into the LLM translation prompt.

You'll quickly realize that context engineering requires some programming, and there's no better language than Python.

Don't be afraid of learning programming. In fact, it's never been easier, with AI Coding. Popular tools include [Cursor](https://cursor.sh/) and [TRAE](https://trae.ai/).

Take your language skill, then operationalize it in a technical context by learning NLP: natural language processing. Consider taking courses in computational linguistics, corpus linguistics, and corpus translation studies.

## Conclusion

The language industry is transitioning from language as a service to language as a feature. This shift is marked by twelve key transitions, from statistical MT to LLM translation, from per-word pricing to subscription models, from traditional file formats to Markdown, and from publishing for humans to publishing for AI agents.

By understanding these transitions and developing the appropriate skills—whether focusing on trust and human oversight, becoming the voice for your market, or taking a systems approach with programming and NLP—students and educators can prepare themselves for the future of language services in the AI era.