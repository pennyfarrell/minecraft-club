# Testing

## Code Validation

The [Stammer Minecraft Club](https://pennyfarrell.github.io/minecraft-club/) webpage was thouroughly tested. HTML code was reviewed in the [W3C HTML Validator](https://validator.w3.org). The CSS code was validated in the [W3C CSS Validator](https://jigsaw.w3.org/css-validator/). There were a few minor errors found regarding incorrect semantic use of header tags, missing closing double quote in attribute and incorrect input labels. All mistakes were corrected and both HTML and CSS files currently have no errors.

The results of HTML validation of each of the pages are as follows:

* Home Page

  ![W3C Validator test result](assets/css/testing-images/validator-w3-home-page.png)

* FAQ Page

  ![W3C Validator test result](assets/css/testing-images/Lighthouse-test-FAQ-page.png)

* Sign Up Page
  ![W3C Validator test result](assets/css/testing-images/validator-w3-signup-page.png)

The CSS Validator results are below:

![W3C CSS Validator result](assets/css/testing-images/validator-w3-jigsaw-css.png)

## Browser Compatibility

The website was tested on the following browsers: Google Chrome, Safari, Microsoft Edge and Mozilla Firefox. There were no errors discovered in the functionality of the site or the individual features.

## Responsiveness Test

Testing of responsive design was carried out manually by utilizing [Google Chrome DevTools](https://developer.chrome.com/docs/devtools) and [Responsive Design Checker](https://www.responsivedesignchecker.com/).

|        | S Galaxy 5 | iPhone 6/6S/7| iPhone 5 | iPad Mini | iPad Pro | Display <1200px | Display >1200px |
|--------|------------|--------------|----------|-----------|----------|-----------------|-----------------|
| Render | pass       | pass         | pass     | pass      | pass     | pass            | pass            |
| Images | pass       | pass         | pass     | pass      | pass     | pass            | pass            |
| Links  | pass       | pass         | pass     | pass      | pass     | pass            | pass            |



## WAVE Testing

I used the WAVE testing tool to try and ensure there are no accessibility issues with my site. 
[WAVE](http://wave.webaim.org/) (Web Accessibility Evaluation Tool) allows developers to create content that is more accessible to users with disabilities. It does this by identifying accessibility and WGAC errors.

The initial test highlighted contrast errors with the title overlays on the home page testimonial section. 
[WAVE Report - Contrast Error](assets/css/testing-images/WAVE image-text-contrast-error.png)

I fixed this by increasing the contrast of the text background by wrapping a span around the text in HTML and styling the background to a higher contrast with CSS. The report shows this error has been fixed.

[WAVE Report - Pass](assets/css/testing-images/WAVE-report.png)

There are 4 alerts in the report. The footer contact have been flagged as potential headings. This is an unordered list and intentional, so I did not change the semantics here.
[WAVE report - Headings Error](assets/css/testing-images/WAVE-report-alert-headings.png)

The alert for a redundant link is for the active link to show which page a user is on. As this is an intended feature, this was not changed. 
[WAVE report - Redundant Link Error](assets/css/testing-images/WAVE-report-alert-redundant-link.png)

The alert for a HTML5 video relates the embedded video tour. As this is an intentional feature, this was retained.
[WAVE report - HTML5 Video Error](assets/css/testing-images/WAVE-report-alert-video.png)

## Fixed Bugs

When validating the code, a few errors came up. these have been fixed. This is a summary of the main errors and steps taken to fix it: 
  
| Bug | Section | Fix |
| :----| :----| :--------:|
|Header element logo and nav bar alignment | Home page |I had help from tutor as i had difficulty aligning the logo/title to the left with the nav bar menu to the right. Adding another div and using Flex solved this. The alignment is now correct and the menu adapts from column for small screens to a row for larger screens. |
| Overuse of margin and padding to align content| Sign Up page | There was a thick bar to the right side of the signup page on screen sizes from large mobile and upwards. Unicorn revealer showed that it was from the body margin. This had been accidentally changed to counteract the alignment of the signup images, form and timetable. The body margin was reverted and the content was aligned using <div> and Flexbox styling. |
| HTML validator error "The value of the for attribute of the label element must be the ID of a non-hidden form control"  | Sign Up page  | I corrected the "ID" tags and made they were the same as the "name" tags. |
| Images correct size but zoomed in to wrong area of image | All pages | I researched the styling options for images and used image-position: center to make sure the image was focused on the central area which showed the content I wanted to be most visible. |
| I used h2 and then h4 without using h3 | Sign Up Page | I changed the h4 to h3 and this improved accessibility and semantic profile pf the page HTML. |
| No video showed when site was first deployed | Home Page | I changed the file path and created a relative filepath which solved the error. |
| Footer overflow when adding back-to-top button | All pages | A max-height command was added which fixed this error.|


## Unfixed Bugs

There are no known bugs in the project.

## Additional Testing

### Lighthouse
The application was also tested using [Google Lighthouse](https://developers.google.com/web/tools/lighthouse) in Chrome Developer Tools. The following aspects were tested:

* Performance - reveals how the site performs during loading
* Accessibility - shows if the site if accessible for all users and suggests ways to improve it
* Best Practices - indicates if the site conforms to industry best practices
* SEO - Search Engine Optimisation - shows if the site is optimised for search engine result rankings


### Results from Lighthouse 

* Home Page

  ![Lighthouse test result](assets/css/testing-images/Lighthouse-test-home-page.png) 

* FAQ Page

  ![Lighthouse test result](assets/css/testing-images/Lighthouse-test-FAQ-page.png)

* Sign Up Page

  ![Lighthouse test result](assets/css/testing-images/Lighthouse-test-signup-page.png)

* Originally, my home page results was poor on performance. I compressed the images and changed the video preload to "none" which improved the performance. For accessibility, I fixed the input aria-labels in the sign-up form which increased the score substantially.