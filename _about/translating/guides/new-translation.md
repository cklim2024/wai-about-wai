---
title: "How to Translate a WAI Resource"
nav_title: New translation
github:
  repository: w3c/wai-about-wai
  path: '_about/translating/guides/new-translation.md'
permalink: /about/translating/guides/new-translation/
ref: /about/translating/guides/new-translation/
lang: en
last_updated: 2024-03-07
redirect_from:
  - /about/translating/guides/translation-guidance/
description: Help make the Web accessible to people with disabilities around the world. We appreciate your contributions to translating W3C WAI accessibility resources.
image: /content-images/wai-about-wai/social-translations.png

feedbackmail: wai@w3.org
footer: |
  <p><strong>Date:</strong> Updated 7 March 2024.</p>
  <p><strong>Editors:</strong> <a href="https://www.w3.org/People/Shawn/">Shawn Lawton Henry</a> and Rémi Bétin.</p>
  <p>Developed as part of the <a href="https://www.w3.org/WAI/about/projects/wai-coop/">WAI-CooP project</a>, co-funded by the European Commission.</p>
---

{::nomarkdown}
{% include box.html type="start" h="2" title="Summary" class="full" %}
{:/}

This page guides you through the technical steps to translate Web Accessibility Initiative (WAI) resources, and provides other important guidance.

For instructions on translating the Web Content Accessibility Guidelines (WCAG), see [[How to Translate WCAG 2]](/about/translating/guides/wcag/).

{::nomarkdown}
{% include box.html type="end" %}
{:/}

{::options toc_levels="2" /}
{::nomarkdown}
{% include_cached toc.html type="start" title="Page Contents" class="simple" %}
{:/}

-   TOC is created automatically.
{:toc}

{::nomarkdown}
{% include toc.html type="end" %}
{:/}

## General guidance

- Do not change or adapt or add to the meaning of the English version in your translation.
- If you have suggestions for changes to the English version, submit them via GitHub or e-mail using the links in the “Help improve this page” box near the bottom of the page.
- Before starting, find the language short code "subtag" from [Language Subtag Registry {% include_cached external.html %}](https://www.iana.org/assignments/language-subtag-registry/language-subtag-registry). You will use it at multiple times during the translation.


## Step 1: Create a new file {#create-file}

Duplicate the file used by the original version, with the language shortcode added to the middle of the filename, as follows:

{::nomarkdown}
{% include box.html type="start" title="Example" %}
{:/}

- Original English file: `index.md`
- New Korean file: `index.ko.md`

{::nomarkdown}
{% include box.html type="end" %}
{:/}

## Step 2: Update "front matter" metadata {#frontmatter}

{::nomarkdown}
{% include box.html type="start" class="highlighted" %}
{:/}

From now on, only edit the newly created translation file.

{::nomarkdown}
{% include box.html type="end" %}
{:/}

At the top of WAI website files are some metadata, also known as "front matter".

Your first step into the file is to update this section.

{::nomarkdown}
{% include box.html type="start" title="Example of front matter (this may differ on your file)" %}
{:/}
```yaml
---
title: Evaluation Tools Overview
lang: en
last_updated: 2020-04-28

github:
  repository: w3c/wai-eval-tools-overview
  path: "content/index.md"

permalink: /test-evaluate/tools/
ref: /test-evaluate/tools/

footer: >
   <p><strong>Date:</strong> Updated 28 April 2020.</p>
   <p><strong>Editor:</strong> <a href="https://www.w3.org/People/Shawn/">Shawn Lawton Henry</a>.</p>
   <p>Video developed by the Education and Outreach Working Group (<a href="http://www.w3.org/WAI/EO/">EOWG</a>) with support from the <a href="https://www.w3.org/WAI/about/projects/wai-guide/">WAI-Guide</a> project funded by the European Commission (EC) under the Horizon 2020 program (Grant Agreement 822245). <a href="./acknowledgements/">Acknowledgements</a>.</p>
---
```
{::nomarkdown}
{% include box.html type="end" %}
{:/}

### General instructions for front matter

#### 2.1. Update the following front matter values:

`lang`
- Replace the original value (`en`) with the language shortcode of your translation.  

`last_updated`
- Change `last_updated: 2000-00-00` to the date you finish the translation.  
  Use the format: YYYY-MM-DD (with month in the middle).

`path` (below `github`)
- Add the language shortcode at the middle of the filename.

`permalink`
- Add the language shortcode at the end of the permalink, with no `/` at the end.

`footer` (not always present)
- If this attribute is present, translate its content.
- Do not change the dates in this section. Those dates should be the same in your translation as in the English version.

#### 2.2. Add translators & contributors names.

After `last_updated`, add these lines, depending on how many translators there are and if there are contributors.  

Policy for names and links is introduced in [Translating WAI Resources]({{ "/about/translating" | relative_url }}#links).

{::nomarkdown}
{% include box.html type="start" %}
{:/}
```yaml
translators:
  - name: "Your Name"
contributors:
  - name: "Other Name"
  - name: "Other Name"
```
{::nomarkdown}
{% include box.html type="end" %}
{:/}

Or, if the lines are there with "`#`" before them to comment them out: delete the # and the space.

#### Updated Example

{::nomarkdown}
{% include box.html type="start" title="Updated front matter for a translation into French" %}
{:/}
{% include excol.html type="start" id="optional-id" %}

Show example

{% include excol.html type="middle" %}

```yaml
---
title: Evaluation Tools Overview
lang: fr
last_updated: 2023-09-13

translators:
  - name: "Your Name"
contributors:
  - name: "Other Name"
  - name: "Other Name"

github:
  repository: w3c/wai-eval-tools-overview
  path: "content/index.fr.md"

permalink: /test-evaluate/tools/fr
ref: /test-evaluate/tools/

footer: >
  <p><strong>Date :</strong> Mise à jour : 28 avril 2020.</p>
  <p><strong>Rédactrice :</strong> <a href="https://www.w3.org/People/Shawn/">Shawn Lawton Henry</a>.</p>
  <p>Vidéo créée par le groupe de travail Éducation et Promotion (<a href="http://www.w3.org/WAI/EO/">EOWG</a>) avec le soutien du projet <a href="https://www.w3.org/WAI/about/projects/wai-guide/">WAI-Guide</a> financé par la Commission européenne (CE) dans le cadre du programme Horizon 2020 (convention de subvention n°822245) <a href="./acknowledgements/">Remerciements</a>.</p>
---
```

{% include excol.html type="end" %}
{::nomarkdown}
{% include box.html type="end" %}
{:/}

### Follow additional inline instructions

Many resources have inline instructions in the front matter (after the "`#`" character). 

Please follow these instructions. It will help you know what to translate/update and what to not change.

## Step 3: Translate main content

### Markdown/Code

Please leave the code, HTML, and markdown as is without changing it.

Make sure to:

{::nomarkdown}
<ul>
<li>
{:/}

Translate titles in the markdown, such as "Summary" in:

{::nomarkdown}
{% include box.html type="start" %}
{:/}
```liquid
{% raw %}{% include box.html type="start" title="Summary" class="" %}{% endraw %}
```
{::nomarkdown}
{% include box.html type="end" %}
{:/}

{::nomarkdown}
</li>
<li>
{:/}

Translate image alternative text, such as “mouse crossed out” in:

{::nomarkdown}
{% include box.html type="start" %}
{:/}

- in Markdown: `![mouse crossed out](https://www.w3.org/WAI/intro/no-mouse.png)`
- in HTML: `<img src="https://www.w3.org/WAI/intro/no-mouse.png" alt="mouse crossed out" />`

{::nomarkdown}
{% include box.html type="end" %}
{:/}

{::nomarkdown}
</li>
<li>
{:/}

Make sure that the quote marks stay as is, and are not converted to "smart quotes" by word processing software.

{::nomarkdown}
</li>
</ul>
{:/}

### Links

Most links are formatted with single or double brackets and parentheses; for example:

{::nomarkdown}
{% include box.html type="start" %}
{:/}
```markdown
[Text that is linked]({%raw%}/{%endraw%}path/to/filename/)
[[Title of WAI Page]]({%raw%}/{%endraw%}path/to/filename/)
```
{::nomarkdown}
{% include box.html type="end" %}
{:/}

Make sure to:
- Keep brackets and parentheses together, with no space between the closing `]` and the opening `(`.
- Keep double `[[` or single brackets `[` as they are.
- Translate the text in the links, including document titles.
- Do not manually add `(in English)`, even for external links.

### Specific wording {#specific-wording}
- Check [other translations in your language](/translations) to see how similar words and concepts have been translated. In particular, [Authorized Translations](https://www.w3.org/Translations/authorized.html) have had significant review and input.
- Read the [General Translation Glossary {% include_cached external.html %}](https://github.com/w3c/translation-glossaries/blob/main/general.md) and see if there is a [glossary for your language {% include_cached external.html %}](https://github.com/w3c/translation-glossaries#readme).
- Consider different dialects. Where possible, the translation should use words and phrases that will be best understood across different areas.

{::nomarkdown}
{% include box.html type="start" title="We are here to help" %}
{:/}

If you have any questions for us about the wording, you can report them in the GitHub issue or send email to [group-wai-translations@w3.org](mailto:group-wai-translations@w3.org)[^1].

We are happy to help you decide on the best translated wording by sharing the considerations and nuances that went into choosing the wording for the English page.

{::nomarkdown}
{% include box.html type="end" %}
{:/}


## Text Editor

The markdown files are very sensitive to indentation, commas, quotes, and special characters.

We recommend that you use a markdown editor or a simple text editor (including GitHub interface) — and not a document editor like Microsoft Word that often changes quotes and indentation.

## Resource-Specific Information

Some resources have specific Translations notes.

{::nomarkdown}
<ul>
<li>
{:/}

At the top of the resource file (in the ["front matter" metadata](/about/translating/guides/new-translation/#frontmatter)), see if there is a comment like this one:

{::nomarkdown}
{% include box.html type="start" %}
{:/}
```
# Read Translations Notes at https://github.com/w3c/path-to-repository#readme
```
{::nomarkdown}
{% include box.html type="end" %}
{:/}

In that case, follow the link and read the specific guidance.

{::nomarkdown}
</li>
<li>
{:/}

If you wish to translate the [WCAG-EM Report Tool](https://www.w3.org/WAI/eval/report-tool/), please read [this specific guidance {% include_cached external.html %}](https://github.com/w3c/wai-wcag-em-report-tool/wiki/How-to-add-a-language), as different steps have to be followed.

{::nomarkdown}
</li>
</ul>
{:/}

## We are here to help

If you have any questions about the translation, please report them in the related GitHub issue so that WAI team and other volunteers can help. Alternatively, send an e-mail to the publicly-archived [public-wai-translations@w3.org](mailto:public-wai-translations@w3.org) mailing-list.

We are happy to help you decide on the best translated wording by sharing the considerations and nuances that went into choosing the wording for the English page.