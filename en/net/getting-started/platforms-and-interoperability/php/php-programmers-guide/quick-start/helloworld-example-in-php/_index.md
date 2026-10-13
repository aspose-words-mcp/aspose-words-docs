---
title: HelloWorld Example in PHP
second_title: Aspose.Words for .NET
articleTitle: HelloWorld Example in PHP
linktitle: HelloWorld Example in PHP
description: "Building documents from scratch using Aspose.Words for .NET in PHP via COM in C#."
type: docs
weight: 40
ai_search_scope: words_net
ai_search_endpoint: "https://docsearch.api.aspose.cloud/ask"
ai_search_fast_endpoint: "https://docsearch.api.aspose.cloud/search"
url: /net/helloworld-example-in-php/
timestamp: 2024-01-27-14-07-04
---

{{% alert color="grey" %}}

## Purpose Summary

This page explains how to run a Hello World example in PHP.

{{% /alert %}}

## Aspose.Words - HelloWorld Example

Hello World Example

**PHP Code**

{{< highlight php >}}
$dataDir = '.';
$doc = new \COM("Aspose.Words.Document");
$builder = new \COM("Aspose.Words.DocumentBuilder");
$builder->Document = $doc;
$builder->Write("Hello world!");
$doc->Save($dataDir . "/HelloWorld Out.docx");
{{< /highlight >}}

## Download Running Code

Download **HelloWorld Example (Aspose.Words)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Plugins/Aspose_Words_NET_for_PHP/src/aspose/words/quickstart/HelloWorld.php)
