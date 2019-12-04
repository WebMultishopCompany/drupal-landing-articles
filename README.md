# Drupal - Landing articles (feature)

Provides Landing article content type and related configuration. An article that is often a landing page for new visitors, such as a product or service promotional article.

## What is in the box

### Content type "Landing article"

Grouped fields:

* Heading
* Teaser/cover
	* Image (`field_lart_image`) Entity reference
	* Description (`field_lart_description`) Text (formatted)
	* About (`field_lart_about`) Text (formatted, long)
* Main article content (Body)
	* Content (`field_lart_text`) Text (formatted, long)
* Additional chapters (sections)
	* Sections (`field_lart_sections`) Entity reference revisions
* Gallery
	* Media gallery (`field_lart_media_gallery`) Entity reference
* Related content
	* Heading (`field_lart_rel_content_heading`) Text (plain)
	* Style (`field_lart_rel_content_style`) List (text)
	* Related content (`field_lart_related_content`) Entity reference revisions
* Advanced publishing
	* Scheduled publishing (`field_lart_published`) Smart date range
	* Publish as dynamic content (`field_lart_topics`) Entity reference
* Additional information
	* Sticker/flag (`field_lart_flag`) Text (formatted)
	* Keywords (`field_lart_keywords`) Entity reference
* Commercial attributes
	* Availability (`field_lart_availability`) Smart date range
	* Price (current) (`field_lart_price`) Number (decimal)
	* Maximum price (`field_lart_price_max`) Number (decimal)
	* Price type (`field_lart_price_type`) Text (plain)
	* Special offer (`field_lart_special_offer`) Boolean
	* Old price (`field_lart_price_old`) Number (decimal)

### Taxonomy dictionary "Topics"

Special dictionary that contains project developer pre-defined "Topics" that are used to dynamically display landing articles depending on given topic.

For example, with topics like:

* Company
* News
* Press release
* Recreation

And pages like:

* in `/news` you could create view, that displays all news and provide filter for users to filter all articles by topic
* in `/about-us/news` you could create view, that displays articles only linked to "Company" and "Press release" topics
* in `/recreation` you could create view, that displays articles only linked to "Recreation" topic

This is meant to enable creation of articles that are related to multiple categories.

### Taxonomy dictionary "Keywords"

Simply for keyword storage to enhance search of content (landing articles and media).

### Image styles

* Landing article big cover (933×700)
* Landing article medium cover (740×555)
* Landing article narrow cover (487×365)
* Landing article small cover (560×420)
* Landing article wide cover (1140×641)
* Media gallery image in full HD (1920×1080)
* Media gallery image thumbnail (480×360)

### Media type "Image"

Fields:

* Image (`field_media_image`) Image
* Keyword (`field_keyword`) Entity reference

Display modes:

* Landing article big cover
* Landing article medium cover
* Landing article narrow cover
* Landing article small cover
* Landing article wide cover
* Media gallery image (image displayed as thumbnail and opened in full using "colorbox" plugin)

That display images styled accordingly.

### Paragraph type "Related content"

Fields:

* "Read more" button label (`field_lart_read_more_label`) Text (plain)
* "Read more" button style (`field_lart_read_more_style`) List (text)
* Show content (`field_lart_teaser_show`) Boolean
* Target (`field_lart_related_node`) Entity reference
* Teaser content override (`field_lart_teaser_override`) Text (formatted, long)

Display modes:

* Related content grid

### Paragraph type "Section"

Fields:

* Section heading (`field_lart_section_heading`) Text (plain)
* Section text (`field_lart_section_text`) Text (formatted, long)

Display modes:

* Sections grid

### Modified view "Media library"

Adds exposed filter "Keyword" to all displays.