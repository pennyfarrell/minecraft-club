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


## Fixed Bugs

When validating the code, a few errors came up especially 
  
| Bug | Section | Fix |
| :----| :----| :--------:|
|Section element used without a header element | All pages |I changed most of the section elements without a header into a div element. On the Contact Us page, however, I included a header with display none, as I did not want to change the look of the page, but had wanted to use the semantically more appropriate element (section rather than div).|
| Use of paragraph element within a span element| Contact Us page | I changed the span element into div element. |
| "li" element around anchor element for the map icon missing  | Find Your Group page  | I added the missing "li" tags  |
| Navigation bar jumping up/moving when hovered on | All pages | I had to take away the padding which I had added to the anchor element in hover position and give it to the anchor element in static position. I also changes the border property for outline property which does not increase the size of the box. |
| I used h1 instead of h2 in inappropriate places | All pages | I changes h1 to h2 in the relevant cases to improve accessibility and increase semantic sense. |
| No images showed when site was first deployed | All pages | I had used two dots (../) instead of just one dot (./) in the relative path for the images. This was easily corrected by taking away one of the dots. |
| Images distorted/blurry | Find Your Group page | I used "object-fit: cover" to fix this issue. |
| Footer overflowing on small screens | All pages | A min-width had been set to the email in the footer. I avoided this issue by substituting the long email address by an envelope icon. |


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

  ![Lighthouse test result](assets/css/testing-images/Lighthouse-test-home-page.png) ***** performance

* FAQ Page

  ![Lighthouse test result](assets/css/testing-images/Lighthouse-test-FAQ-page.png)

* Sign Up Page

  ![Lighthouse test result](****** accessibility input labels)

* Originally, my site results were poor on performance and on accessibility. I compressed all images using [the Squoosh app](https://squoosh.app/) and it improved the peformance significantly. As for accessibility, I added extra aria-labels especially for the form which increased the score substantialy.