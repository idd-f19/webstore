**Interface Development 1, Final Project**
# Web Store: Layout & Filter Content

---
## Overview

Using either the web store you created in previous semesters, or using the `index.html` supplied in this folder, develop a single-page product-list application.

In this project, you will complete three (3) deliverables outlined below:

1. Style interface and load products (due: Week 13)
2. Structure products and map by click (due: Week 14)
3. Filter products via form components (due: Week 15)

All deliverables are due before the start of class in the week shown above.


---
## To Get Started Now

Everyone complete these steps as soon as possible:

1. Hit the "Fork" button in the top-right corner of this repository to make a copy of the project to your Github account (must be logged in)
2. After forking, ensure your Github account name is shown ahead of the repository name (and the page url), for example: `your-github-name / webstore` (where `your-github-name` is your Github username, *not mine!*)
3. In VSCode, clone the repository (`Cmd + Shift + p`, search for "Git: Clone repo". Paste *your* repo url. Save to your desktop)
4. On your repository, go to "Settings" (sub menu at the top, or just add `/settings` to your repo's url). Scroll to the "Github Pages" section and change the "Source" dropdown to show "master branch" (default is likely "None").
5. Once reloaded, scroll back down to "Github Pages" and copy the page URL (it should be something like `https://your-github-name.github.io/webstore/`). Back at your repo's home page, edit the repo description and paste the URL in the "website" input field, then save.

Your repository will by tracked by the original as a fork, which will be used as your submission on the due dates automatically. All work must be committed and pushed to that repository to submit - no exceptions.

It's advised you keep your work local-only (ie, frequent commits, but don't push to remote), or keep your repository "private" until submission. If opting for the former, ensure you have a sufficient automatic digital backup method in place.

---
## Deliverables

### 1. Style interface and load products
**Due: Before class, Week 13**

#### HTML/CSS
**If you are using your own document:**
1. Replace `index.html` in this project with your own (file name should remain the same)
2. Place all necessary dependencies into the cloned folder (images, css files, etc)
3. Confirm everything shows up as you expected when testing using a local server ("Live Server" extension, or other)
4. Test styling consistency by deleting all products except one, then duplicate that product 5 times. Your page should maintains its structure.
   - Remember that you will be writing HTML from Javascript, so it's imperative that there are no odd "one off" styling dependencies
5. Update your document content to ensure it includes the required fields listed below

**If you are using index.html:**
1. Select a product theme for your store (ie, What type of products are you selling? What's the site name/brand?)
2. Add default site styling to the `body` (fonts, background, text alignment, etc) in CSS
3. Apply styling to major landmarks, like the header, footer, headings, etc, so the page is easy to ready and navigate
4. Modify content for a single product to match your site's theme and product type (ie, selling computer would not have S/M/L/XL, but may have Ram or CPU options). A product must also include the required fields below. Also review the entire site and modify content as you see fit. *You should modify this document extensively! **Make the page unique.***
5. Fully style all aspects of one product element to completion (they all currently have `.product` class applied to them). Any classes applied must be general and repeatable.

**In either case, before beginning your Javascript coding, ensure your page:**
- Passes w3c validation: <https://validator.w3.org/#validate_by_input>
- Scores green across all Google Chrome "Audit" metrics
  - Chrome Developer Tools > "Audit" Tab > Device: "Mobile" > "Run audits"


#### Javascript

##### A. Product Data
 
Structure data for five sample products, each as its own Object `{}` stored as a `const` variable, named from `product0` to `product4`. Vary the content for each product so that they all appear to be distinctly different when loaded into the document.

At minimum, each product should include:
- `id` (a unique identifier - a sequential Number works great)
- `name`
- `image` (a url, relative to the root folder)
- `description`
- `price`
- `quantity` (in stock)
- Some selectable criteria (`size`, `color`, etc)

Other example data points to consider (optional):
- `category`
- `rating`
- `seller` (if you are creating an *open-market* type application)
- Split `price` into `priceRegular` and `priceSale`
- Add other data points of your own

It may help you to create a Spreadsheet (Google Doc or Office 365) of products to determine what information might be helpful to track  products for a web store.

Each object must have the same identical data structure. If a value is not available or not applicable, use the keyword `null` as the value (no quotes) to show that the value has not yet (or never will be) set.

##### B. Writing `document` Content

Remove all example products from your HTML document, leaving in their place a single block element with `id="products"` to hold the new data that will be dynamically generated.

Write a function that receives a **product** (Object) as a *parameter* and will `return` a String of structured contentful-HTML. The return String should include all the necessary unique data from the Object that was received.

Note that some product data (like the product's `id`) may not be necessary for output, but will be useful later. Simply ignore those data points.

At the bottom of your JS file, call upon the custom function once for each of the product Objects you wrote. With each call, append the `return` String (the structured HTML) to the document element with `id="products"`.

You should now have five identically structured products with data that's written from Javascript.

#### Criteria Assessed
1. Code syntax and project setup
2. Scalability of content and style
3. Data structuring of products
4. Output of content to the document


### 2. Formalize structure and map by click
**Due: Before class, Week 14**

- Structure all products Objects into an Array
- Use a combination of the various Array functions to create one HTML Element for each complete product stored
- Increase list of items to at least 10 (all should have the same structure, but content should be very different)
   - Notes: If a property doesn't have/need a value for one element, give it a value of `null`
- Add a `click` listener to an Element in the `document` that does *something* (loads products, adds a class, etc)
- Dynamically style for various product states (limited supply, unavailable, categories, sale, clearance, etc)
- Prepare and test for pagination
  - Ensure the pagination component (list of clickable page numbers) is styled
  - Experiment: print only the first 5 products (use "splice()")


### 3. Filter products on form submit
**Due: Before class, Week 15**

- Increase total number of unique products to 20
- Capture form events and the relevant data
- Filter products before display by at using at least **two** separate filter conditions
  - For example: price range (high and low) and colour


Other (optional) ways to go "above and beyond":
- Sort by a product property (try numerical and string)
- Paginate your document
- Take direction from the user in regard to how many products to show per page
- Make product buttons clickable (for adding to cart)
- Create an array to hold the `id` of some products (ex, favourited or added to cart)


---
## Rubric

Each developed aspect of the project is measured using the following criteria:

- **Level 1 (Below Expectation):** Lack of practical understanding of material or concepts
- **Level 2 (Approaching Standard):** Fundamental understanding, but needs additional practice to meet required standard
- **Level 3 (Standard Met):** Strong grasp of concepts; some room for maturity
- **Level 4 (Mastered):** Expert level knowledge, would be able to effectively teach others

#### A Note on Expectations

Because this project is mostly lead in class, completing the project as per exact specification for each deliverable in each category will result in a *maximum* grade of 70% in that category. To earn additional grades in each category, you will be required to think outside the box and complete additional functionality.

For example, consider something like product "states". If a product is low on quantity, is that shown to the user? Is that different than when a product is sold out? What about if a product has been added to the cart? Writing and testing additional classes and places to put custom content or messaging to help with state management is one ways to start thinking beyond just "evergreen" content. 

Experiment with other sites and applications that sell products. Start thinking like a user - what's required to make this interface most usable or most unique?

