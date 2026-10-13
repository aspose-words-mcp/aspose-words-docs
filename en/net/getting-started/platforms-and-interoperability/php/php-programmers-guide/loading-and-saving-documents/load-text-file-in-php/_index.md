---
title: Load Text File in PHP
second_title: Aspose.Words for .NET
articleTitle: Load Text File in PHP
linktitle: Load Text File in PHP
description: "Loading text document using Aspose.Words for .NET in PHP using COM in C#."
type: docs
weight: 10
ai_search_scope: words_net
ai_search_endpoint: "https://docsearch.api.aspose.cloud/ask"
ai_search_fast_endpoint: "https://docsearch.api.aspose.cloud/search"
url: /net/load-text-file-in-php/
timestamp: 2024-01-27-14-07-04
---

{{% alert color="grey" %}}

## Purpose Summary

This page explains how to load a text file in PHP using Aspose.Words for .NET via PHP bindings.

{{% /alert %}}

## Aspose.Words - Load Text File Conversion Example

Load Text File Example

**PHP Code**

{{< highlight php >}}
$dataDir = '.';
$comHelper = new \COM("Aspose.Words.ComHelper");

// The encoding of the text file is automatically detected.
$doc = $comHelper->Open($dataDir."/LoadTxt.txt");

// Save as any Aspose.Words supported format, such as DOCX.
$doc->Save($dataDir . "/LoadTxt Out.docx");
print "Text document loaded successfully.\nFile saved at " . $dataDir . "LoadTxt Out.docx" . PHP_EOL;
{{< /highlight >}}

## Download Running Code

Download **Load Text File Example (Aspose.Words)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Plugins/Aspose_Words_NET_for_PHP/src/aspose/words/LoadingAndSaving/LoadTxt.php)
