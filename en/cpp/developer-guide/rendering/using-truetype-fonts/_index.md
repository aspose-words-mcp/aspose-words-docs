---
title: Using TrueType Fonts in C++
second_title: Aspose.Words for C++
articleTitle: Using TrueType Fonts
linktitle: Using TrueType Fonts
description: "Aspose.Words for C++ can find the right font or its suitable replacement for correct document rendering. This ensures that the difference between the displayed document and the original is minimal when there is not enough information about a font."
type: docs
weight: 20
ai_search_scope: words_cpp
ai_search_endpoint: "https://docsearch.api.aspose.cloud/ask"
ai_search_fast_endpoint: "https://docsearch.api.aspose.cloud/search"
url: /cpp/using-truetype-fonts/
timestamp: 2024-01-27-14-07-04
---

{{% alert color="grey" %}}

## Purpose Summary

This page explains how to use TrueType fonts with Aspose.Words, including embedding and substitution.

{{% /alert %}}

When working with documents, you often have to use different fonts, styles, and sizes. Documents can contain any number of fonts, which are not necessarily limited to the fonts that are installed in the operating system. The fonts can be completely different, such as fonts taken from other operating systems, purchased, or created by users themselves.

Sometimes, information about the fonts being used is embedded in the document, eliminating display problems during document transfer. In some other cases, only the font name is known, which does not guarantee that the document will look the same way on another computer. In this case, Aspose.Words can find the right font or its suitable replacement, if the required font cannot be found, for correct rendering. 

## FAQ

1. **Q:** How can I tell Aspose.Words for C++ where to look for TrueType fonts on a Linux machine?
   **A:** Create a `FontSettings` object, call `SetFontsFolder` with the path to the folder that contains the required fonts, and assign it to the document via `Document::set_FontSettings`. Note that `SetFontsFolder` replaces the default font sources, so system fonts are no longer scanned. To keep them, combine your folder with the sources returned by `GetFontsSources` and pass the result to `SetFontsSources`.

2. **Q:** What should I do if a document references a font that is not installed on the target system?
   **A:** Font substitution is enabled by default, so Aspose.Words automatically selects a replacement font. To control the replacement explicitly, map the missing font name to an available TrueType font using the table substitution rule: `fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"MissingFont", System::MakeArray<System::String>({u"Arial"}));`.

3. **Q:** Can I embed the original TrueType font into the output PDF or DOCX so that the document looks identical on any machine?
   **A:** Yes. When saving to PDF, Aspose.Words embeds the used fonts by default as subsets; call `PdfSaveOptions::set_EmbedFullFonts(true)` to embed complete font files instead. For DOCX and other flow formats, call `doc->get_FontInfos()->set_EmbedTrueTypeFonts(true)` before saving.

4. **Q:** How do I load a font from a memory stream instead of a file path?
   **A:** Create a `MemoryFontSource` from the font bytes (e.g., `System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes)`) and pass it to `FontSettings::SetFontsSources` together with any other font sources you need. This allows the engine to use fonts that are embedded in your application or downloaded at runtime.

```cpp
// Example: Set custom font folder and embed full fonts into PDF
System::SharedPtr<Aspose::Words::Fonts::FontSettings> fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->SetFontsFolder(u"/usr/share/fonts/truetype", true);

System::SharedPtr<Aspose::Words::Document> doc = System::MakeObject<Aspose::Words::Document>(u"input.docx");
doc->set_FontSettings(fontSettings);

System::SharedPtr<Aspose::Words::Saving::PdfSaveOptions> saveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
saveOptions->set_EmbedFullFonts(true);
doc->Save(u"output.pdf", saveOptions);
```