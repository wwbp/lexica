# Lexica

A list of data driven lexica developed by the World Well-Being Project.


### Age and Gender Lexica

Read the full publication [here](http://wwbp.org/publications.html#p83). 

#### Citation

```
@inproceedings{sap2014developing,
author={Sap, Maarten and Park, Greg and Eichstaedt, Johannes C and Kern, Margaret L and Stillwell, David J and Kosinski, Michal and Ungar, Lyle H and Schwartz, H Andrew},
title={Developing age and gender predictive lexica over social media},
booktitle={Proceedings of the 2014 Conference on Empirical Methods in Natural Language Processing (EMNLP)},
year={2014},
}
```

### PERMA Lexicon

Read the full publication [here](http://wwbp.org/publications.html#p83). 

#### Citation

```
@{h. andrew schwartz2016predicting,
author={H. Andrew Schwartz, Maarten Sap, Margaret L. Kern, Johannes C. Eichstaedt, Adam Kapelner, Megha Agrawal, Eduardo Blanco, Lukasz Dziurzynski, Gregory Park, David Stillwell, Michal Kosinski, Martin E.P. Seligman, Lyle H. Ungar.},
title={Predicting Individual Well-Being Through the Language of Social Media},
year={2016},
pages={516-527}
}
```

### Spanish PERMA Lexicon

Read the full publication [here](http://wwbp.org/publications.html#p91). 

#### Citation

```
@inproceedings{smith2016does,
  title={Does ‘well-being’translate on Twitter?},
  author={Smith, Laura and Giorgi, Salvatore and Solanki, Rishi and Eichstaedt, Johannes and Schwartz, H Andrew and Abdul-Mageed, Muhammad and Buffone, Anneke and Ungar, Lyle},
  booktitle={Proceedings of the 2016 Conference on Empirical Methods in Natural Language Processing},
  pages={2042--2047},
  year={2016}
}
```

### Affect and Intensity Lexicon

Read the full publication [here](http://wwbp.org/publications.html#p83). 

#### Citation

```
@inproceedings{preoctiuc2016modelling,
  title={Modelling valence and arousal in facebook posts},
  author={Preo{\c{t}}iuc-Pietro, Daniel and Schwartz, H Andrew and Park, Gregory and Eichstaedt, Johannes and Kern, Margaret and Ungar, Lyle and Shulman, Elisabeth},
  booktitle={Proceedings of the 7th Workshop on Computational Approaches to Subjectivity, Sentiment and Social Media Analysis},
  pages={9--15},
  year={2016}
}
```

### Prospection Lexicon: Temporal Orientation

Read the full publication [here](http://wwbp.org/publications.html#p37). 

#### Citation

```
@inproceedings{schwartz2015extracting,
  title={Extracting human temporal orientation from Facebook language},
  author={Schwartz, H Andrew and Park, Gregory and Sap, Maarten and Weingarten, Evan and Eichstaedt, Johannes and Kern, Margaret and Stillwell, David and Kosinski, Michal and Berger, Jonah and Seligman, Martin and others},
  booktitle={Proceedings of the 2015 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies},
  pages={409--419},
  year={2015}
}
```

## Example 

A weighted lexicon is often applied as the sum of all weighted word relative frequencies over a document:

![image](http://latex.codecogs.com/svg.latex?usage_{lex}=\sum_{word\in%20lex}w_{lex}(word)\frac{freq(word,doc)}{freq(*,doc)})
 
where ![image](http://latex.codecogs.com/svg.latex?w_{lex}(word)) is the lexicon  ![image](http://latex.codecogs.com/svg.latex?(lex)) weight for the word, ![image](http://latex.codecogs.com/svg.latex?freq(word,%20doc))  is frequency of the word in the document (or for a given user), and ![image](http://latex.codecogs.com/svg.latex?freq(*,%20doc)) is the total word count for that document (or user).

For example, let's say a lexicon has the following weights for words a, b, and c:

![image](http://latex.codecogs.com/svg.latex?\textbf{lex:}\%20a:%203,%20b:%2087,%20c:%20-15)

and two documents with the following frequencies of words:

![image](http://latex.codecogs.com/svg.latex?document_1:%20a:%202,%20b:%2010,%20c:%203,%20d:%200,%20e:%206,%20f:%204)

![image](http://latex.codecogs.com/svg.latex?document_2:%20a:%205,%20b:%203,%20c:%208,%20d:%204,%20e:%200,%20f:%2010)

therefore the total word uses in the documents are:

![image](http://latex.codecogs.com/svg.latex?document_1:%202%20+%2010%20+%203%20+%200%20+%206%20+%204%20=%2025)

![image](http://latex.codecogs.com/svg.latex?document_2:%205%20+%203%20+%208%20+%204%20+%200%20+%2010%20=%2030)

The documents' lexicon usage are given by summing the weighted relative frequencies:

![image](http://latex.codecogs.com/svg.latex?doc_{1,lex}%20=%20(2/25)\cdot3%20+%20(10/25)\cdot87%20+%20(3/25)\cdot(-15)%20=%2034.24)

![image](http://latex.codecogs.com/svg.latex?doc_{2,lex}%20=%20(5/30)\cdot3%20+%20(3/30)\cdot87%20+%20(8/30)\cdot(-15)%20=%205.2)

Once the usages have been computed, the intercept of the lexicon needs to be added to the usages:

![image](http://latex.codecogs.com/svg.latex?intercept_{lex}%20=%2023.2189)

![image](http://latex.codecogs.com/svg.latex?lex_{doc1}%20=%2034.24%20+%2023.2189%20=%2056.4589)

![image](http://latex.codecogs.com/svg.latex?lex_{doc2}%20=%205.2%20+%2023.2189%20=%2028.4189)

If the lexicon used represents age, ![image](http://latex.codecogs.com/svg.latex?lex_{doc1}) and ![image](http://latex.codecogs.com/svg.latex?lex_{doc2})  are the predicted ages for both documents. If it represents gender, simply take the sign of the result and if it's positive, the document is female, else it's male.

## License

Unless specified in the lexica's subdirectory all lexica are licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 3.0 Unported License.

## Background

Developed by the [World Well-Being Project](https://www.wwbp.org) based out of the University of Pennsylvania and Stony Brook University.


