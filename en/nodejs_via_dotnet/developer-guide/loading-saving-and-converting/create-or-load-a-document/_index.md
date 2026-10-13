---
title: Create or Load a Document in Node.js
second_title: Aspose.Words for Node.js via .NET
articleTitle: Create or Load a Document
linktitle: Create or Load a Document
type: docs
ai_search_scope: words_nodejs
ai_search_endpoint: "https://docsearch.api.aspose.cloud/ask"
ai_search_fast_endpoint: "https://docsearch.api.aspose.cloud/search"
url: /nodejs-net/create-or-load-a-document/
aliases:
 - /nodejs/creating-or-loading-a-document/
 - /nodejs/create-or-load-a-document/
description: "Create a blank document or to load it from a file or stream using Node.js."
keywords: "create a document Node.js, load a document Node.js, create a blank document Node.js, load a document from file Node.js, load a document from stream Node.js, create a document Aspose Node.js, load a document Aspose Node.js, load formats supported by Aspose.Words"
weight: 10
timestamp: 2025-01-21-14-07-04
---

Almost any task that you want to perform with Aspose.Words involves loading a document. The [Document](https://reference.aspose.com/words/nodejs-net/aspose.words/document/) class represents a document loaded into memory. The document has several overloaded constructors allowing you to create a blank document or to load it from a file or an Array or Buffer. The document can be loaded in any load format supported by Aspose.Words. For the list of all supported load formats, see the [LoadFormat](https://reference.aspose.com/words/nodejs-net/aspose.words/loadformat/) enumeration.

## Create a New Document

We will call the [Document](https://reference.aspose.com/words/nodejs-net/aspose.words/document/) constructor without parameters to create a new blank document. If you want to generate a document programmatically, the simplest way is to use the [DocumentBuilder](https://reference.aspose.com/words/nodejs-net/aspose.words/documentbuilder/) class to add document contents.

The following code example shows how to create a document using the document builder:

{{< gist "aspose-words-gists" "96e42cb4a611465927f8e7b1b3d546d3" "create-new-document.js" >}}

{{% alert color="primary" %}}

Note the default values:

- A blank document contains one section with default parameters, one empty paragraph, some document styles. Actually this document is the same as the result of creating the “New document” in Microsoft Word.
- The document paper size is [PaperSize.Letter](https://reference.aspose.com/words/nodejs-net/aspose.words/papersize/#letter).

{{% /alert %}}

## Load a Document

To load an existing document in any of the [LoadFormat](https://reference.aspose.com/words/nodejs-net/aspose.words/loadformat/) formats, pass the file name or the Array or Buffer into one of the [Document](https://reference.aspose.com/words/nodejs-net/aspose.words/document/) constructors. The format of the loaded document is automatically determined by its extension.

### Load from a File

Pass a file name as string to the [Document](https://reference.aspose.com/words/nodejs-net/aspose.words/document/) constructor to open an existing document from a file.

The following code example shows how to open a document from a file:

{{< gist "aspose-words-gists" "96e42cb4a611465927f8e7b1b3d546d3" "open-document.js" >}}

You can download the template file of this example from [Aspose.Words GitHub](https://github.com/aspose-words/Aspose.Words-for-Node.js-via-.NET/blob/master/Data/Document.docx).

### Load from an Array or Buffer

To open a document from an Array or Buffer, simply pass an Array or Buffer object that contains the document into the [Document](https://reference.aspose.com/words/nodejs-net/aspose.words/document/) constructor.

The following code example shows how to open a document from an Array or Buffer:

{{< gist "aspose-words-gists" "96e42cb4a611465927f8e7b1b3d546d3" "open-from-stream.js" >}}

{{% alert color="primary" %}}

You can download the template file of this example from [Aspose.Words GitHub](https://github.com/aspose-words/Aspose.Words-for-Node.js-via-.NET/blob/master/Data/Document.docx).

{{% /alert %}}
