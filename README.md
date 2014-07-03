SWITCHcast User Manual
======================

This manual explains how to use the recorder of SWITCHcast. It has been written using the EPUB3 standard and is currently still a work in progress.

Some useful links:

* [About SWITCHcast](https://www.switch.ch/cast)
* [Download SWITCHcast Recorder](https://www.switch.ch/cast/downloads/)


Create content using Susy, SASS and Compass
-------------------------------------

## Install Gems

Currently, a pre-release version of Compass has to be installed to make it work with Susy

  gem install compass --pre
  gem install susy sass

If you get error messages when Compass compiles, add this gem as well

  gem install compass-susy-plugin


## Tell Compass to watch for changes

  compass watch


Compile book.epub
-----------------


    ./publish book


Development
-----------


## ePub validation

This project uses epubcheck to validate the generated ePubs. If the ``build.sh`` script complains when running ``epubcheck``, make sure you have java installed and it's in your PATH.

If you need help running epubcheck read this <a href="http://blog.threepress.org/2010/12/16/running-epubcheck-on-your-computer/">step-by-step guide</a>.

## Using the check script to validate the book.

It's supereasy. Just do:

    ./check book.epub

This project currently uses EpubCheck version 3.0.1.


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
