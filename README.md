# Summary

This data is a manual annotation of the corpus from multimedia annotated corpus
of the [Chuklang](http://chuklang.ru/) project, a dialectal corpus of the Amguema
variant of Chukchi.

# Introduction

The corpus contains spoken Chukchi in the Amguema variant. Chukchi is a polysynthetic
language spoken in the Chukotka Autonomous Okrug in the north-east of Siberia.


# Acknowledgements

This work is entirely based on the glossed corpus developed by 
the [Chuklang](http://chuklang.ru/) project. They have their own
[acknowledgements](http://chuklang.ru/acknowledgements) here.

## References

* (citation)

# Orthography

The original texts were transcribed from recordings using a Latin-based transcription 
system and glosses. The system of glosses is largely described in the document 
[Глоссы Экспедицинного Проекта Чукотка—2016](http://chuklang.ru/static/chukchi_glosses_20171020.pdf).

The transcriptions have been converted to Chukchi orthography automatically using
a [convertor](https://github.com/BasilisAndr/chkchn/tree/master/translit) developed
by [Vasilisa Adriyanets](github.com/BasilisAndr/). There may be errors in the automatic
conversion. Particularly the treatment of Russian loan words and proper nouns, the 
character *s*, and the glottal stop.

# Metadata

Each sentence has the following information:

* `sent_id`: This indicates the file and the sentence number. The filename is equivalent 
to the name from the [Chuklang](http://chuklang.ru/) site.
* `text`: The text in the Chukchi orthography. This is automatically generated from the 
phonemic transcription and partially manually corrected. See Orthography notes above.
* `text[phon]`: A phonemic transcription. Words in Cyrillic in here are either false 
starts or sequences of loan words.
* `text[rus]`: A free translation of the sentence in Russian.
* `text[eng]`: A free translation of the sentence in English.
* `labels`: A set of labels indicating some metadata about the sentence, may include the 
annotator name, if the sentence is complete, or just has dependencies, or if there is 
something unclear in the syntax.

In addition, some sentences have extra information

* `timestamp`: The offset of the `.wav` file in `hh:mm:ss` format where the sentence
starts.
* `comment`: A comment from the transcriber, usually in Russian.
* `text[eng']`: A secondary, more literal translation in English of the structure that
the sentence is believed to have.

# Tokenisation

Tokens in the corpus are defined as sequences of non-whitespace or punctuation
characters separated by whitespace.

Underneath tokens are syntactic words. These are words which take part
in dependency relations.

A single token may be split into more than one word based on the following criteria:

* Emphatic clitics are split (notably *-ъм* and *-а*)
* In non-absolutive noun phrases, attributive modifiers (nouns, adjectives and numerals) 
which have been incorporated are split. The splits are based on the provided gloss.

Incorporation into lexical verbs does not involve splitting in the basic representation,
sentences are annotated according to their surface syntax, e.g. a verb
with an incorporated object is annotated as intransitive following its
agreement morphology.

In the enhanced representation, the argument structure is recovered,
incorporated items are given nodes.

# Morphology

# Syntax

# Changelog

* 2020-11-15 v2.7
  * Initial release in Universal Dependencies.


<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.7
License: CC BY-SA 4.0
Includes text: yes
Genre: speech
Lemmas: not available
UPOS: converted with corrections
XPOS: not available
Features: not available
Relations: manual
Contributors: Tyers, Francis; Mischenkova, Karina
Contributing: elsewhere
Contact: ftyers@iu.edu
===============================================================================
</pre>

