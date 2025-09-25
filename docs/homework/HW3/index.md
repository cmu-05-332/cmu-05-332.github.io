# HW3: Accessibility Evaluation

## Learning Goals

* You will explore making content that is accessible  
* You will explore how to use tools to automatically assess the accessibility of web pages.  
* Determining whether a web page is accessible can be difficult to do automatically, and so part of the goal of this exercise is to become familiar with some of those limitations.

## Project Context

In this week’s homework, you will make a web page more accessible. The web page you’ll start with has been constructed to allow you to practice with a wide variety of different kinds of web content, and thus practice making a variety of web page content accessible. Another way of saying this is that the web page you’ll start with is absolutely dreadful, but we have seen all of the problems it contains on web pages not only “in the wild” but in accessibility evaluations.

This is an **individual assignment** worth 100 points.

## Getting Started

The purpose of this web page is to advertise accessibility and provide some hints for people who want to get started. You’ll make the basic web page accessible, make its embedded video accessible, etc. The page is a bit ridiculous because of how many different kinds of content it contains all on one page, but is formed of fairly common components.

The base web page (HTML, CSS, and Javascript) files can [be downloaded here](https://cmu-05-332.github.io/homework/HW3/homework3-base-webpage.zip).

The final state of the web page will look visually similar, but it will be much more accessible\! Your final web page might look a bit different. Please feel free to deviate from the style here if you need to do so for better accessibility or usability.

Below is a list of what you’ll need to do for this assignment. As your write-up, please keep a “lab notebook” that includes the results from the activities below. You’ll turn in that, along with your final web page.

## Instructions

### Exploring Automatic Accessibility

Before getting started in your manual evaluation of the accessibility of this page, use one of the many (free) accessibility evaluation tools to get a quick sense of obvious problems that should be fixed. There are many such tools, and you’re free to use whatever one you want, but one good option is [WAVE](http://wave.webaim.org/extension/). There are others so feel free to explore.

Copy & paste the output from WAVE (or your preferred tool) into your lab notebook. Then write a short description of the main problems that the tool was able to discover.

### Making the Page Accessible

To make the web page accessible, please pay attention to the following points. To receive full points please find and fix at least one problem in each category below; you can earn up to 10 points for each category.

Record in your lab notebook a description of each problem, your estimate of the severity of the problem, how you fixed it, and whether or not it was detected by the automatic accessibility evaluator you tried in the previous step. You might optionally also look up what guideline it breaks in [WCAG 2](https://www.w3.org/WAI/intro/wcag), and note the level of compliance it corresponds to (A, AA, AAA).

1. [Headings and Landmarks](https://cmu-05-332.github.io/homework/HW3/#headings-and-landmarks)  
2. [Good Alternative Text for Images](https://cmu-05-332.github.io/homework/HW3/#good-alternative-text-for-images)  
3. [Form Labels](https://cmu-05-332.github.io/homework/HW3/#form-labels)  
4. [Video Captions](https://cmu-05-332.github.io/homework/HW3/#video-captions)  
5. [Audio Descriptions](https://cmu-05-332.github.io/homework/HW3/#audio-descriptions)  
6. [Tab Order & Visible Focus](https://cmu-05-332.github.io/homework/HW3/#tab-order-and-visible-focus)  
7. [Color Contrast](https://cmu-05-332.github.io/homework/HW3/#color-contrast)  
8. [Keyboard Access](https://cmu-05-332.github.io/homework/HW3/#keyboard-access)  
9. [Information Conveyed Only via Color](https://cmu-05-332.github.io/homework/HW3/#information-conveyed-only-via-color)

#### Headings and Landmarks

Headings and landmarks provide an outline for the web. This helps in reading, but also helps in efficiently navigating the page if you’re using a screen reader. Headings are the \\\<h1\> through \\\<h6\> HTML tags.

You can read more about headings and other elements for providing semantics at this WebAim article on [Semantic Structure](http://webaim.org/techniques/semanticstructure/#contentstructure).

#### Good Alternative Text for Images

Visual information have an alternative text form so that users who can’t see the content can still access that information. While somewhat intuitive, deciding on good alternative text and which images need alternative text can be a little tricky. When in doubt, label an image.

You can read more about images and alternative descriptions at this WebAim article on [Alternative Text](http://webaim.org/techniques/alttext/).

#### Form Labels

Providing labels for form fields makes them easier to understand for someone who is not viewing the visual layout of the page, or is not viewing it in the way it was designed for (e.g., at a different level of magnification).

You can read more about form labels, including what makes a good form label and how to assign them on this WebAim article on [Creating Accessible Forms](http://webaim.org/techniques/forms/controls).

#### Video Captions

A deaf or hard of hearing person cannot listen to video content without a suitable visual substitute. One way to do that is to provide captioning for the video, which means creating a text alternative for the speech in the video and allowing it to be displayed.

Different video players have different ways of allowing you to provide captions. One relatively easy way to create captions is to upload your video to YouTube, [request it automatically caption your video](http://ncdae.org/resources/cheatsheets/youtube.php), and then [edit those captions](https://support.google.com/youtube/answer/2734705?hl=en). Once you do this, you can either keep your video on YouTube, and use the embedded player to put the content on your own site. Or, you can [download the caption file](http://downsub.com/), and put it into your own player. For example, the HTML5 \\\<video\> tag [accepts captioning files](https://developer.mozilla.org/en-US/Apps/Fundamentals/Audio_and_video_delivery/Adding_captions_and_subtitles_to_HTML5_video), and is pretty easy to use once you have created the captioning.

#### Audio Descriptions

Audio descriptions are the video equivalent of alternative text for images. Oftentimes, visual content in an image is not mentioned in the audio track. In that case, you’ll need to provide information about the visuals in the audio track so that people who can’t see the visuals have access to them. This can be tricky, mostly because of timing \-- it can be really hard to fit in audio descriptions into natural pauses.

You can add video descriptions in a few different ways. One is to use video editing software, such as Adobe Premiere or iMovie, to add a new audio track to the video that contains the descriptions. Another way is to upload your video to YouTube, and then use the [YouDescribe](https://youdescribe.org/) service to add the alternative descriptions. For some reason, it’s a little tricky to find the video you want to describe from the YouDescribe interface \-- the best approach I’ve found is to post your video publicly on YouTube, then search for your username, which should display all of your public videos.

Regardless of tool used, you’ll want to think about what you’ll need to describe, versus what doesn’t need visual description. For instance, if a person is talking, there’s probably no reason to say that there is a person on-screen. But, you might want to describe facial expressions, or mention someone sneaking onto the screen.

Here’s a video describing [how to create audio descriptions using iMovie](https://www.youtube.com/watch?v=1siUNBsR_Gg), including a number of useful tidbits about what goes into a good audio description. Here’s a short [professionally-created video that has been audio described](https://www.youtube.com/watch?v=H9j1qKRaIMw). You might also check out your favorite movie’s special features to see if it has an audio description track that you can turn on. Many popular movies have these nowadays\!

#### Tab Order and Visible Focus

A proper tab order means that as you move through the page with the TAB and SHIFT-TAB keys, a logical order is followed. This is the natural result in simple pages, but as content can be placed pretty much wherever you want. And, as web pages are increasingly formed by bringing in content for various sources, sometimes the result is a nonsensical order.

Another element of this is that to be able to effectively “tab through” a web page, you need to be able to see what element currently has focus. Setting the outline property to “none” in CSS, or making the change on focus too difficult to see, can make doing so very hard. The focused element on a page should be easily visible.

WebAim has more about these issues in its [Keyboard Accessibility](http://webaim.org/techniques/keyboard/) page.

#### Color Contrast

The foreground and background need to have sufficient contrast in order to be possible to see. WCAG 2.0 provides very specific guidance on acceptable contrast levels, but you might wonder how you can test that? Fortunately, WebAim has a [free and easy contrast checker](http://webaim.org/resources/contrastchecker/).

#### Keyboard Access

All functions of the page should be possible to use with the keyboard. This is important for people who can’t use the mouse, or are using some other input device that effectively acts as a keyboard. Most “soft keyboards” effectively act as a keyboard as far as the web page is concerned. Software keyboards take input from switches, head mouses, speech, eye gaze, etc., and turn it into key presses. So, if a page doesn’t work for a keyboard, it won’t work for these inputs either.

We already covered tab order and visible focus in a previous item, so for this item you’re looking to make sure that all functionality is possible without the mouse, i.e., can you press all the buttons, follow all the links, interact with form controls, etc.

#### Information Conveyed Only via Color

Information conveyed only in color is not accessible to people who cannot see or who have limited color vision. As a result, color should be supplemented with other content that is more semantic in order to make it accessible. Avoid such things as, “the items in blue are required”, or denoting links only by their color (and not by some other font decoration, such as underlining).

You can learn more about color blindness and other related issues at WebAim’s article on [Color-blindness](http://webaim.org/articles/visual/colorblind).

## Deliverables

The final website files and a PDF of your lab notebook as one archive (.zip) turned in to Canvas by Wednesday, September 17th, 11:59pm ET.  
