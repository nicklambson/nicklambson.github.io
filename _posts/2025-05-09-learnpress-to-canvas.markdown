---
layout: post
title: From LearnPress to Canvas: My Journey to a Better LMS
date: 2025-05-10 12:41:00 +0000
description: Canvas offers excellent features, and it's free for teachers.
img: canvas.jpg
fig-caption: 
tags: [education, ai]
categories: [blog]
author: Nick Lambson
---
Canvas is a learning management system (LMS) based in Salt Lake City, Utah. Although that's where I grew up, my road to Canvas has a roundabout one.

## Cyber Attack

Initially, when I started teaching at BLCU in 2018, I was asked to use a proprietary learning management system (LMS) offered by the university. I designed curricula for seven courses of 16+ weeks each and uploaded them to the university's LMS. It worked fine for a year, until one summer, the LMS server began to receive thousands of spam user account registrations. The server was the target of a cyber attack. As a result, the university took the server down. I was lucky in that I was still able to export my data from the server.

## LearnPress

In the fall of 2019, I launched nicklambson.com and installed LearnPress, a free LMS. I uploaded all my course content to LearnPress and began using it with my students. I enjoyed having total control over my data. However, things didn't work out perfectly.

One downside is all the time required to set it up and learn how to use it. To be honest, it's a little clunky. The development team has not put in all the work required to make it function smoothly. The support team also does not reply to questions and requests on the forums. Not communicative.

Another downside is that certain basic features of an LMS are not available by default, like a gradebook. Without an extra plugin, you can't see the grades of all the students in your class. You can't split your students into sections. That means year after year, new students get tossed into the mix, making course management more complicated. I went as far as developing an app that exports WordPress's database in the form of JSON files, then parses all the JSON files to re-create all the student-course-assignment relationships and build a scorecard for each class. It involved extensive tooling using Python and the data analysis library `pandas`.

I experienced bandwidth issues with Bluehost, my hosting provider. One reason is that I had hundreds of students logged in concurrently. Another reason is that Bluehost hosted my website on a server in the United States that perhaps wasn't friendly to Chinese ISPs. For that reason, traffic to my website would be throttled to certain devices. As a result, my students had trouble accessing pages quickly and couldn't download files in a prompt manner. This was especially troublesome when I asked my students to take an exam online. Connection errors and timeouts caused a lot of frustration for both my students and me.

To solve the bandwidth issues, I paid an extra sum of money to upgrade my hosting plan to professional plus. This improved the performance considerably. There were no longer any challenges with hundreds of users being logged in concurrently. This worked well for about three years.

## Crossroads

I was justifying the expense by making available two online courses: Python for Localization (Foundation) and (Professional). Sales of the courses were good. It was a profitable venture. But interest tapered off after about two years. Most everyone who was interested in the course had already purchased it. Cash flow dried up.

The three-year introductory pricing on professional plus web hosting eventually expired, and reality set in. I would have to pay a thousand dollars if I wanted to keep my hosting plan after the fourth year. Thank goodness Canvas came to the rescue. I had heard good reviews of Canvas, and its free-for-teacher program seemed too good to be true.

In the summer of 2024, I ported all my content from LearnPress to Canvas. This process was made easier by downloading my entire LearnPress website contents to my local machine over FTP. Any page HTML content could be copy-pasted seamlessly. Hyperlinks, images, and documents had to be manually added to Canvas and re-linked. Quizzes, exams, and assignments had to be re-created manually. It was a menial task, but it was well worth it.

As for my other web content, I re-created nicklambson.com using GitHub pages and Jekyll. It's now primarily the lightweight blog site that you are browsing now. I was also hosting music on nicklambson.com, which I now do on SoundCloud instead.

## Canvas in China

My students in China can easily and reliably access Canvas in China because Canvas is hosted on stable and robust AWS servers. Performance is fast. The user interface has even been localized into Chinese. The Chinese UX is good.

However, Canvas does not accept @qq.com email addresses for user registration. QQ is very popular among Chinese, so this can be a cumbersome hurdle. I asked a Canvas customer success manager about this restriction and he clarified that it's because users were creating spam Canvas accounts using @qq.com email addresses, then creating courses, uploading illegal or illicit content, and distributing it. Apparently, this wave of spam accounts caused Canvas engineers to simply blanket ban all @qq.com email addresses.

This @qq.com restriction posed a real challenge for me and other teachers from the BYU China Teachers Program who are teaching in China. Between all of us, we have several thousand students. The customer success manager arranged a solution for us where we would just email lists of students and emails to a Canvas representative, who would create accounts for those users manually. However, this was clumsy, manual work, and we had thousands of students that needed to get onboarded fast. Education in China moves at light speed. This workaround was not feasible for us.

Although many teachers were enthusiastic about using Canvas to manage their courses, they were dissuaded by the technical difficulties that got in their way because of the @qq.com blanket ban. They eventually threw in the towel. Now, they keep their distance from Canvas, retaining a vivid recollection of the source of their headaches.

## How I use Canvas

As for myself, I was able to get around the @qq.com blanket ban by asking my students to sign up with a non-qq email address. I did something unique in the early days of student registration on Canvas. I did not allow my students to sign up for Canvas themselves. Instead, I asked them to complete a form and submit their English name, Chinese name, email address, and other information. From the form results, I concatenated their English name, Chinese name, and class. I then signed up for them with the concatenated name that I had created. This way, there is no confusion about who is who. If I allowed them to sign up on their own, they would name themselves random monikers like CloudPrincess88 or VorpalBlade666. Ok, VorpalBlade666 is pretty cool actually.

### Overcoming difficulties

There are several cons of using Canvas. Technically, my data is not self-hosted. It's on Canvas's servers, and access to my data is subject to Canvas's terms and conditions. However, I can download my courses in a standard format and import them into another LMS if push comes to shove.

Another downside is that the free version of Canvas doesn’t support uploading more than 500 MB per course. I find that plain text, HTML, Word docs, and PDFs don't dent the max capacity. Images can add up quickly. You need to compress them to JPEG before uploading them. Videos will quickly exceed the limit. If you're going to upload videos to Canvas, consider recording your videos at 720P, 10 frames per second. Then, use Handbrake to compress the video.

To work with the file upload limitation, I upload my videos to my university’s cloud storage. Then, I just link to the videos on the cloud storage from Canvas. My students also have access to the same university cloud storage, they have access to all my videos.

### Favorite features

The rubric feature is especially good. It provides a quick formula for me to use when grading exams. This is essential for programming and localization exams where excellent performance means successful completion of certain tasks with an attention to detail. Rubrics make it easy for me to look at each exam objectively and mark off items from a checklist. It reduces my cognitive stress when grading exams.

I like using the mobile app. I am frequently on the move, away from my computer. But I can quickly go to the mobile app to give a grade to a student or leave a comment.

It’s easy to weight assignment groups. Here are the weightings for my advanced English reading and writing class:
 - Midterm exam: 30%
 - Final exam: 30%
 - Writing assignments: 15%
 - Writing labs: 10%
 - Reading quizzes: 15%

Once the semester is over, the final grades are already calculated automatically.

I sometimes schedule review sessions and I can put them on the calendar on Canvas.

I write a Chrome extension that allows me to send my students' work directly to AI for assessment and receive back a score on the CEFR scale and the comments from the AI. I hope to develop more AI tools that integrate with Canvas via Chrome browser extensions.

Overall, I'm very pleased with Canvas and look forward to new features that are developed.