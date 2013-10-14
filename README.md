ePub-Boilerplate
================

http://javierarce.github.com/epub-boilerplate

ePub Boilerplate is a simple template that helps you build ePub-formatted books.

## How to use the template

1. Clone the repo:

        $ git clone git@github.com:javierarce/epub-boilerplate.git

2. Edit the contents of the ``book`` directory<sup>1</sup>.

3. Run the publish script to generate and validate the book:

        $ ./publish book

1: You'll find comments inside several files to guide you.

## Structure of a book

Here's the structure of the sample book included in the repo:

    ▾ book/
      ▾ META-INF/
          com.apple.ibooks.display-options.xml
          container.xml
      ▾ OEBPS/
        ▾ Images/
            cover.jpg
            image-01.jpg
            image-02.png
        ▾ Styles/
            style.css
        ▾ Text/
            acknowledgements.xhtml
            chapter01.xhtml
            chapter02.xhtml
            chapter03.xhtml
            cover.xhtml
            dedication.xhtml
            endnotes.xhtml
            foreword.xhtml
            frontmatter.xhtml
            introduction.xhtml
            toc.xhtml
          content.opf
          toc.ncx
        mimetype
        
## ePub validation

This project uses epubcheck to validate the generated ePubs. If the ``build.sh`` script complains when running ``epubcheck``, make sure you have java installed and it's in your PATH.

If you need help running epubcheck read this <a href="http://blog.threepress.org/2010/12/16/running-epubcheck-on-your-computer/">step-by-step guide</a>.

## Using the check script to validate the book.

It's supereasy. Just do: 

    $ ./check book.epub

This project currently uses EpubCheck version 3.0-RC-1.

## Style

*Caveat lector*: currently there aren't any defined styles. While I add a basic layout have a look at the <a href="https://github.com/mattharrison/epub-css-starter-kit">ePub CSS Starter Kit</a>.

## ePub → mobi

Here's what you can do if you want to transform your ``.epub`` file to ``.mobi``:

1. Download [KindleGen](http://www.amazon.com/gp/feature.html?ie=UTF8&docId=1000765211).
2. Uncompress the file.
3. Copy the ``kindlegen`` executable to the ``bin`` folder.
4. Run ``./bin/kindlegen book.epub``.

## Useful resources
      
* [EPUB 3.0 spec](http://idpf.org/epub/30)
* [Device compatibilty chart](http://wiki.mobileread.com/wiki/Device_Compatibility)
* [ePub CSS Starter Kit](https://github.com/mattharrison/epub-css-starter-kit)
* [ePub Validator](http://code.google.com/p/epubcheck)
* [UUID generator](http://www.famkruithof.net/uuid/uuidgen)
* [BISAC Subject Headings List](http://www.bisg.org/what-we-do-0-136-bisac-subject-headings-list-major-subjects.php)
* [Practical ePub metadata: Authorship](http://blog.threepress.org/2009/11/27/practical-epub-metadata-authorship/)
* [MARC Code List for Relators](http://www.loc.gov/marc/relators)
* [What Is EPUB 3? An Introduction to the EPUB Specification for Multimedia Publishing](http://shop.oreilly.com/product/0636920022442.do)
