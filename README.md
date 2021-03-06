# 1.0) The Life of Julius Caesar

The internet is full of high quality sources to help students of history, teachers and enthusiasts of history-studies access primary sources. These are however often overshadowed by more accesible sites with less thorough or vetted information such as wikipedia. A primary reason for users prefering the ease of use of Wikipedia is that Wikipedia was designed for browser-reading from the start. Most sites presenting historical documents online tend to either be direct copies of the text and sometimes actual photo-copies of the physical document!

The purpose of this site is to provide an educational site, designed to be used by teachers, students and enthusiasts of the Roman period. I have elected to take a 1911 translation of the Life of Julius Caesar, in the public domain, and republish it in a digital format with a design centered around providing modal-views explaining difficult concept as well as a thorough list of suggested further reading. The hope is that repackaging the content in this way will make reading Suetonius more accesible and fun, increasing interest in the user to read more about the Roman period.



## 1.1) UX design

This website is for the following three groups:

Teachers, looking to provide their students with a more accessible way to study the life of Julius Caesar.
Students, looking to find the original source material faithfully reproduced but also with annotations to make it easier to follow.
Enthusiasts, people who enjoy reading history, who will benefit from getting the original words of Suetonius while also finding links to further reading on the period.

As I have contacts who work in library and information science, I discussed the formatting of the read-now.html site extensively with them, to ensure it was easily browsed by readers. Eventually the decision was made to cut the full lenght text into 6 separate pages and add browsing between these pages through a bootstrap navbar dropdown and a pair of "back" and "forth" buttons stickied to the navbar. I considered other methods such as nested dropdowns, per-section ID-linking but in the end I decided that this was the more clear and feasible way to implement the full text without redacting or distracting from the content.


## 1.2) Wireframes

I created a set of wireframes with Balsamiq to aid in the design process, they can be viewed [HERE](assets/wireframes/MS1-wireframe.pdf)

## 1.3) User stories:

A teacher who wants to make Suetonius more accessible to their class could go straight for the "Read now!" link in the Navigation section and find the text reproduced in full.

A student who is writing a paper on Caesar could utilize the chapter-browsing feature to quickly  find information and quotes in each pages' quick summary

Enthusiasts can use the further-reading segment to find a variety of resources to find more information about the Roman period, ranging from podcasts to books to documentaries.


# 2.0) Features 

A full-length reproduction of the Life of Caesar in a 1911 translation whose copyright has expired.

Browsing-by-chapter through the Navbar in relevant pages, ensuring readability

A gallery of images related to the life of Caesar

A series of suggested further readings

## 2.1) Features left to include

Further reproductions of Suetonius work

A modal-system, including definitions of various latin and Roman terms for beginners

Including PhP code to activate the contact.html form



# 3.0) Testing process

I went through multiple stages of testing, before and after deployment. 

## 3.1) Stage One - Pre-deployment testing 26/2

In this stage, I implemented boilerplate html-templating. I used Visual Studio Code to write all code, with added bootstrap functionality from a Marketplace add-in to generate template for basic bootstrap and grid function on index.html. ( Relevant link: https://marketplace.visualstudio.com/items?itemName=thekalinga.bootstrap4-vscode )

Once I had generated a workable general layout that matched my design in wireframes, I used the chrome DevTools to test a variety of resolutions and to test responsiveness. 
Once I was satisfied with this stage of the process, I performed my first commit on February 27th.

## 3.2) Stage Two - Content testing 30/2

The site being primarily intended as a e-reading aide, UXD design for the chapters was very important for readability. I have friends in publishing and in library work and consulted
on the design of the chapter and navbar. Multiple iterations were gone through, with updates performed to the design for readability and navigation, particularily on small screens. Final CSS designs and all content was implemented on the 9th of March, at which point I did a new commit and push.

## 3.3) Stage Three - Temporary deployment 8/3

I deployed the site to a temporary URL on a free hosting-service and shared the URLs with a set of testers, asking them to try different resolutions and report anything amiss. Testing was conducted on the following devices:

iPhone 5/6/7/8
Samsung Galaxy 7
Asus Zenphone 
iPad 4
Microsoft Surface Go
Desktop (Resolution: 1920x1080) with browsers Safari, Mozilla, Chrome and Edge.

In addition, testing was done with DevTools on a variety of common resolutions.

A series of display errors on small resolution screens, related to the contact form. Multiple errors had occured on the pages labelled in this build as read-now-*, with chapters that were outside their display-box. This was a HTML error in the template I had made for this series of pages.

## 3.4) Stage Four - REM compatibility 13/3

On the 12th of March, I was checking Slack for input on industry standards to make sure I was in compliance. I was informed that styling should be done in REM units, for better responsiveness. I reworked my CSS sheet to make it compatible with REM as the standard font-sizing measurement. While ensuring I was in compliance with other industry standards, I also found that I had mislabelled all read-now-*.html files, in that I had included dashes in their filenames. After manually testing the REM units to ensure there were no major display errors caused, I did a new git push.

## 3.5) Stage Five - Second mentor consultation 17/3

A few issues were raised during my second mentor-meeting. Specifically, readability with the grid-columns, issues with the carousel "jumping" upon slide and overlap of the bootstrap slide indicators and the text as well as restyling contact.html for better readability. I fixed the carousel by applying fixed heights in pixels to the surrounding container and the images themselves, and some adjustments of margins.

## 3.6) Stage Six - Validation 22/3

After implementing the changes suggested in our last meeting, I went on to perform HTML and CSS validation using the following validator: [W3C Validation Service](https://validator.w3.org/)

Errors found in index.html related to a stray </div> and an improper "name" tag on a button. These errors were fixed.

Errors found in about.html was another stray </div> that was fixed.

Errors found in contact.html were a pair of elements lacking an "ID" tag in the form.

No errors were found in read-now.html through read-now-5.html. Errors found in read-now-6.html were related to a mislabelled ID on the navbar link and was fixed.

CSS validation found 4 errors, all related to syntax in shorthand-margins. These errors were fixed.


## 3.7) Stage Seven - Peer Review 24/3

I submitted the project for peer review on slack on the 24/3 and asked for feedback both on looks, code and documentation. Feedback on the documentation was generally good. A slight resolution error on contact.html was discovered on a Samsung A40, a handheld small-screen phone with high-resolution (1080x2200pixels) - I reworked contact.html accordingly, using bootstrap form-classes to make it more responsive and less error-prone, as it had previously relied on direct media-queries and normal HTML for the form styling.

## 3.8) Stage Eight Final mentor meeting 26/3 

I presented my work to my mentor for final notes. He had some notes on making certain elements of the README more readable and for being more specific in my documentation. After reviewing my code, I followed instructions from the milestone guidelines and ran my CSS through the vendor-prefixer [HERE](https://autoprefixer.github.io/). After testing these CSS changes locally, I performed a commit and push. I then submitted the project.


# 4.0) Deployment

Deployment was made from GitHub onto GitHub pages, following the following instructions: 

https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages

1) Open the repo
2) Scroll down to github pages
3) Select the correct branch as the source
4) You will be able to see if it was correctly deployed by the checkmark.

Deployment was easily configured by following those instructions and generally uneventful.

Instructions for cloning the repository here:

https://help.github.com/en/articles/cloning-a-repository

# 5.0) Technologies used:


Languages used in the project are primarily HTML5 and CSS, with some JavaScript included to ensure Bootstrap works properly. 

I used Bootstrap 4 for responsive site-design.

Balsamiq for wireframe design

GitHub was used to provide version-control throughout the process.

I wrote the vast majority of the code in Visual Studio Code, for ease of use when I was in a no-wifi area at my workplace. VS-Code is a lightweight IDE with many optional plug-ins, one of which was exceptionally useful to this project:

I used the following plugin to generate quick bootstrap templates for the main HTML:

https://marketplace.visualstudio.com/items?itemName=thekalinga.bootstrap4-vscode 

All other code was produced with instructions from course-materials and by referencing the bootstrap documentation when neccesary:

https://getbootstrap.com/

