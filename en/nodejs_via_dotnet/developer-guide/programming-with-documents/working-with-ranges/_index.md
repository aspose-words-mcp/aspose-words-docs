---
title: Working with Ranges in Node.js
second_title: Aspose.Words for Node.js via .NET
articleTitle: Working with Ranges
linktitle: Working with Ranges
description: "Work with ranges in a document using Node.js."
type: docs
weight: 130
ai_search_scope: words_nodejs
ai_search_endpoint: "https://docsearch.api.aspose.cloud/ask"
ai_search_fast_endpoint: "https://docsearch.api.aspose.cloud/search"
url: /nodejs-net/working-with-ranges/
timestamp: 2025-07-09-10-05-05
---

{{% alert color="primary" %}}

In Aspose.Words, a [Range](https://reference.aspose.com/words/nodejs-net/aspose.words/range/) is a “flat window” into an otherwise tree-like model of the document.

{{% /alert %}}

If you have worked with Microsoft Word Automation, you probably know that one of the main tools to examine and modify document content is the [Range](https://reference.aspose.com/words/nodejs-net/aspose.words/range/) object. [Range](https://reference.aspose.com/words/nodejs-net/aspose.words/range/) is like a "window" into the document content and formatting. Aspose.Words also has the [Range](https://reference.aspose.com/words/nodejs-net/aspose.words/range/) class and it is designed to look and act similarly to **Range** in Microsoft Word. Although **Range** cannot cover an arbitrary portion of a document and does not have a **Start** and **End**, you can access the range covered by any document node including the [Document](https://reference.aspose.com/words/nodejs-net/aspose.words/document/) itself. In other words, each node has its own range. The [Range](https://reference.aspose.com/words/nodejs-net/aspose.words/range/) object allows you to access and modify text, bookmarks and form fields within the range.

## Retrieve Plain Text

Use the [text](https://reference.aspose.com/words/nodejs-net/aspose.words/range/text/) property to retrieve plain, unformatted text of the range.

The following code example shows how to get a plain, unformatted text of a range:

{{< gist "aspose-words-gists" "5abf4b66965fca92533f9a266a06c7ed" "ranges-get-text.js" >}}

{{% alert color="primary" %}}

You can download the sample file of this example from [Aspose.Words GitHub](https://github.com/aspose-words/Aspose.Words-for-Node.js-via-.NET/tree/main/Data/Document.docx).

{{% /alert %}}

## Deleting Text

Range allows the deletion of all characters of the range by calling [delete](https://reference.aspose.com/words/nodejs-net/aspose.words/range/delete/). 

The following code example shows how to delete all characters of a range:

{{< gist "aspose-words-gists" "5abf4b66965fca92533f9a266a06c7ed" "ranges-delete-text.js" >}}

{{% alert color="primary" %}}

You can download the sample file of this example from [Aspose.Words GitHub](https://github.com/aspose-words/Aspose.Words-for-Node.js-via-.NET/tree/main/Data/Document.docx).

{{% /alert %}}
