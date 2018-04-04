# Microdata-JSON-LD-Schema.org-Rich-Snippets
This guide has been created to provide a quick and easy way of generating different types of rich snippets for your website, using a combination of Schema.org and either Microdata or the recently endorsed JSON-LD.

I must point out that before you proceed with integrating any form of mark-up, you should be aware of the guidelines provided by Google, and Bing. Any attempt to mark-up content that is invisible to users, or content that is irrelevant/misleading just to generate the rich snippet may result in action being taken against your website.

1. [**What is Microdata?**](#what-is-microdata)
2. [**What is JSON-LD**](#what-is-json-ld)
3. [**What is Schema.org?**](#what-is-schemaorg)
4. [**Why use mark-up?**](#why-use-mark-up)
5. [**Using Review Data to Enhance Your Search Result Snippets**](#using-review-data-to-enhance-your-search-result-snippets)
6. [**Draw Attention to your Products with Richer Snippets**](#draw-attention-to-your-products-with-richer-snippets)
7. [**Maximise the Impact of Editorial Reviews in Search**](#maximise-the-impact-of-editorial-reviews-in-search)
8. [**Swoop a Grammy by Marking-up Movie Content**](#swoop-a-grammy-by-marking-up-movie-content)
9. [**Bring Your TV Listing Search Results to Life**](#bring-your-tv-listing-search-results-to-life)
10. [**Show Business Credibility in Search Results**](#show-business-credibility-in-search-results)
11. [**Use Recipe Mark-up to Generate Appetising Rich Snippets**](#use-recipe-mark-up-to-generate-appetising-rich-snippets)
12. [**Add Authenticity & Trust to Mobile App Listings**](#add-authenticity--trust-to-mobile-app-listings)
13. [**Promote Software Applications in Search Results**](#promote-software-applications-in-search-results)
14. [**Tell Us About Yourself with Person Mark-up**](#tell-us-about-yourself-with-person-mark-up)
15. [**Sell Tickets for Multiple Events with a Single Search Listing**](#sell-tickets-for-multiple-events-with-a-single-search-listing)
16. Dramatically Increase Size of Search Results for Audio Coverage
17. Generate Rich Media Listings with Video Mark-up
18. Create Interactive Breadcrumb Trails for your Search Listings
19. Logo & Social Sitelinks in Knowledge Graph
20. SearchAction – Sitelinks Search Box
21. InDepth Article Markup
22. Gmail
    - View Action
    - Save Action
    - Confirm Action
    - RSVP Action
    - Numeric Rating
    - Parcel Delivery
    - View Order
    - Event Booking
    - Flight Booking
23. Tools & Resources
    - Tools
    - Plugins
       - Wordpress
       - Magento
       - Joomla
       - Drupal
    - Useful Resources

## What is Microdata?

Microdata (like RDFa and Microformats) is a form of semantic mark-up designed to describe elements on a web page e.g. review, person, event etc. This mark-up can be combined with typical HTML properties to dedlfine each item type through the use of associated attributes. For example, ‘Person’ has the properties name, url and title – attributes can be applied to HTML tags to describe each property:

```HTML
<div itemscope itemtype="http://data-vocabulary.org/Person">
  Name: <span itemprop="name">Özgür Can Karagöz</span>
  Website: <a href="https://www.oxyn.org" itemprop="url">oxyn.org</a>
  Title: <span itemprop="title">Head of SEO</span>
</div>
```

- [X] 1 - Itemscope – is an indicator that the content within this <div> is an item.
- [X] 2 - Itemtype – describes what the item is, in the above instance ‘Person’.
- [X] 3 - Itemprop – describes each property of the specific item.
  
**Further Reading:** [About microDATA](https://developers.google.com/search/docs/guides/intro-structured-data?visit_id=1-636582308679739602-3891983355&hl=en&rd=1) – Google Webmaster Help, [HTML Microdata](https://www.w3.org/TR/microdata/) – W3C
  
## What is JSON-LD

Based on the popular JSON format, the linked data format JSON-LD allows webmasters to define the context of the data contained through the use of types and properties. When combined with Schema.org, these properties follow a standardised mark-up supported by major search engines, and joins Microdata & RDFa as methods for integration. Unlike Microdata & RDFa, JSON-LD offers greater ease of implementation with all the necessary mark-up contained within inline <script> tags, instead of wrapping HTML properties. However, as elegant and lightweight that JSON-LD is, there are some potential road blocks. In some instances it’s just not practical to mark-up content, for example that on a larger scale, as the content would need to be effectively repeated within the script tags in order to validate. Also as the mark-up is invisible, the likelihood of marking up content that is not on the visible page increases, which is against search engine usage guidelines. It is for these reasons that Google in particular still favours Microdata & RDFa for marking up HTML content.

**Further Reading:** [What is JSON-LD](https://json-ld.org/) – JSON-LD.org, [JSON-LD](https://developers.google.com/search/docs/guides/intro-structured-data) – Google Developers, [Structured Data Testing Tool](https://search.google.com/structured-data/testing-tool) (New) – Google Developers.

## What is Schema.org?

Schema.org is a universally supported vocabulary extension by Google, Microsoft and Yahoo! for mark-up languages such as Microdata. It is designed to make the lives of webmasters easier, by offering one standardised mark-up understood by all the major search engines. Currently, Schema.org is compatible with Microdata, RDFa and JSON-LD.

**Further Reading:** [What is Schema.org](http://schema.org/) – Schema.org, [Schema.org FAQ](http://schema.org/docs/faq.html?visit_id=1-636582311145661231-2254729040&hl=en&rd=1) – Google Webmaster Help.

## Why use mark-up?

Marking up content on your website can:

- Lead to the generation of rich snippets in search engine results e.g.

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/sg-ebay.png" />


- This has the potential to enhance CTR from the search results from anywhere between 10-25%.
- Search engines and organisations are using this mark-up to develop new tools, for example Google Recipe Search, which may open up other marketing channels if not now, in the near future.
- Provide greater information to search engines to improve their understanding of the content on your website.

## Using Review Data to Enhance Your Search Result Snippets
### Example live snippet
<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/sg-ebay.png">

### 1.2 The core mark-up features at a glance:
**Itemtype** attributes utilised:

| Itemtype      | Description   |
| ------------- | ------------- |
| http://www.schema.org/AggregateRating      | The average rating based on multiple ratings or reviews. |
| http://www.schema.org/Review               | A review of an item e.g. product or movie.               |
| http://www.schema.org/Rating               | An individual rating given for an item.                  |
	
**Itemprop** attributes utilised:

| Itemprop      | Description   | Property of   |
| ------------- | ------------- | ------------- |
| itemprop=“name”             | The name of the item being marked up. | All |
| itemprop=“description”      | Describe the item being marked up.    | All |
| itemprop=“aggregateRating”  | The overall rating, based on a collection of reviews or ratings of the item.                  | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=“ratingValue”      | The rating for the content.           | [Rating](http://schema.org/Rating) |
| itemprop=“reviewCount”      | The total number of reviews.          | [AggregateRating](http://schema.org/AggregateRating) |
| itemprop=“author”           | The author of this content. HTML 5 rel=author tag can be utilised instead. | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=“datePublished”    | Date of first broadcast/publication.  | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=“reviewRating”     | The rating given in this review.      | [Rating](http://schema.org/Rating) |
| itemprop=“reviewBody”       | The actual body of the review.        | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=“worstRating”      | The lowest possible rating.           | [Rating](http://schema.org/Rating) |
| itemprop=“bestRating”       | The highest possible rating.          | [Rating](http://schema.org/Rating) |


### 1.3 The mark-up
The following code examples form the bare-bone template mark-up for review data. The first part of this example forms the aggregate rating, and could be utilised by itself to generate the rich snippet from point 1.1:

**JSON-LD**

```javascript
<script type="application/ld+json">
{
  "@context": "http://schema.org",
  "@type": "Product",
  "name": "[the name of the product]",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "[rating]",
    "reviewCount": "[number of reviews]"
  }
}
</script>
```
**Microdata**

```HTML
<div itemscope itemtype="http://schema.org/Product">
  <span itemprop="name">[the name of the product]</span>
  <div itemprop="aggregateRating" itemscope itemtype="http://schema.org/AggregateRating">
    <span itemprop="ratingValue">[rating]</span> stars – based on
    <span itemprop="reviewCount">[number of reviews]</span> reviews
  <div>
</div>
```
The second piece of mark up should be utilised on each review, this also adds further validity to the aggregate rating defined above:

**JSON-LD**

```javascript
<script type="application/ld+json">
{
  "@context": "http://schema.org",
  "@type": "Product",
  "name": "[the name of the product]",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "[rating]",
    "reviewCount": "[number of reviews]"
  },
  "review": [
    {
      "@type": "Review",
      "name": "[review title/summary]",
      "author": "[name of reviewer]",
      "datePublished": "[date in ISO format e.g. 2012-04-15]",
      "description": "[the actual user review text]",
      "reviewRating": {
        "@type": "Rating",
        "bestRating": "[highest possible rating]",
        "ratingValue": "[rating given by reviewer]",
        "worstRating": "[lowest possible rating]"
      }   
    }
  ]
}
</script>
```

**Microdata**

```HTML
<div itemprop="review" itemscope itemtype="http://schema.org/Review">
  <span itemprop="name">[review title/summary]</span> - by
  <span itemprop="author">[name of reviewer]</span>,
  <meta itemprop="datePublished" content="[date in ISO format e.g. 2012-04-15]">April 15th, 2012
  <div itemprop="reviewRating" itemscope itemtype="http://schema.org/Rating">
    <meta itemprop="worstRating" content="[lowest possible rating]">
    <span itemprop="ratingValue">[rating given by reviewer]</span>/
    <span itemprop="bestRating">[highest possible rating]</span>stars
  </div>
  <span itemprop="description">[The actual user review text]</span>
</div>
```

### 1.4 The Test…
Filling in the blanks, the resulting snippet using the structured data testing tool should resemble something like this:
<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/test-1-1.png" />

**Further Reading:** [Review Schema.org Creator](https://raventools.com/site-auditor/seo-guide/schema-structured-data) – Raven Tools, [Rich Snippets: Reviews Video](https://www.youtube.com/watch?v=n0SF6PLCx4I) – Google Webmaster Help, [Review & AggregateRating](http://schema.org/AggregateRating) – Schema.org

# Draw Attention to your Products with Richer Snippets
### 2.1 Example live snippet

Extending the capability of the review mark up for products can lead to this type of rich snippet:

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/sg-ebay.png" />

### 2.2 The core mark-up features at a glance:
**Itemtype** attributes utilised:

| Itemtype      | Description   |
| ------------- | ------------- |
| http://www.schema.org/Product              | Describes a product on sale.                              |
| http://www.schema.org/Offer                | Describes a products offer details.                       |
| http://www.schema.org/AggregateRating      | The average rating based on multiple ratings or reviews.  |

**Itemprop** attributes utilised:

| Itemprop      | Description   | Property of   |
| ------------- | ------------- | ------------- |
| itemprop=“name”             | The name of the item being marked up. | All |
| itemprop=“description”      | Describe the item being marked up.    | All |
| itemprop=”price“            | The price stated for a product.       | [Offer](http://schema.org/Offer) |
| itemprop=”aggregateRating“  | The overall rating, based on a collection of reviews or ratings of the item.  | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=”ratingValue“      | The rating for the content.           | [Rating](http://schema.org/Rating) |
| itemprop=”reviewCount“      | The total number of reviews.          | [AggregateRating](http://schema.org/AggregateRating) |

### 2.3 The mark-up

Exploiting review mark-up for a product with offer details:

**JSON-LD**

```javascript
<script type="application/ld+json">
{
  "@context": "http://schema.org",
  "@type": "Product",
  "name": "[product name]",
  "offers": {
    "@type": "Offer",
    "price": "[product sale price]",
    "priceCurrency": "[currency in 3 letter ISO 4217 format e.g. USD]"
  },
    "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "[aggregate rating given]",
    "reviewCount": "[number of reviews]"
  }
 }
 </script>
```

**Microdata**

```HTML
<div itemscope itemtype="http://schema.org/Product">
  <span itemprop="name">[product name]</span>
  <span itemprop="offers" itemscope itemtype="http://schema.org/Offer">
    <span itemprop="price">[product sale price]</span>
  </span>
  <div itemprop="aggregateRating" itemscope itemtype="http://schema.org/AggregateRating">
    <span itemprop="ratingValue">[aggregate rating given]</span> stars – based on
    <span itemprop="reviewCount">[number of reviews]</span> reviews
  </div>
</div>
```

As an aggregate review rating has been given for this product, the individual corresponding user reviews will need to be marked up using the code identified in part two of point 1.3.

### 2.4 The Test…

Filling in the blanks, the resulting snippet using the structured data testing tool should resemble something like this:

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/2-4test.jpg" />

### 2.5 Extending this mark-up

By altering the /Offer segment of the code to the below we can add a price range to the snippet:

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/2-5test.jpg" />

**JSON-LD**

```javascript
JSON-LD DISPLAYED IN ITS ENTIRETY:
<script type="application/ld+json">
{
  "@context": "http://schema.org",
  "@type": "Product",
  "name": "[product name]",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "[aggregate rating given]",
    "reviewCount": "[number of reviews]"
  },
  "offers": {
    "@type": "AggregateOffer",
    "lowPrice": "[lowest product price]",
    "highPrice": "[highest product price]",
    "priceCurrency": "[currency in 3 letter ISO 4217 format e.g. USD]"
 }
}
</script>
```

**Microdata**

```HTML
<span itemprop="offers" itemscope itemtype="http://schema.org/AggregateOffer">
  <span itemprop="lowPrice">[lowest product price]</span> to
  <span itemprop="highPrice">[highest product price]</span>
</span>
```

This can be further extended to include ‘In Stock’ within the rich snippet by including the following line also within the /Offer segment:

```HTML
"availability": "http://schema.org/InStock"
<link itemprop="availability" href="http://schema.org/InStock" >
```

**Further Reading:** [Product Schema.org Creator](http://schema-creator.org/product.php) – Raven Tools, [Rich Snippets: Products](https://developers.google.com/search/docs/data-types/product?visit_id=1-636582735837372902-962109021&hl=en&rd=1) – Google Webmaster Help, [Product](http://schema.org/Product) & [Offer](http://schema.org/Offer) – Schema.org

# Maximise the Impact of Editorial Reviews in Search

### 3.1 Example live snippet

Individual reviews in an editorial format can also be marked up to generate an extension of the ratings snippet to include the author name and publication date:

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/3-1example.jpg" />

### 3.2 The core mark-up features at a glance:

**Itemtype** attributes utilised:

| Itemtype      | Description   |
| ------------- | ------------- |
| http://www.schema.org/Review               | A review of an item e.g. product or movie.                |
| http://www.schema.org/Rating               | An individual rating given for an item.                   |

**Itemprop** attributes utilised:

| Itemprop      | Description   | Property of   |
| ------------- | ------------- | ------------- |
| itemprop=“itemreviewed”     | The name of the item being reviewed.  | [Review](http://schema.org/Review) |
| itemprop=“worstRating”      | The worst possible rating.            | [Rating](http://schema.org/Rating) |
| itemprop=“bestRating”       | The highest possible rating.          | [Rating](http://schema.org/Rating) |
| itemprop=“ratingValue”      | The rating for the content.           | [Rating](http://schema.org/Rating) |
| itemprop=“datePublished”    | The publication date of the review.   | [Review](http://schema.org/Review) |
| itemprop=“author”           | The name of the author.               | [Review](http://schema.org/Review) |

### 3.3 The mark-up

The mark-up for an editorial review:

**JSON-LD**

```javascript
<script type="application/ld+json">
{
  "@context": "http://schema.org",
  "@type": "Review",
  "itemReviewed": "[The item being reviewed]",
  "reviewRating": {
    "@type": "Rating",
    "bestRating": "[best rating]",
    "worstRating": "[worst rating]",
    "ratingValue": "[rating received]"
  },
  "datePublished": "[date in ISO format e.g. 2012-04-15]",
  "author": "[author name]"
}
</script>
```

**Microdata**

```HTML
<div itemprop="review" itemscope itemtype="http://schema.org/Review">
  <span itemprop="itemreviewed">[the item being reviewed]</span>
  <div itemprop="reviewRating" itemscope itemtype="http://schema.org/Rating">
    <meta itemprop="worstRating" content = "[worst rating]">
    <meta itemprop="bestRating" content="[best rating]">
    <meta itemprop="ratingValue" content="[rating received]">
  </div>
  <span itemprop="datePublished" content="[date in ISO format e.g. 2012-04-15]">[publication date]</span>
  <span itemprop="author">[author name]</span>
</div>
```

### 3.4 The test…

Filling in the blanks, the resulting SERP using the structured data testing tool should resemble something like this:

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/3-4test.jpg" />

### 3.5 Extending this mark-up

By altering this code slightly, combining properties from schema.org/Product we can add a price to the snippet as well:

**JSON-LD**

```javascript
<script type="application/ld+json">
{
  "@context": "http://schema.org",
  "@type": "Review",
  "itemReviewed": "[the item being reviewed]",
  "reviewRating": {
    "@type": "Rating",
    "bestRating": "[best rating]",
    "worstRating": "[worst rating]",
    "ratingValue": "[rating received]"
  },
  "datePublished": "[date in ISO format e.g. 2012-04-15]",
  "author": "[author name]",
  "offers": {
    "@type": "Offer",
    "price": "[product sale price]",
    "priceCurrency": "[currency in 3 letter ISO 4217 format e.g. USD]"
  }
}
</script>
```

**Microdata**

```HTML
<div itemscope itemtype="http://schema.org/Product">
  <span itemprop="name">[product being reviewed]</span>
  <div itemprop="review" itemscope itemtype="http://schema.org/Review">
    <div itemprop="reviewRating" itemscope itemtype="http://schema.org/Rating">
      <meta itemprop="worstRating" content = "[worst possible rating]">
      <meta itemprop="bestRating" content="[best possible rating]">
      <meta itemprop="ratingValue" content="[rating given]">
    </div>
    <span itemprop="author">[author name]</span>
    <span itemprop="datePublished" content="[date in ISO format e.g. 2012-04-15]"> [publication date]</span>
  </div>
  <span itemprop="offers" itemscope itemtype="http://schema.org/Offer">
    <span itemprop="price">[product price]</span>
  </span>
</div>
```

This would create the following snippet:

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/3-5-1test.jpg" />

You can extend this even further to include a price range; just replace the schema.org/Offer section with:

**JSON-LD**

```javascript
<script type="application/ld+json">
{
  "@context": "http://schema.org",
  "@type": "Review",
  "itemReviewed": "[the item being reviewed]",
  "reviewRating": {
    "@type": "Rating",
    "bestRating": "[best rating]",
    "worstRating": "[worst rating]",
    "ratingValue": "[rating received]"
  },
  "datePublished": "[date in ISO format e.g. 2012-04-15]",
  "author": "[author name]",
  "offers": {
    "@type": "AggregateOffer",
    "lowPrice": "[lowest product price]",
    "highPrice": "[highest product price]",
    "priceCurrency": "[currency in 3 letter ISO 4217 format e.g. USD]"
  }
}
</script>
```

**Microdata**

```HTML
<span itemprop="offers" itemscope itemtype="http://schema.org/AggregateOffer">
  <span itemprop="lowPrice">[lowest retail price]</span>
  to <span itemprop="highPrice">[highest retail price]</span>
</span>
```

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/3-5-2test.jpg" />

**Further Reading:** [Individual Reviews](https://developers.google.com/search/docs/data-types/review?visit_id=1-636582744460117386-443891566&hl=en&rd=1#Individual_reviews) – Google Webmaster Help, [Review](http://schema.org/Review) – Schema.org

# Swoop a Grammy by Marking-up Movie Content

### 4.1 Example live snippet

Schema.org review mark-up when combined with the schema.org/Movie itemtype can produce the following type of snippet:

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/4-1example.jpg" />

There is no direct impact to the text displayed alongside the review segment; however an additional line is inserted alongside the Meta description featuring the directors and actors starring in the film.

### 4.2 The core mark-up features at a glance:

**Itemtype** attributes utilised:

| Itemtype      | Description   |
| ------------- | ------------- |
| http://www.schema.org/Movie                | Describes a film.                                         |
| http://www.schema.org/Person               | Describes a person (living, dead or fictional).           |
| http://www.schema.org/AggregateRating      | The average rating based on multiple ratings or reviews.  |

**Itemprop** attributes utilised:

| Itemprop      | Description   | Property of   |
| ------------- | ------------- | ------------- |
| itemprop=“name”             | The name of the item being marked up.            | All |
| itemprop=“description”      | Describe the item being marked up.               | All |
| itemprop=“director”         | The director of the movie, tv series or episode. | [Movie](http://schema.org/Movie) |
| itemprop=”url“              | URL of the item.                                 | All |
| itemprop=“author”	      | The author of this content.                      | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=“bestRating”       | The highest possible rating.                     | [Rating](http://schema.org/Rating) |
| itemprop=“ratingValue”      | The rating for the content.                      | [Rating](http://schema.org/Rating) |
| itemprop=“ratingCount”      | The number of ratings obtained.                  | [AggregateRating](http://schema.org/AggregateRating) |
| itemprop=“actor”            | A cast member of the movie.                      | [Movie](http://schema.org/Movie) |

### 4.3 The mark-up

Exploiting review mark-up for a Movie:

**JSON-LD**

```javascript
<script type="application/ld+json">
{
  "@context": "http://schema.org",
  "@type": "Movie",
  "name": "[name of the movie]",
  "description": "[description of the movie]",
  "director": {
    "@type": "Person",
    "name": "[director's name]"
  },
  "author": {
      "@type": "Person",
      "name": "[script writer]"
  },
  "actor": [
    {
      "@type": "Person",
      "name": "[actor's name]"
    },
    {
      "@type": "Person",
      "name": "[actor's name]"
    },
    {
      "@type": "Person",
      "name": "[actor's name]"
    }
  ],
  "aggregateRating": {
    "@type": "AggregateRating",
    "bestRating": "[best possible rating]",
    "ratingCount": "[total ratings received]",
    "ratingValue": "[rating given]"
  } 
}
</script>
```

**Microdata**

```HTML
<div itemscope itemtype="http://schema.org/Movie">
  <h1 itemprop="name">[name of the movie]</h1>
  <span itemprop="description">[description of the movie]</span>
  <div itemprop="director" itemscope itemtype="http://schema.org/Person">
    <a href="[url]" itemprop="url"><span itemprop="name">[director’s name]</span></a>
  </div>
  <div itemprop="author" itemscope itemtype="http://schema.org/Person">
    <a href="[url]" itemprop="url"><span itemprop="name">[script writer]</span></a>
  </div>
  <div itemprop="actor" itemscope itemtype="http://schema.org/Person">
    <a href="[url]" itemprop="url"><span itemprop="name">[actor’s name]</span></a>,
  </div>
  <div itemprop="actor" itemscope itemtype="http://schema.org/Person">
    <a href="[url]" itemprop="url"><span itemprop="name">[actor’s name]</span></a>,
  </div>
  <div itemprop="aggregateRating" itemscope itemtype="http://schema.org/AggregateRating">
    <span itemprop="ratingValue">[rating given]</span>/
    <span itemprop="bestRating">[best possible rating]</span> stars from
    <span itemprop="ratingCount">[total ratings received]</span> users.
  </div>
</div>
```

### 4.4 The Test…

Filling in the blanks, the resulting snippet using the structured data testing tool should resemble something like this:

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/4-4test.jpg" />

The structured data testing tool does not yet display the additional line of text with references to actors/directors, however if implemented correctly the displayed data extract should contain this information.

**Further Reading:** [Movie Schema.org Creator](https://raventools.com/site-auditor/seo-guide/schema-structured-data) – Raven Tools, [Movie](http://schema.org/Movie) – Schema.org

# Bring Your TV Listing Search Results to Life

### 5.1 Example live snippet

There is also specific mark up for a TV series/season/episode which can also be combined with the review mark-up to produce a similar snippet as ‘Movie’:

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/5-1example.jpg" />

The result is the same as Schema.org/Movie with an additional line of text included referencing the director(s) and actor(s), however a further line has been inserted for episodes and episodes cast.

### 5.2 The core mark-up features at a glance:


**Itemtype** attributes utilised:

| Itemtype      | Description   |
| ------------- | ------------- |
| http://www.schema.org/TVSeries               | Describes a television series.                            |
| http://www.schema.org/TVSeason               | Describes a single TV season.                             |
| http://www.schema.org/TVEpisode              | The episode of a TV series or season.                     |
| http://www.schema.org/Person                 | Describes a person (living, dead or fictional).           |
| http://www.schema.org/AggregateRating        | The average rating based on multiple ratings or reviews.  |

**Itemprop** attributes utilised:

| Itemprop      | Description   | Property of   |
| ------------- | ------------- | ------------- |
| itemprop=“name”             | The name of the item being marked up.              | All |
| itemprop=“description”      | Describe the item being marked up.                 | All |
| itemprop=“director”         | The director of the movie, tv series or episode.   | [TVSeries](http://schema.org/TVSeries), [TVSeason](http://schema.org/TVSeason), [TVEpisode](http://schema.org/Episode) |
| itemprop=“actor”            | A cast member of the TV series, season or episode. | [TVSeries](http://schema.org/TVSeries), [TVSeason](http://schema.org/TVSeason), [TVEpisode](http://schema.org/Episode) |
| itemprop=“author”	      | The author of this content.                        | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=“numberofEpisodes” | The number of episodes in the series or season.    | [TVSeries](http://schema.org/TVSeries), [TVSeason](http://schema.org/TVSeason) |
| itemprop=“datePublished”    | Date of first broadcast/publication.               | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=“episode”          | An episode of a TV series of season.               | [TVSeries](http://schema.org/TVSeries), [TVSeason](http://schema.org/TVSeason) |
| itemprop=“numberofEpisodes” | The episode number.                                | [TVEpisode](http://schema.org/Episode) |
| itemprop=“ratingValue”      | The rating for the content.                        | [Rating](http://schema.org/Rating) |
| itemprop=“ratingCount”      | The number of ratings obtained.                    | [AggregateRating](http://schema.org/AggregateRating) |

### 5.3 The mark-up

Utilising review mark-up and combining TV series, season and episode schema:

**JSON-LD**

```javascript
<script type="application/ld+json">
{
  "@context": "http://schema.org",
  "@type": "TVSeries",
  "name": "[name of show]",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "[aggregate rating given]",
    "ratingCount": "[number of reviews]",
    "bestRating": "[best possible rating]"
  },
 "description": "[description of the TV show]",
 "author": {
    "@type": "Person",
    "name": "[writers name]"
 },
 "actor": [
    {
      "@type": "Person",
      "name": "[actors name]"
    },
    {
      "@type": "Person",
      "name": "[actors name]"
    }
  ],
  "season": [
    {
      "@type": "TVSeason",
      "name": "[season]",
      "numberOfEpisodes": "[no. of episodes]",
      "datePublished": "[date in ISO format e.g. 2012-04-15]"
    },
    {
      "@type": "TVSeason",
      "name": "[season]",
      "numberOfEpisodes": "[no. of episodes]",
      "datePublished": "[date in ISO format e.g. 2012-04-15]",
      "episode": {
        "@type": "TVEpisode",
        "episodeNumber": "[episode number]",
        "name": "[name of episode]"
      }
    }
  ]
}
</script>
```

**Microdata**

```HTML
<div itemscope itemtype="http://schema.org/TVSeries">
  <h1 itemprop="name">[name of TV show]</h1>
  <div itemprop="aggregateRating" itemscope itemtype="http://schema.org/AggregateRating">
    <span itemprop="ratingValue">[rating given]</span>/
    <span itemprop="bestRating">[best possible rating]</span> stars from
    <span itemprop="ratingCount">[total number of reviews]</span> users.
  </div>
  <span itemprop="description">[description of the TV show]</span>
  <div itemprop="author" itemscope itemtype="http://schema.org/Person">
    <span itemprop="name">[actor’s name]</span>
  </div>
  <div itemprop="actor" itemscope itemtype="http://schema.org/Person">
    <span itemprop="name">[actor’s name]</span>
  </div>
  <div itemprop="season" itemscope itemtype="http://schema.org/TVSeason">
    <span itemprop="name">[season 1, 2 or 3...?]</span> -
    <meta itemprop="numberofEpisodes" content="[number of episodes in this season]"/>
    <meta itemprop="datePublished" content="[date in ISO format e.g. 2012-04-15]">[broadcast date]
  </div>
  <div itemprop="season" itemscope itemtype="http://schema.org/TVSeason">
    <span itemprop="name">[season 1, 2 or 3...?]</span> -
    <meta itemprop="numberofEpisodes" content="[number of episodes in this season]"/>
    <meta itemprop="datePublished" content="[date in ISO format e.g. 2012-04-15]"> [broadcast date]
    <div itemprop="episode" itemscope itemtype="http://schema.org/TVEpisode">
      <span itemprop="name">[episode name]</span> -
      <meta itemprop="episodeNumber" content="[episode number]"/>
    </div>
  </div>
</div>
```

### 5.4 The Test…

Filling in the blanks, the resulting snippet using the structured data testing tool should resemble something like this:

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/5-4test.jpg" />

The structured data testing tool does not yet display the additional line of text with references to episodes/episodes cast, however if implemented correctly the displayed data extract should contain this information.

**Further Reading:** [TVSeries](http://schema.org/TVSeries), [TVSeason](http://schema.org/TVSeason) & [TVEpisode](http://schema.org/TVEpisode) – Schema.org

# Show Business Credibility in Search Results

### 6.1 Example snippet

Local Business Schema.org alone does not yet result in a specific type of snippet, although can be combined with standard review mark-up to produce the below snippet:

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/6-1example.jpg" />

Local Business schema.org mark-up can also act as authentication for a business address if it matches the Google Business Listing, in doing so improve local SEO.

### 6.2 The core mark-up features at a glance:

**Itemtype** attributes utilised:

| Itemtype      | Description   |
| ------------- | ------------- |
| http://www.schema.org/LocalBusiness              | Describes a physical business or branch of an organization. |
| http://www.schema.org/PostalAddress              | The location of the event or organization.                  |
| http://www.schema.org/AggregateRating            | The average rating based on multiple ratings or reviews.    |

**Itemprop** attributes utilised:

| Itemprop      | Description   | Property of   |
| ------------- | ------------- | ------------- |
| itemprop=“name”             | The name of the item being marked up.              | All |
| itemprop=“streetAddress”    | The street address.                                | [PostalAddress](http://schema.org/PostalAddress) |
| itemprop=“addressLocality”  | The locality.                                      | [PostalAddress](http://schema.org/PostalAddress) |
| itemprop=“addressRegion”    | The region.                                        | [PostalAddress](http://schema.org/PostalAddress) |
| itemprop=“postalCode”	      | The postal code.                                   | [PostalAddress](http://schema.org/PostalAddress) |
| itemprop=“telephone”        | The telephone number.                              | [ContactPoint](http://schema.org/ContactPoint) |
| itemprop=“ratingValue”      | The rating for the content.                        | [Rating](http://schema.org/Rating) |
| temprop=“bestRating”        | The best possible rating.                          | [Rating](http://schema.org/Rating) |
| itemprop=“ratingCount”      | The number of ratings obtained.                    | [AggregateRating](http://schema.org/AggregateRating) |

### 6.3 The mark-up
Utilising review mark-up and combining Local Business schema:

**JSON-LD**

```javascript
<script type="application/ld+json">
{
  "@context": "http://schema.org",
  "@type": "LocalBusiness",
  "name": "[business name]",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[street name]",
    "addressLocality": "[locality]",
    "addressRegion": "[region]",
    "postalCode": "[postal code]"
  },
  "telephone": "[telephone number]",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "[aggregate rating given]",
    "bestRating": "[highest rating]",
    "reviewCount": "[total number of reviews]"
  }
}
</script>
```

**Microdata**

```HTML
<div itemscope itemtype="http://schema.org/LocalBusiness">
  <span itemprop="name">[business name]</span>
  <div itemprop="address" itemscope itemtype="http://schema.org/PostalAddress">
    <span itemprop="streetAddress">[street name]</span>
    <span itemprop="addressLocality">[locality]</span>,
    <span itemprop="addressRegion">[region]</span>
    <span itemprop="postalCode">[postal code]</span>
  </div>
  <span itemprop="telephone">[telephone number]</span>
  <div itemprop="aggregateRating" itemscope itemtype="http://schema.org/AggregateRating">
    <span itemprop="ratingValue">[rating given]</span>/
    <span itemprop="bestRating">[highest rating]</span> stars from
    <span itemprop="reviewCount">[total number of reviews]</span> users.
  </div>
</div>
```

**Further Reading:** [LocalBusiness](http://schema.org/LocalBusiness) & [PostalAddress](http://schema.org/PostalAddress) – Schema.org, [Business Schema Tool](http://www.microdatagenerator.com/local-business-schema/) – microData generator

# Use Recipe Mark-up to Generate Appetising Rich Snippets

### 7.1 Example live snippet
Another more developed Schema.org type is Recipe, which allows for the development of rich snippets like the below:

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/7-1example.jpg" />

There are a lot more elements however taken from the Recipe schema which determine visibility in Google’s recipe search – [http://www.google.com/landing/recipes/](http://www.google.com/landing/recipes/)

### 7.2 The core mark-up features at a glance:

**Itemtype** attributes utilised:

| Itemtype      | Description   |
| ------------- | ------------- |
| http://www.schema.org/Recipe	                   | Describes a recipe.                                         |
| http://www.schema.org/NutritionInformation       | Describes the nutrition information of a recipe.            |
| http://www.schema.org/AggregateRating            | The average rating based on multiple ratings or reviews.    |

**Itemprop** attributes utilised:

| Itemprop      | Description   | Property of   |
| ------------- | ------------- | ------------- |
| itemprop=“name”               | The name of the item being marked up.              | All |
| itemprop=“image”              | URL of an image of the item.                       | All |
| itemprop=“author”	        | The author of this content.                        | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=“description”        | Describe the item being marked up.                 | All |
| itemprop=“ingredients”        | An ingredient used in the recipe.                  | [Recipe](http://schema.org/Recipe) |
| itemprop=“recipeCategory”     | The category of the recipe e.g. starter.           | [Recipe](http://schema.org/Recipe) |
| itemprop=“recipeCuisine”      | The cuisine of the recipe e.g. Chinese             | [Recipe](http://schema.org/Recipe) |
| itemprop=“recipeYield”        | The quantity produced by the recipe.	           | [Recipe](http://schema.org/Recipe) |
| itemprop=“cookTime”           | The time it takes to cook the dish in ISO duration format. | [Recipe](http://schema.org/Recipe) |
| itemprop=“prepTime”           | The length of time it takes to prepare the recipe. | [AggregateRating](http://schema.org/AggregateRating) |
| itemprop=“calories”           | The number of calories.                            | [NutritionInfomation](http://schema.org/NutritionInfomation) |
| itemprop=“fatContent”         | The number of grams of fat.                        | [NutritionInfomation](http://schema.org/NutritionInfomation) |
| itemprop=“recipeInstructions” | The steps to make the dish.                        | [Recipe](http://schema.org/Recipe) |
| itemprop=“ratingValue”        | The rating for the content.                        | [Rating](http://schema.org/Rating) |
| itemprop=“bestRating”         | The best possible rating.                          | [Rating](http://schema.org/Rating) |
| itemprop=“reviewCount”        | The number of reviews obtained.                    | [AggregateRating](http://schema.org/AggregateRating) |

### 7.3 The mark-up

Utilising review mark-up and combining the recipe schema:

**JSON-LD**

```javascript
<script type="application/ld+json">
{
  "@context": "http://schema.org",
  "@type": "Recipe",
  "author": "[author name]",
  "datePublished": "[date in ISO format e.g. 2012-04-15]",
  "name": "[recipe name]",
  "image" : "[recipe image url]",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "[aggregate rating given]",
    "bestRating": "[highest rating]",
    "reviewCount": "[total number of reviews]"
  },
  "description" : "[a description of the recipe]",
  "ingredients" : [
    "[ingredient 1]",
    "[ingredient 2]",
    "[ingredient 3]",
    "[ingredient 4]"
   ],
  "recipeCategory": "[url to recipe category]",
  "recipeCuisine": "[url to recipe cuisine category]",
  "recipeYield": "[recipe yield]",
  "cookTime": "[ISO duration format e.g. PT2H45M]",
  "prepTime": "[ISO duration format e.g. PT2H45M]",
  "nutrition": {
    "@type": "NutritionInformation",
    "calories": "[total calories]",
    "fatContent": "[grams of fat]"
  },
  "recipeInstructions" : [
    "[instruction 1]",
    "[instruction 2]",
    "[instruction 3]"
  ]
}
</script>
```

**Microdata**

```HTML
<div itemscope itemtype="http://schema.org/Recipe">
  <span itemprop="author">[author name]</span>
  <span itemprop="datePublished" content="[date in ISO format e.g. 2012-04-15]">[publication date]</span>
  <span itemprop="name">[recipe name]</span>
  <img itemprop="image" src="[recipe image url]" />
  <div itemprop="aggregateRating" itemscope itemtype="http://schema.org/AggregateRating">
    <span itemprop="ratingValue">[rating given]</span>/
    <span itemprop="bestRating">[highest possible rating]</span> stars from
    <span itemprop="reviewCount">[total number of reviews]</span> users.
  </div>
  <span itemprop="description">[a description of the recipe]</span>
  <ul>
    <li itemprop="ingredients">[ingredient 1]</li>
    <li itemprop="ingredients">[ingredient 2]</li>
    <li itemprop="ingredients">[ingredient 3]</li>
    ...
  </ul>
  <span itemprop="recipeCategory"><a href="[url to recipe category]">[recipe category]</a></span>
  <span itemprop="recipeCuisine"><a href="[url to recipe cuisine category]">[recipe cuisine]</a></span>
  <span itemprop="recipeYield">[recipe yield]</span>
  <span itemprop="cookTime" content="[ISO duration format e.g. PT2H45M]">[cooking time]</span>
  <span itemprop="prepTime" content="[ISO duration format e.g. PT45M]">[prep time]</span>
  <div itemprop="nutrition" itemscope itemtype="http://schema.org/NutritionInformation">
    <span itemprop="calories">[total calories]</span>
    <span itemprop="fatContent">[grams of fat]</span>
  </div>
  <ol itemprop="recipeInstructions">
    <li>1. [Instruction 1]...</li>
  </ol>
</div>
```

### 7.4 The test…

Filling in the blanks, the resulting snippet using the structured data testing tool should resemble something like this:

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/7-4test.jpg" />

**Further Reading:** [Recipe](http://schema.org/Recipe) & [NutritionInformation](http://schema.org/NutritionInformation) – Schema.org, [Recipe Schema Tool](http://www.microdatagenerator.com/recipe-schema/) – microDATA generator, [Rich Snippet Recipes](http://support.google.com/webmasters/bin/answer.py?hl=en&answer=173379) – Google Webmaster Help

# Add Authenticity & Trust to Mobile App Listings

### 8.1 Example snippet

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/8-1example.jpg" />

### 8.2 The core mark-up features at a glance:

| Itemtype      | Description   |
| ------------- | ------------- |
| http://www.schema.org/MobileApplication    | Describes a Mobile application.                           |
| http://www.schema.org/Organization         | Describes an organization.                                |

**Itemprop** attributes utilised:

| Itemprop      | Description   | Property of   |
| ------------- | ------------- | ------------- |
| itemprop=“name”             | The name of the item being marked up.            | All |
| itemprop=“image”            | URL of an image of the item.                     | All |
| itemprop=“description”      | Describe the item being marked up.               | All |
| itemprop=”url“              | URL of the item.                                 | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=“author”	      | The author of this content.                      | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=”datePublished“    | Date of first broadcast/publication.             | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=“operatingSystems” | The operating systems supported.                 | [SoftwareApplication](http://schema.org/SoftwareApplication) |
| itemprop=“fileSize”         | Size of the application.                         | [SoftwareApplication](http://schema.org/SoftwareApplication) |
| itemprop=“interactionCount” | A count of a specific user interaction with this item. | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=“contentRating”    | Official rating for a piece of content.	         | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=“bestRating”       | The highest possible rating.                     | [Rating](http://schema.org/Rating) |
| itemprop=“ratingValue”      | The rating for the content.                      | [Rating](http://schema.org/Rating) |
| itemprop=“ratingCount”      | The number of ratings obtained.                  | [AggregateRating](http://schema.org/AggregateRating) |

### 8.3 The mark-up

Applying Mobile Application mark-up:

**JSON-LD**

```javascript
<script type="application/ld+json">
{
  "@context": "http://schema.org",
    "@type": "MobileApplication",
    "image": "[image url for application icon]",
    "name": "[name of the mobile application]",
    "author": {
      "@type": "Organization",
      "url": "[author url]",
      "name": "[developer name]"
    },
  "aggregateRating": {
    "@type" : "AggregateRating",
    "ratingValue" : "[rating given]",
    "bestRating" : "[highest possible rating]",
    "ratingCount" : "[total number of ratings]"
  },
  "datePublished": "[date in ISO format e.g. 2012-04-15]",
  "operatingSystem": "[supported operating system]",
  "fileSize" : "[file size e.g. 14mb]",
  "interactionCount" : "[number of user downloads]",
  "contentRating" : "[content rating e.g. Low Maturity]",
  "description" : "[description of the mobile application]",
  "applicationCategory" : "[application category e.g. http://schema.org/GameApplication]"
}
</script>
```

**Microdata**

```HTML
<div itemscope itemtype="http://schema.org/MobileApplication">
  <img itemprop="image" src="[image URL for application icon]" />
  <span itemprop="name">[name of the mobile application]</span> -
  <div itemprop="author" itemscope itemtype="http://schema.org/Organization">
    <a itemprop="url" href="[author url]"><span itemprop="name">[developer name]</span></a>
  </div>
  <div itemprop="aggregateRating" itemscope itemtype="http://schema.org/AggregateRating">
    <span itemprop="ratingValue">[rating given]</span>/
    <span itemprop="bestRating">[highest possible rating]</span> stars from
    <span itemprop="ratingCount">[total number of ratings]</span> users.
  </div>
  <time itemprop="datePublished" datetime="[date in ISO format e.g. 2012-04-15]">[publication date]</time>
  <span itemprop="operatingSystems">[supported operating system]</span>
  <meta itemprop="fileSize" content="[file size e.g. 14MB]"/>
  <meta itemprop="interactionCount" content="[number of user downloads] UserDownloads">
  <span itemprop="contentRating">[content rating e.g. Low Maturity]</span>
  <span itemprop="description">[description of the mobile application]</span>
</div>
```

### 8.4 The test…

Filling in the blanks, the resulting snippet using the structured data testing tool should resemble something like this:

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/8-4test.jpg" />

### 8.5 Extending this mark-up

By combining some properties from schema.org/Offers we can add a price to the snippet. Just add the below mark up:

**JSON-LD**

```javascript
"Offers": {
    "@type" : "Offer",
    "price" : "[app price]"
}
```

**Microdata**

```HTML
<div itemprop="offers" itemscope itemtype="http://schema.org/Offer">
  <span itemprop="price">[price]</span>
</div>
```

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/8-5test.jpg" />

**Further Reading:** [MobileApplication](http://schema.org/MobileApplication) – Schema.org, [Rich Snippets for Apps: a New Way to be Seen in SERPs](http://searchenginewatch.com/article/2123992/Rich-Snippets-for-Apps-A-New-Way-to-be-Seen-in-SERPs) – SEWatch generator, [Rich Snippets: Software Applications](http://support.google.com/webmasters/bin/answer.py?hl=en&answer=1645432) – Google Webmaster Help

# Promote Software Applications in Search Results

### 9.1 Example live snippet

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/9-1example.jpg" />

Software Application mark-up is very similar to Mobile; however there are some additional features that can be included to develop this snippet.

### 9.2 The core mark-up features at a glance:

**Itemtype** attributes utilised:

| Itemtype      | Description   |
| ------------- | ------------- |
| http://www.schema.org/SoftwareApplication  | Describes a Mobile application.                           |
| http://www.schema.org/Organization         | Describes an organization.                                |
| http://www.schema.org/AggregateRating      | The average rating based on multiple ratings or reviews.  |
| http://www.schema.org/Offer                | Describes a products offer details.                       |

**Itemprop** attributes utilised:

| Itemprop      | Description   | Property of   |
| ------------- | ------------- | ------------- |
| itemprop=“name”             | The name of the item being marked up.            | All |
| itemprop=“image”            | URL of an image of the item.                     | All |
| itemprop=“description”      | Describe the item being marked up.               | All |
| itemprop=”url“              | URL of the item.                                 | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=“author”	      | The author of this content.                      | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=”datePublished“    | Date of first broadcast/publication.             | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=“operatingSystems” | The operating systems supported.                 | [SoftwareApplication](http://schema.org/SoftwareApplication) |
| itemprop=“fileSize”         | Size of the application.                         | [SoftwareApplication](http://schema.org/SoftwareApplication) |
| itemprop=“interactionCount” | A count of a specific user interaction with this item. | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=“contentRating”    | Official rating for a piece of content.	         | [CreativeWork](http://schema.org/CreativeWork) |
| itemprop=“bestRating”       | The highest possible rating.                     | [Rating](http://schema.org/Rating) |
| itemprop=“ratingValue”      | The rating for the content.                      | [Rating](http://schema.org/Rating) |
| itemprop=“ratingCount”      | The number of ratings obtained.                  | [AggregateRating](http://schema.org/AggregateRating) |
| itemprop=“price”            | The price of the item.                           | [Offer](http://schema.org/Offer) |

### 9.3 The mark-up

Utilising Software Application mark-up:

**JSON-LD**

```javascript
<script type="application/ld+json">
{
  "@context": "http://schema.org",
  "@type": "SoftwareApplication",
  "image": "[software application icon image url]",
  "name": "[name of the software application]",
  "author": {
    "@type": "Organization",
    "url": "[author url]",
    "name": "[developer name]"
  },
  "aggregateRating": {
    "@type" : "AggregateRating",
    "ratingValue" : "[rating given]",
    "bestRating" : "[highest possible rating]",
    "ratingCount" : "[total number of ratings]"
  },
  "datePublished": "[date in ISO format e.g. 2012-04-15]",
  "fileSize" : "[file size e.g. 14mb]",
  "interactionCount" : "[number of user downloads]",
  "contentRating" : "[content rating e.g. Low Maturity]",
  "description" : "[description of the software application]",
  "downloadURL" : "[download url]"
  "operatingSystem" : [
    "[operating system 1]",
    "[operating system 2]"
  ],
  "applicationCategory" : "[application category e.g. http://schema.org/GameApplication]",
  "Offers": {
    "@type" : "Offer",
    "price" : "[app price]"
 }
}
</script>
```

**Microdata**

```HTML
<div itemscope itemtype="http://schema.org/SoftwareApplication">
  <img itemprop="image" src="[software application icon image url]" />
  <span itemprop="name">[name of application]</span> -
  <div itemprop="author" itemscope itemtype="http://schema.org/Organization">
    <a itemprop="url" href="[author url]"><span itemprop="name">[developer name]</span></a>
  </div>
  <div itemprop="aggregateRating" itemscope itemtype="http://schema.org/AggregateRating">
    <span itemprop="ratingValue">[rating given]</span>/
    <span itemprop="bestRating">[highest possible rating]</span> stars from
    <span itemprop="ratingCount">[total number of ratings]</span> users.
  </div>
  <div itemprop="offers" itemscope itemtype="http://schema.org/Offer">
    <span itemprop="price">[price]</span>
  </div>
  <span itemprop="description">[description of application]</span>
  <a itemprop="downloadURL" href="[download url]">Download</a>
  <time itemprop="datePublished" datetime="[date in ISO format e.g. 2012-04-15]">[publication date]</time>
  <span itemprop="operatingSystems">[supported operating systems]</span>
  <span itemprop="applicationCategory">[category]</span>
  <meta itemprop="fileSize" content="[file size e.g. 14MB]"/>
  <meta itemprop="interactionCount" content="[number of downloads] UserDownloads">
</div>
```

### 9.4 The Test…

Filling in the blanks, the resulting snippet using the structured data testing tool should resemble something like this:

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/9-4test.jpg" />

**Further Reading:** [SoftwareApplication](http://schema.org/SoftwareApplication) – Schema.org, [Rich Snippets: Software applications](http://support.google.com/webmasters/bin/answer.py?hl=en&answer=1645432) – Google Webmaster Help

# Tell Us About Yourself with Person Mark-up

### 10.1 Example snippet

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/10-1example.jpg" />

### 10.2 The core mark-up features at a glance:

**Itemtype** attributes utilised:

| Itemtype      | Description   |
| ------------- | ------------- |
| http://www.schema.org/Person                     | Describes a person (living, dead or fictional).             |
| http://www.schema.org/PostalAddress              | The location of the event or organization.                  |

**Itemprop** attributes utilised:

| Itemprop      | Description   | Property of   |
| ------------- | ------------- | ------------- |
| itemprop=“name”             | The name of the item being marked up.              | All |
| itemprop=“image”            | URL of an image of the person.                     | All |
| itemprop=“jobTitle”         | The job title of the person.                       | [Person](http://schema.org/Person) |
| itemprop=“address”          | Physical address of the person.                    | [PostalAddress](http://schema.org/PostalAddress) |
| itemprop=“addressLocality”  | The address locality of the person.                | [PostalAddress](http://schema.org/PostalAddress) |
| itemprop=“addressRegion”    | The region in which the person resides.            | [PostalAddress](http://schema.org/PostalAddress) |
| itemprop=“postalCode”	      | The postal code.                                   | [PostalAddress](http://schema.org/PostalAddress) |
| itemprop=“telephone”        | The person’s telephone number.                     | [Person](http://schema.org/Person) |
| itemprop=“email”            | The person’s email address.                        | [Person](http://schema.org/Person) |

### 10.3 The mark-up

Utilising Person mark-up:

**JSON-LD**

```javascript
<script type="application/ld+json">
{
  "@context": "http://schema.org",
  "@type" : "Person",
  "name" : "[person's name]",
  "image" : "[image url of person]",
  "jobTitle": "[job tile]",
  "address" : {
    "@type" : "PostalAddress",
    "addressLocality" : "[Locality]",
    "addressRegion" : "[region]",
    "postalCode" : "[postal code]"
  },
  "telephone" : "[telephone number]",
  "email" : "[email address]"
}
</script>
```

**Microdata**

```HTML
<div itemscope itemtype="http://schema.org/Person">
  <span itemprop="name">[person’s name]</span>
  <img src="[image url of person]" itemprop="image" />
  <span itemprop="jobTitle">[job title]</span>
  <div itemprop="address" itemscope itemtype="http://schema.org/PostalAddress">
    <span itemprop="addressLocality">[locality]</span>,
    <span itemprop="addressRegion">[region]</span>
    <span itemprop="postalCode">[postal code]</span>
  </div>
  <span itemprop="telephone">[telephone number]</span>
  <a href="mailto:[email address]" itemprop="email">jane-doe@xyz.edu</a>
</div>
```

**Further Reading:** [Person](http://schema.org/Person) – Schema.org, [Rich Snippets: People](http://support.google.com/webmasters/bin/answer.py?hl=en&answer=146646) – Google Webmaster Help

# Sell Tickets for Multiple Events with a Single Search Listing

### 11.1 Example snippet

<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/11-1example.jpg" />

Live examples of Schema.org/Event are very scarce at the moment, with the majority of sites opting for Microdata, Microformats or RDFa equivalent mark-up. Up to 3 entries of Event mark-up can be seen within the rich snippet.

### 11.2 The core mark-up features at a glance:

**Itemtype** attributes utilised:

| Itemtype      | Description   |
| ------------- | ------------- |
|http://www.schema.org/Event | Describes an upcoming event. |

**Itemprop** attributes utilised:

| Itemprop      | Description   | Property of   |
| ------------- | ------------- | ------------- |
| itemprop=“name”             | The name of the item being marked up.              | All |
| itemprop=“url”              | URL of the item.                                   | All |
| itemprop=“location”         | The location of the event.	                   | [Event](http://schema.org/Event) |
| itemprop=“startDate”        | The start date and time of the event.              | [Event](http://schema.org/Event) |

### 11.3 The mark-up

Utilising Event mark-up:

**JSON-LD**

```javascript
REPEAT FOR EACH EVENT:
<script type="application/ld+json">
{
  "@context": "http://schema.org",
  "@type" : "Event",
  "name" : "[event name]",
  "url" : "[event url]",
  "location": {
    "@type" : "Place",
    "name" : "[location name]",
    "address" : "[event location]"
    },
  "startDate": "[date in ISO format e.g. 2013-03-16]"
  }
</script>
```

**Microdata**

```HTML
<div itemprop="event" itemscope itemtype="http://schema.org/Event">
  <a href="[event url]" itemprop="url">
    <span itemprop="name">[event name]</span>
  </a>
  <span itemprop="location">[event location]</span>
  <meta itemprop="startDate" content="[date in ISO format e.g. 2013-03-16]">
</div>
<div itemprop="event" itemscope itemtype="http://schema.org/Event">
  <a href="[event url]" itemprop="url">
    <span itemprop="name">[event name]</span>
  </a>
  <span itemprop="location">[event location]</span>
  <meta itemprop="startDate" content="[date in ISO format e.g. 2013-03-16]">
</div>
```

**Further Reading:** [Event](http://schema.org/Event) – Schema.org, [Rich Snippets: Events](http://support.google.com/webmasters/bin/answer.py?hl=en&answer=164506&topic=1088474&ctx=topic) – Google Webmaster Help

# To be continued...
