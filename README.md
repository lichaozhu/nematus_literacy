# netatus_literacy

## Steps

### Tokenization

### Annotation
1. Download [Stanford CoreNLP (4.5.4)](https://nlp.stanford.edu/software/stanford-corenlp-4.5.4.zip) and unzip
2. Download [French Lnguage Model](https://nlp.stanford.edu/software/stanford-corenlp-4.5.4-models-french.jar)
3. Put the French Language Model into the unzipped Stanford CoreNLP repository
4. Go to the Stanford CoreNLP repository 
5. ! export CLASSPATH="$CLASSPATH:/path_to/stanford-corenlp-4.5.4/stanford-corenlp-4.5.4.jar:/path_to/stanford-corenlp-4.5.4/stanford-corenlp-4.5.4-models-french.jar"; for file in `find . -name "*.jar"`; do export CLASSPATH="$CLASSPATH:`realpath $file`"; done
6. java -cp "*" edu.stanford.nlp.pipeline.StanfordCoreNLP -props StanfordCoreNLP-french.properties -annotators "tokenize, ssplit, pos, depparse, lemma" -ssplit.eolonly true -tokenize.whitespace true -numThreads 8 -outputFormat conll < /content/drive/MyDrive/input_txt/celine.tok.fr > /content/drive/MyDrive/input_txt/celinef.mai.en.conll
