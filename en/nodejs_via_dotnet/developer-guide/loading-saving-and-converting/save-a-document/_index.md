---
title: Save a Document in Node.js
second_title: Aspose.Words for Node.js via .NET
articleTitle: Save a Document
linktitle: Save a Document
aliases: [/nodejs/saving-a-document/]
type: docs
description: "Save a document in any supported format using Node.js."
keywords: "save a document Node.js, save a document to file Node.js, save a document to stream Node.js, save a document Aspose, save formats supported by Aspose.Words"
weight: 20
ai_search_scope: words_nodejs
ai_search_endpoint: "https://docsearch.api.aspose.cloud/ask"
ai_search_fast_endpoint: "https://docsearch.api.aspose.cloud/search"
url: /nodejs-net/save-a-document/
aliases: [/nodejs/save-a-document/]
timestamp: 2025-04-21-14-07-04
---

Most of the tasks you need to perform with Aspose.Words involve saving a document. To save a document Aspose.Words provides the [save](https://reference.aspose.com/words/nodejs-net/aspose.words/document/save/) method of the [Document](https://reference.aspose.com/words/nodejs-net/aspose.words/document/) class. There are overloads that allow saving a document to a file or stream. The document can be saved in any save format supported by Aspose.Words. For the list of all supported save formats, see the [SaveFormat](https://reference.aspose.com/words/nodejs-net/aspose.words/saveformat/) enumeration.

## Save a Document to a File {#save-a-document-to-a-file}

Simply use the [save](https://reference.aspose.com/words/nodejs-net/aspose.words/document/save/) method with a file name. Aspose.Words will determine the save format from the file extension that you specify.

The following code example shows how to load and save a document to a file:

{{< gist "aspose-words-gists" "757cf7d3534a39730cf3290d418681ab" "load-and-save.js" >}}

{{% alert color="primary" %}}

You can download the template file of this example from [Aspose.Words GitHub](https://github.com/aspose-words/Aspose.Words-for-Node.js-via-.NET/blob/master/Data/Document.docx).

{{% /alert %}}

## Save a Document to a Stream {#save-a-document-to-a-stream}

Pass a stream object to the [save](https://reference.aspose.com/words/nodejs-net/aspose.words/document/save/) method. It's necessary to specify the save format explicitly when saving to a stream.

The following code example shows how to load and save a document to a stream:

{{< gist "aspose-words-gists" "757cf7d3534a39730cf3290d418681ab" "load-and-save-to-stream.js" >}}

You can download the template file of this example from [Aspose.Words GitHub](https://github.com/aspose-words/Aspose.Words-for-Node.js-via-.NET/blob/master/Data/Document.docx).

## Save a Document to PCL {#save-a-document-to-pcl}

Aspose.Words supports saving a document into PCL (Printer Command Language). Aspose.Words can save documents into PCL 6 (PCL 6 Enhanced or PCL XL) format. The [PclSaveOptions](https://reference.aspose.com/words/nodejs-net/aspose.words.saving/pclsaveoptions/) class can be used to specify additional options when saving a document into the PCL format.

The following code example shows how to save a document to PCL using save options:

{{< gist "aspose-words-gists" "757cf7d3534a39730cf3290d418681ab" "rasterize-transformed-elements.js" >}}

