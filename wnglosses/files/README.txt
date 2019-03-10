

This package contains an automatic parsing of the Princeton WordNet Gloss Corpus project, in an easy-to-use XML file.
The original data are here: http://wordnetcode.princeton.edu/glosstag.shtml

DISCLAIMER:
This XML is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.


NOTE:
- Within example sentences, only the synset terms were disambiguated.
- Text enclosed within tags has been escaped using XML entities. In order to retrieve the actual human-readable character we highly suggest to unescape it.
  (e.g. in Java, you can use the StringEscapeUtils class provided by the apache commons-lang API).


==============================================================================================================================================
FORMAT OF THE XML FILE
==============================================================================================================================================

The XML contains a list of "synset" tags, with the respective "id" (i.e. the part-of-speech and the WordNet offset) as attribute.
Each synset contains a list of "examples" and "definitions" tags.
Then, example and definition contains the plain text (tokenized), and a list of "token" tag.   
Each token has two or four attributes,  depending on whether or not contains an annotation :
 - "pos" : the part of speech of the token;
 - "lemma" : the lemma of the token;
 - "senseID" : the WordNet senseKey of the token (if it is disambiguated);
 - "senseType" : the sense annotation type.

There are two different sense annotation type:
 - man : manually-inserted sense tag
 - auto : automatically generated sense tag
    

The following listing shows the XML representation:

<?xml version="1.0" encoding="UTF-8" wordnet="3.0"?>
<synset id="v00003662">
	<examples>
		<example>
		<text>force out the air</text>
		<tokens>
			<token pos="VB" lemma="force" senseID="force_out%2:29:00::" senseType="auto">force</token>
			<token pos="RP" lemma="out" senseID="force_out%2:29:00::" senseType="auto">out</token>
			<token pos="DT" lemma="the">the</token>
			<token pos="NN" lemma="air">air</token>
		</tokens>
		</example>
		<example>
		<text>force out the splinter</text>
		<tokens>
			<token pos="VB" lemma="force" senseID="force_out%2:29:00::" senseType="auto">force</token>
			<token pos="RP" lemma="out" senseID="force_out%2:29:00::" senseType="auto">out</token>
			<token pos="DT" lemma="the">the</token>
			<token pos="NN" lemma="splinter">splinter</token>
		</tokens>
		</example>
	</examples>
	<definitions>
		<definition>
		<text>emit or cause to move with force of effort</text>
		<tokens>
			<token pos="VB" lemma="emit" senseID="emit%2:29:00::" senseType="man">emit</token>
			<token pos="CC" lemma="or">or</token>
			<token pos="VB" lemma="cause">cause</token>
			<token pos="TO" lemma="to">to</token>
			<token pos="VB" lemma="move">move</token>
			<token pos="IN" lemma="with">with</token>
			<token pos="NN" lemma="force">force</token>
			<token pos="IN" lemma="of">of</token>
			<token pos="NN" lemma="effort" senseID="effort%1:04:01::" senseType="man">effort</token>
		</tokens>
		</definition>
	</definitions>
</synset>
<synset id="...






