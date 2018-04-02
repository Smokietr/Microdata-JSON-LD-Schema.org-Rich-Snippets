# Microdata-JSON-LD-Schema.org-Rich-Snippets
This guide has been created to provide a quick and easy way of generating different types of rich snippets for your website, using a combination of Schema.org and either Microdata or the recently endorsed JSON-LD.

I must point out that before you proceed with integrating any form of mark-up, you should be aware of the guidelines provided by Google, and Bing. Any attempt to mark-up content that is invisible to users, or content that is irrelevant/misleading just to generate the rich snippet may result in action being taken against your website.

## What is Microdata?

Microdata (like RDFa and Microformats) is a form of semantic mark-up designed to describe elements on a web page e.g. review, person, event etc. This mark-up can be combined with typical HTML properties to dedlfine each item type through the use of associated attributes. For example, ‘Person’ has the properties name, url and title – attributes can be applied to HTML tags to describe each property:

```
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
<img src="https://36bvmt283fg61unuud3h7qua-wpengine.netdna-ssl.com/wp-content/uploads/2013/02/sg-ebay.png">
- This has the potential to enhance CTR from the search results from anywhere between 10-25%.
- Search engines and organisations are using this mark-up to develop new tools, for example Google Recipe Search, which may open up other marketing channels if not now, in the near future.
- Provide greater information to search engines to improve their understanding of the content on your website.

# To be continued
