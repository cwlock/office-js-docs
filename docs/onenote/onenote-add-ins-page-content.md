# Work with OneNote page content 

In the OneNote add-ins JavaScript API, page content is represented by the following object model.

  ![OneNote page object model diagram](../../images/OneNoteOM-page.png)

- A Page object contains a collection of PageContent objects.
- A PageContent object contains a content type of Outline, Image, or Other.
- An Outline object contains a collection of Paragraph objects.
- A Paragraph object contains a content type of RichText, Image, Table, or Other.

To create an empty OneNote page, use one of the following methods:

- [Section.addPage](../../reference/onenote/section.md#addpagetitle-string)
- [Page.insertPageAsSibling](../../reference/onenote/page.md#insertpageassiblinglocation-string-title-string)

Then use methods in the following objects to work with the page content, such as Page.addOutline and Outline.appendHtml. 

- [Page](../../reference/onenote/page.md)
- [Outline](../../reference/onenote/outline.md)
- [Paragraph](../../reference/onenote/paragraph.md)

The content and structure of a OneNote page are represented by HTML. Only a subset of HTML is supported for creating or updating page content, as described below.

## Supported HTML

The OneNote add-in JavaScript API supports the following HTML for creating and updating page content:

- `<html>`, `<body>`, `<div>`, `<span>`, `<br/>` 
- `<p>`
- `<img>`
- `<a>`
- `<ul>`, `<ol>`, `<li>` 
- `<table>`, `<tr>`, `<td>`
- `<h1>` ... `<h6>`
- `<b>`, `<em>`, `<strong>`, `<i>`, `<u>`, `<del>`, `<sup>`, `<sub>`, `<cite>`

## Accessing page contents

You are only able to access *Page Content* via `Page#load` for the currently
active page. To change the active  page, invoke `navigateToPage($page)`.

Metadata such as title can still be queried for any page.

## Additional resources

- [OneNote JavaScript API programming overview](onenote-add-ins-programming-overview.md)
- [OneNote JavaScript API reference](../../reference/onenote/onenote-add-ins-javascript-reference.md)
- [Rubric Grader sample](https://github.com/OfficeDev/OneNote-Add-in-Rubric-Grader)
- [Office Add-ins platform overview](https://dev.office.com/docs/add-ins/overview/office-add-ins)
