bnd-book
========

An online eBook about the BND tool for OSGi.

Created from [the original BND book/manual](http://www.aqute.biz/Bnd/Bnd) by [Peter Kriens][1]

Building
--------
This book is composed of a series of [markdown](http://daringfireball.net/projects/markdown/) formatted sections (much like a Wiki). 
These are in the `docs` folder in the source. A scala based tool called [pamflet](http://pamflet.databinder.net/Pamflet.html) is
used to transform these sources into HTML (in the `target` folder). 

To build the source you will need to install the [simple build tool (sbt)](http://www.scala-sbt.org/). 
Please follow [these instructions](https://github.com/harrah/xsbt/wiki/Getting-Started-Setup) to get this tool installed and setup.

When you have SBT installed run `sbt write-pamflet` from the command line. You then need to copy the images in the `docs/img` folder into the `target` folder.
(the [Ant](http://ant.apache.org/) build script (`build.xml`) has a target named `init` that perfoms this copying; use `ant init` from the command line).

To publish the eBook (`bnd-book.epub`) you need to install [pandoc](http://johnmacfarlane.net/pandoc/installing.html). 
Then use the command `pandoc -f html -t epub -o bnd.book.epub target/Combined+Pages.html` (or again the Ant script contains the `epub` target that invokes this command if it is on the PATH).

Contributors
-----------
* Original content created by [Peter Kriens][1]
* This derivative version created by [Chris Senior](https://github.com/duckAsteroid)
* Pamflet and build support provided by [Richard Dallaway](https://github.com/d6y)

License
--------
All material in this repository is licensed under the [Apache License version 2.0](http://www.apache.org/licenses/LICENSE-2.0.html), unless explicitly stated
otherwise.

   [1]: https://github.com/bnd