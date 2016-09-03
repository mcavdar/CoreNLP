---
title: Download
keywords: download
permalink: '/download.html'
---

Stanford CoreNLP can be downloaded via the link below. This will download a large (536 MB) zip file containing (1) the CoreNLP code jar, (2) the CoreNLP models jar (required in your classpath for most tasks) (3) the libraries required to run CoreNLP, and (4) documentation / source code for the project. This is everything for getting going on English!  Unzip this file, open the folder that results and you're ready to use it.

<div style="text-align:center; margin-top: 5ex; margin-bottom:5ex;"> <a class="downloadbutton" href="http://nlp.stanford.edu/software/stanford-corenlp-full-2015-12-09.zip">Download CoreNLP 3.6.0</a> </div>

**Other languages:** For working with another (human) language, you need additional model files. We have model files for several other languages. And we have more
model files for English, including for dealing with uncased English (that is, English which is not conventionally capitalized, whether texting or telegrams).
You can find the latest models in the table below.  Versions for earlier releases are available on [the release history page](history.html).

| Language | model jar | version |
| :------- | :-------- | | :----- |
| Chinese | [download](http://nlp.stanford.edu/software/stanford-chinese-corenlp-2016-01-19-models.jar) | 3.6.0 |
| English | [download](http://nlp.stanford.edu/software/stanford-english-corenlp-2016-01-10-models.jar) | 3.6.0 |
| French | [download](http://nlp.stanford.edu/software/stanford-french-corenlp-2016-01-14-models.jar) | 3.6.0 |
| German | [download](http://nlp.stanford.edu/software/stanford-german-2016-01-19-models.jar) | 3.6.0 |
| Spanish | [download](http://nlp.stanford.edu/software/stanford-spanish-corenlp-2015-10-14-models.jar) | 3.6.0 |

If you want to change the source code and recompile the files, see [these instructions](files/basic-compiling.txt).
Previous releases can be found on [the release history page](history.html).

**Java:** Stanford CoreNLP now requires Java 8. If you do not have
this installed you should first of all install Java 8.  Probably
[the JDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html),
but [the JRE](http://java.com/) will do if you are only going to be a user.

**GitHub**: Here is the [Stanford CoreNLP GitHub site](https://github.com/stanfordnlp/CoreNLP).

**Maven**: You can find Stanford CoreNLP on [Maven Central](http://search.maven.org/#browse%7C11864822). The crucial thing to know is that CoreNLP needs its models to run (most parts beyond the tokenizer) and so you need to specify both the code jar and the models jar in your `pom.xml`, as follows:
(Note: Maven releases are made several days after the release on the website.)

``` xml
<dependencies>
<dependency>
    <groupId>edu.stanford.nlp</groupId>
    <artifactId>stanford-corenlp</artifactId>
    <version>3.6.0</version>
</dependency>
<dependency>
    <groupId>edu.stanford.nlp</groupId>
    <artifactId>stanford-corenlp</artifactId>
    <version>3.6.0</version>
    <classifier>models</classifier>
</dependency>
</dependencies>
```

If you want to get a language models jar off of Maven for Chinese, Spanish, or German, add this to your `pom.xml`:

``` xml
<dependency>
    <groupId>edu.stanford.nlp</groupId>
    <artifactId>stanford-corenlp</artifactId>
    <version>3.6.0</version>
    <classifier>models-chinese</classifier>
</dependency>
```

Replace "models-chinese" with one or more of "models-english", "models-french", "models-german" or "models-spanish" for resources for other languages!

