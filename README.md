# netatus_literacy

## Steps
1.  java -cp /path/to/stanford-corenlp-3.9.1.jar:/path/to/stanford-corenlp-3.9.1-models.jar edu.stanford.nlp.pipeline.StanfordCoreNLP -annotators "tokenize, ssplit, pos, depparse, lemma" -ssplit.eolonly true -tokenize.whitespace true -outputFormat conll < input_file > output_file 2> /dev/null
