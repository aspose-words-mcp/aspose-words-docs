---
title: Convert a Multi-page Document to an Image in C++
second_title: Aspose.Words for C++
articleTitle: Convert a Multi-page Document to an Image
linktitle: Convert a Multi-page Document to an Image
type: docs
description: "Export multi-page documents to raster images (JPG, PNG, GIF, BMP, TIFF, WebP) using C++."
weight: 45
ai_search_scope: words_cpp
ai_search_endpoint: "https://docsearch.api.aspose.cloud/ask"
ai_search_fast_endpoint: "https://docsearch.api.aspose.cloud/search"
url: /cpp/convert-a-multi-page-document-to-an-image/
timestamp: 2025-07-16-11-12-25
---

{{% alert color="grey" %}}

## Purpose Summary

This page explains how to convert multi-page documents into multi-frame images, including configuration of image size, resolution, and page range.

{{% /alert %}}

Aspose.Words for C++ allows users to export multi-page documents to raster images. This can be useful for generating previews, archives, or visual representations of documents for non-editable use.

## What Formats Support Multi-page Export?

Aspose.Words supports multi-page export to the following raster image formats:

* Jpeg
* Gif
* Png
* Bmp
* Tiff
* WebP

## How to Export a Multi-page Document to an Image

The feature of exporting a multi-page document to an image is implemented using the [MultiPageLayout](https://reference.aspose.com/words/cpp/aspose.words.saving/multipagelayout/) class – you can specify how the pages should be organized when saving to an image:

* [SinglePage](https://reference.aspose.com/words/cpp/aspose.words.saving/multipagelayout/singlepage/) – save only the first of the specified pages
* [Grid](https://reference.aspose.com/words/cpp/aspose.words.saving/multipagelayout/grid/) – arrange the pages in a grid, left-to-right and top-to-bottom, while specifying the number of columns
* [Horizontal](https://reference.aspose.com/words/cpp/aspose.words.saving/multipagelayout/horizontal/) – arrange the pages horizontally side-by-side, left-to-right, in a single output
* [Vertical](https://reference.aspose.com/words/cpp/aspose.words.saving/multipagelayout/vertical/) – arrange the pages vertically one below the other in a single output
* [TiffFrames](https://reference.aspose.com/words/cpp/aspose.words.saving/multipagelayout/tiffframes/) – arrange each page as a separate frame in a multi-frame TIFF image, applies only to TIFF image formats

The following code example shows how to save a multi-page DOCX document as JPEG image with Horizontal layout:

{{< gist "aspose-words-gists" "8eeaafcfcc55d78505f0f378ad8c6907" "horizontal-layout.cs" >}}

You can also customize the output file page appearance – specify [BackColor](https://reference.aspose.com/words/cpp/aspose.words.saving/multipagelayout/get_backcolor/), [BorderColor](https://reference.aspose.com/words/cpp/aspose.words.saving/multipagelayout/get_bordercolor/), and [BorderWidth](https://reference.aspose.com/words/cpp/aspose.words.saving/multipagelayout/get_borderwidth/).

The following code example shows how to save a multi-page DOCX document as PNG image with Grid layout:

{{< gist "aspose-words-gists" "8eeaafcfcc55d78505f0f378ad8c6907" "grid-layout.cs" >}}

------ 

## FAQ

1. **Q:** How can I export each page of a document as a separate image file?  
   **A:** Use the `SinglePage` layout together with the `PageRange` property of `ImageSaveOptions`. Set `PageRange` to the desired page number and call `Save` inside a loop for all pages.

2. **Q:** Can I create a multi‑frame TIFF where each page becomes a separate frame?  
   **A:** Yes. Set `options->set_MultiPageLayout(Aspose::Words::Saving::MultiPageLayout::TiffFrames());` and use `SaveFormat::Tiff`. Each document page will be stored as an individual frame in the resulting TIFF file.

3. **Q:** How do I control the resolution (DPI) of the exported images?  
   **A:** Use `options->set_Resolution(int dpi);`. For example, `options->set_Resolution(300);` will generate 300 DPI images, which is useful for high‑quality prints.

4. **Q:** Is it possible to export only a subset of pages, e.g., pages 2‑5?  
   **A:** Yes. Set the `PageRange` property: `options->set_PageRange(Aspose::Words::Saving::PageRange(2, 5));`. The export will include only the specified pages using the chosen layout.

5. **Q:** How can I change the background color of the exported image pages?  
   **A:** Access the layout object via `options->get_PageLayout()` and call `set_BackColor`. Example: `options->get_PageLayout()->set_BackColor(System::Drawing::Color::get_White());`. This color fills the area around each page when using grid‑type layouts.