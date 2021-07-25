# StackOverFlow-Tag-Prediction

* Stack Overflow is the largest, most trusted online community for developers to learn, share their programming knowledge, and build their
  careers.
  
* Stack Overflow is something which every programmer use one way or another. Each month, over 50 million developers come to Stack
  Overflow to learn, share their knowledge, and build their careers. It features questions and answers on a wide range of topics in computer
  programming. The website serves as a platform for users to ask and answer questions, and, through membership and active participation,
  to vote questions and answers up or down and edit questions and answers in a fashion similar to a wiki or Digg. As of April 2014 Stack
  Overflow has over 4,000,000 registered users, and it exceeded 10,000,000 questions in late August 2015. Based on the type of tags
  assigned to questions, the top eight most discussed topics on the site are: Java, JavaScript, C#, PHP, Android, jQuery, Python and HTML.

* Problem Statemtent
  Suggest the tags based on the content that was there in the question posted on Stackoverflow.

* Source: https://www.kaggle.com/c/facebook-recruiting-iii-keyword-extraction/
  (https://www.kaggle.com/c/facebook-recruiting-iii-keyword-extraction/)

* Source / useful links

  Data Source : https://www.kaggle.com/c/facebook-recruiting-iii-keyword-extraction/data (https://www.kaggle.com/c/facebook-recruiting-iii-
  keyword-extraction/data)

  Youtube : https://youtu.be/nNDqbUhtIRg (https://youtu.be/nNDqbUhtIRg)

  Research paper : https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/tagging-1.pdf (https://www.microsoft.com/en-
  us/research/wp-content/uploads/2016/02/tagging-1.pdf)

  Research paper : https://dl.acm.org/citation.cfm?id=2660970&dl=ACM&coll=DL (https://dl.acm.org/citation.cfm?
  id=2660970&dl=ACM&coll=DL)

*  Real World / Business Objectives and Constraints
    1. Predict as many tags as possible with high precision and recall.
    2. Incorrect tags could impact customer experience on StackOverflow.
    3. No strict latency constraints.


* Procedure for solving CaseStudy:

      1. The major objective is Predict as many tags as possible with high precision and recall And the Performance metric used = Mean Average F1Score                because it takes Frequency of Tags into Account.
      2. We loaded Data using pandas.
      3. Did Ananlysis of Tag and found most frequent tags are Programming Languages like:
                            C#,Java,php,Javascript,Android
      4. Did Analysis of Titles by finding titles similar to above programming languages.
      5. Did Preprocessing and cleaning of Data and took 1M points for Analysis and 5500 tags.
      6. Due to compute resources took only 0.5M points with 500 tags .
      7. Furthher reduced to 100K points and 500 tags.
      8. perfromed TFIDF Vectorzer and did SVM One Vs Rest .
      9. Performd CountVect with n_gram=(1,4), took top 10K featuress.
      10.Applied GridSearch for hypertuning with Logistic Regression One Vs Rest.
      11.Found Best HyperParam of C = 1
      12.Applied Logistic Regression One Vs Rest
      13.On DataSet of 100K [80K train data and 20K test data], Micro Avg F1 Score comes out to be 0.425.  
